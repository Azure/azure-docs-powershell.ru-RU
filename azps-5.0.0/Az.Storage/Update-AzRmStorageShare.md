---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316892"
---
# <span data-ttu-id="77278-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="77278-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="77278-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77278-102">SYNOPSIS</span></span>
<span data-ttu-id="77278-103">Изменение общего файлового файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="77278-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="77278-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77278-104">SYNTAX</span></span>

### <span data-ttu-id="77278-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77278-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77278-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="77278-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77278-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="77278-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77278-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="77278-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77278-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77278-109">DESCRIPTION</span></span>
<span data-ttu-id="77278-110">Командлет **New-AzRmStorageShare** изменяет файловый общий доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="77278-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="77278-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77278-111">EXAMPLES</span></span>

### <span data-ttu-id="77278-112">Пример 1: изменение метаданных общего файлового файла хранилища и предоставление общего доступа к квоте с именем учетной записи хранения и именем общего доступа</span><span class="sxs-lookup"><span data-stu-id="77278-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="77278-113">Эта команда изменяет метаданные общего файлового файла хранилища и общую квоту с учетной записью хранения и именем общего доступа, а также отображает результат изменения с помощью возвращенного объекта общего доступа.</span><span class="sxs-lookup"><span data-stu-id="77278-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="77278-114">Пример 2: изменение метаданных в общей папке хранилища с помощью объекта учетной записи хранения и имени общего файла</span><span class="sxs-lookup"><span data-stu-id="77278-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="77278-115">Эта команда изменяет метаданные в общей папке хранилища, используя объект учетной записи хранения и имя общего файла.</span><span class="sxs-lookup"><span data-stu-id="77278-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="77278-116">Пример 3: изменение квоты общего доступа для всех общих файлов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="77278-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="77278-117">Эта команда изменяет квоту общего доступа как 5000 GiB для всех общих файлов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="77278-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="77278-118">Пример 4: изменение общего файла хранилища с помощью accesstier как круто</span><span class="sxs-lookup"><span data-stu-id="77278-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="77278-119">Эта команда изменяет общую файловую систему хранилища с accesstier как круто.</span><span class="sxs-lookup"><span data-stu-id="77278-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="77278-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77278-120">PARAMETERS</span></span>

### <span data-ttu-id="77278-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="77278-121">-AccessTier</span></span>
<span data-ttu-id="77278-122">Уровень доступа для определенного общего доступа.</span><span class="sxs-lookup"><span data-stu-id="77278-122">Access tier for specific share.</span></span> <span data-ttu-id="77278-123">StorageV2 учетная запись может выбрать один из TransactionOptimized (по умолчанию), горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="77278-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="77278-124">FileStorage учетная запись может выбрать платный.</span><span class="sxs-lookup"><span data-stu-id="77278-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77278-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77278-125">-DefaultProfile</span></span>
<span data-ttu-id="77278-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77278-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77278-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77278-127">-InputObject</span></span>
<span data-ttu-id="77278-128">Объект общего доступа к хранилищу</span><span class="sxs-lookup"><span data-stu-id="77278-128">Storage Share object</span></span>

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

### <span data-ttu-id="77278-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="77278-129">-Metadata</span></span>
<span data-ttu-id="77278-130">Общий доступ к метаданным</span><span class="sxs-lookup"><span data-stu-id="77278-130">Share Metadata</span></span>

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

### <span data-ttu-id="77278-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77278-131">-Name</span></span>
<span data-ttu-id="77278-132">Имя общего доступа</span><span class="sxs-lookup"><span data-stu-id="77278-132">Share Name</span></span>

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

### <span data-ttu-id="77278-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="77278-133">-QuotaGiB</span></span>
<span data-ttu-id="77278-134">Предоставление общего доступа к квоте в Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="77278-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="77278-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77278-135">-ResourceGroupName</span></span>
<span data-ttu-id="77278-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77278-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="77278-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77278-137">-ResourceId</span></span>
<span data-ttu-id="77278-138">Введите идентификатор ресурса для общего доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="77278-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="77278-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="77278-139">-StorageAccount</span></span>
<span data-ttu-id="77278-140">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="77278-140">Storage account object</span></span>

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

### <span data-ttu-id="77278-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="77278-141">-StorageAccountName</span></span>
<span data-ttu-id="77278-142">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="77278-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="77278-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77278-143">-Confirm</span></span>
<span data-ttu-id="77278-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77278-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77278-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77278-145">-WhatIf</span></span>
<span data-ttu-id="77278-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77278-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77278-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77278-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77278-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77278-148">CommonParameters</span></span>
<span data-ttu-id="77278-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77278-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77278-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77278-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77278-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77278-151">INPUTS</span></span>

### <span data-ttu-id="77278-152">System. String</span><span class="sxs-lookup"><span data-stu-id="77278-152">System.String</span></span>

### <span data-ttu-id="77278-153">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="77278-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="77278-154">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="77278-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="77278-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77278-155">OUTPUTS</span></span>

### <span data-ttu-id="77278-156">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="77278-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="77278-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="77278-157">NOTES</span></span>

## <span data-ttu-id="77278-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77278-158">RELATED LINKS</span></span>
