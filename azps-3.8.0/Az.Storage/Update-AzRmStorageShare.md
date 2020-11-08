---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065962"
---
# <span data-ttu-id="c809a-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c809a-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="c809a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c809a-102">SYNOPSIS</span></span>
<span data-ttu-id="c809a-103">Изменение общего файлового файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="c809a-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="c809a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c809a-104">SYNTAX</span></span>

### <span data-ttu-id="c809a-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c809a-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c809a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c809a-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c809a-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="c809a-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c809a-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="c809a-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c809a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c809a-109">DESCRIPTION</span></span>
<span data-ttu-id="c809a-110">Командлет **New-AzRmStorageShare** изменяет файловый общий доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="c809a-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="c809a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c809a-111">EXAMPLES</span></span>

### <span data-ttu-id="c809a-112">Пример 1: изменение метаданных общего файлового файла хранилища и предоставление общего доступа к квоте с именем учетной записи хранения и именем общего доступа</span><span class="sxs-lookup"><span data-stu-id="c809a-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="c809a-113">Эта команда изменяет метаданные общего файлового файла хранилища и общую квоту с учетной записью хранения и именем общего доступа, а также отображает результат изменения с помощью возвращенного объекта общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c809a-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="c809a-114">Пример 2: изменение метаданных в общей папке хранилища с помощью объекта учетной записи хранения и имени общего файла</span><span class="sxs-lookup"><span data-stu-id="c809a-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="c809a-115">Эта команда изменяет метаданные в общей папке хранилища, используя объект учетной записи хранения и имя общего файла.</span><span class="sxs-lookup"><span data-stu-id="c809a-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="c809a-116">Пример 3: изменение квоты общего доступа для всех общих файлов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="c809a-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="c809a-117">Эта команда изменяет квоту общего доступа как 5000 GiB для всех общих файлов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="c809a-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="c809a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c809a-118">PARAMETERS</span></span>

### <span data-ttu-id="c809a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c809a-119">-DefaultProfile</span></span>
<span data-ttu-id="c809a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c809a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c809a-121">-InputObject</span></span>
<span data-ttu-id="c809a-122">Объект общего доступа к хранилищу</span><span class="sxs-lookup"><span data-stu-id="c809a-122">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c809a-123">-Metadata</span></span>
<span data-ttu-id="c809a-124">Общий доступ к метаданным</span><span class="sxs-lookup"><span data-stu-id="c809a-124">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c809a-125">-Name</span></span>
<span data-ttu-id="c809a-126">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="c809a-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="c809a-127">-QuotaGiB</span></span>
<span data-ttu-id="c809a-128">Предоставление общего доступа к квоте в Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="c809a-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c809a-129">-ResourceGroupName</span></span>
<span data-ttu-id="c809a-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c809a-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c809a-131">-ResourceId</span></span>
<span data-ttu-id="c809a-132">Введите идентификатор ресурса для общего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="c809a-132">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c809a-133">-StorageAccount</span></span>
<span data-ttu-id="c809a-134">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c809a-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c809a-135">-StorageAccountName</span></span>
<span data-ttu-id="c809a-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c809a-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c809a-137">-Confirm</span></span>
<span data-ttu-id="c809a-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c809a-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c809a-139">-WhatIf</span></span>
<span data-ttu-id="c809a-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c809a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c809a-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c809a-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c809a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c809a-142">CommonParameters</span></span>
<span data-ttu-id="c809a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c809a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c809a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c809a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c809a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c809a-145">INPUTS</span></span>

### <span data-ttu-id="c809a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c809a-146">System.String</span></span>

### <span data-ttu-id="c809a-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c809a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c809a-148">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c809a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c809a-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c809a-149">OUTPUTS</span></span>

### <span data-ttu-id="c809a-150">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="c809a-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c809a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="c809a-151">NOTES</span></span>

## <span data-ttu-id="c809a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c809a-152">RELATED LINKS</span></span>
