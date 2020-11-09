---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316898"
---
# <span data-ttu-id="87169-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="87169-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="87169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87169-102">SYNOPSIS</span></span>
<span data-ttu-id="87169-103">Создание общего файлового файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="87169-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="87169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87169-104">SYNTAX</span></span>

### <span data-ttu-id="87169-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87169-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87169-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="87169-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87169-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87169-107">DESCRIPTION</span></span>
<span data-ttu-id="87169-108">Командлет **New-AzRmStorageShare** создает файловый общий доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="87169-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="87169-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87169-109">EXAMPLES</span></span>

### <span data-ttu-id="87169-110">Пример 1. Создайте общую файловую систему хранения данных с именем учетной записи хранения и именем общего доступа, используя метаданные и общую квоту в качестве 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="87169-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="87169-111">Эта команда создает общую файловую систему хранилища с метаданными и общей квотой в формате 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="87169-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="87169-112">Пример 2: создание общей файловой системы хранения с помощью объекта учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="87169-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="87169-113">Эта команда создает общую файловую систему хранилища с объектом учетной записи хранения и именем общего доступа.</span><span class="sxs-lookup"><span data-stu-id="87169-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="87169-114">Пример 3: создание общего файла хранилища с accesstier в качестве горячего</span><span class="sxs-lookup"><span data-stu-id="87169-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="87169-115">Эта команда создает общую файловую систему хранилища, в которой accesstier является горячим.</span><span class="sxs-lookup"><span data-stu-id="87169-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="87169-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87169-116">PARAMETERS</span></span>

### <span data-ttu-id="87169-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="87169-117">-AccessTier</span></span>
<span data-ttu-id="87169-118">Уровень доступа для определенного общего доступа.</span><span class="sxs-lookup"><span data-stu-id="87169-118">Access tier for specific share.</span></span> <span data-ttu-id="87169-119">StorageV2 учетная запись может выбрать один из TransactionOptimized (по умолчанию), горячий и крутой.</span><span class="sxs-lookup"><span data-stu-id="87169-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="87169-120">FileStorage учетная запись может выбрать платный.</span><span class="sxs-lookup"><span data-stu-id="87169-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="87169-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87169-121">-DefaultProfile</span></span>
<span data-ttu-id="87169-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87169-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87169-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="87169-123">-Metadata</span></span>
<span data-ttu-id="87169-124">Общий доступ к метаданным</span><span class="sxs-lookup"><span data-stu-id="87169-124">Share Metadata</span></span>

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

### <span data-ttu-id="87169-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87169-125">-Name</span></span>
<span data-ttu-id="87169-126">Имя общего файлового файла Azure</span><span class="sxs-lookup"><span data-stu-id="87169-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87169-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="87169-127">-QuotaGiB</span></span>
<span data-ttu-id="87169-128">Предоставление общего доступа к квоте в Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="87169-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="87169-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87169-129">-ResourceGroupName</span></span>
<span data-ttu-id="87169-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87169-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="87169-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="87169-131">-StorageAccount</span></span>
<span data-ttu-id="87169-132">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="87169-132">Storage account object</span></span>

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

### <span data-ttu-id="87169-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87169-133">-StorageAccountName</span></span>
<span data-ttu-id="87169-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="87169-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="87169-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87169-135">-Confirm</span></span>
<span data-ttu-id="87169-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87169-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87169-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87169-137">-WhatIf</span></span>
<span data-ttu-id="87169-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87169-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87169-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87169-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87169-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87169-140">CommonParameters</span></span>
<span data-ttu-id="87169-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87169-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87169-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87169-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87169-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87169-143">INPUTS</span></span>

### <span data-ttu-id="87169-144">System. String</span><span class="sxs-lookup"><span data-stu-id="87169-144">System.String</span></span>

### <span data-ttu-id="87169-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87169-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="87169-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87169-146">OUTPUTS</span></span>

### <span data-ttu-id="87169-147">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="87169-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="87169-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="87169-148">NOTES</span></span>

## <span data-ttu-id="87169-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87169-149">RELATED LINKS</span></span>
