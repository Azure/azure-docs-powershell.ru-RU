---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 7612b323600b2f076c30225994d6e475d66c01ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973304"
---
# <span data-ttu-id="f39d5-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f39d5-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="f39d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f39d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f39d5-103">Изменяет файловую папку хранилища.</span><span class="sxs-lookup"><span data-stu-id="f39d5-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="f39d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f39d5-104">SYNTAX</span></span>

### <span data-ttu-id="f39d5-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f39d5-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39d5-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f39d5-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f39d5-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f39d5-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f39d5-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="f39d5-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39d5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39d5-109">DESCRIPTION</span></span>
<span data-ttu-id="f39d5-110">Для **файлового пространства New-AzRmStorageShare** будет модификатор.</span><span class="sxs-lookup"><span data-stu-id="f39d5-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="f39d5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f39d5-111">EXAMPLES</span></span>

### <span data-ttu-id="f39d5-112">Пример 1. Изменяет метаданные и квоту для файла хранилища с помощью имени учетной записи хранения и имени для нее.</span><span class="sxs-lookup"><span data-stu-id="f39d5-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="f39d5-113">Эта команда изменяет метаданные и квоту для файла хранилища с помощью имени учетной записи хранения и имени, а также показывает результат изменения с возвращенным объектом.</span><span class="sxs-lookup"><span data-stu-id="f39d5-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="f39d5-114">Пример 2. Модификирует метаданные в папке хранилища с объектом учетной записи хранения и именем</span><span class="sxs-lookup"><span data-stu-id="f39d5-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="f39d5-115">Эта команда изменяет метаданные в папке хранилища с объектом учетной записи хранения и именем.</span><span class="sxs-lookup"><span data-stu-id="f39d5-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="f39d5-116">Пример 3. Модификаторы квоты для всех файлов хранилища в учетной записи хранения с конвейером</span><span class="sxs-lookup"><span data-stu-id="f39d5-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="f39d5-117">Эта команда изменяет квоту на 5000 giB для всех файловых папков хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="f39d5-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="f39d5-118">Пример 4. Изменение папки с файлами хранилища с помощью accesstier</span><span class="sxs-lookup"><span data-stu-id="f39d5-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="f39d5-119">Эта команда изменяет файл хранилища с помощью accesstier на cool.</span><span class="sxs-lookup"><span data-stu-id="f39d5-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="f39d5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f39d5-120">PARAMETERS</span></span>

### <span data-ttu-id="f39d5-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="f39d5-121">-AccessTier</span></span>
<span data-ttu-id="f39d5-122">Доступ к уровням для определенного уровня доступа.</span><span class="sxs-lookup"><span data-stu-id="f39d5-122">Access tier for specific share.</span></span> <span data-ttu-id="f39d5-123">Учетная запись StorageV2 может выбрать между TransactionOptimized (по умолчанию), Hot и Cool.</span><span class="sxs-lookup"><span data-stu-id="f39d5-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="f39d5-124">Для учетной записи FileStorage можно выбрать premium.</span><span class="sxs-lookup"><span data-stu-id="f39d5-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="f39d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39d5-125">-DefaultProfile</span></span>
<span data-ttu-id="f39d5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f39d5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f39d5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f39d5-127">-InputObject</span></span>
<span data-ttu-id="f39d5-128">Объект "Поделиться хранилищем"</span><span class="sxs-lookup"><span data-stu-id="f39d5-128">Storage Share object</span></span>

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

### <span data-ttu-id="f39d5-129">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="f39d5-129">-Metadata</span></span>
<span data-ttu-id="f39d5-130">Совместноеирование метаданных</span><span class="sxs-lookup"><span data-stu-id="f39d5-130">Share Metadata</span></span>

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

### <span data-ttu-id="f39d5-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f39d5-131">-Name</span></span>
<span data-ttu-id="f39d5-132">Имя "Поделиться"</span><span class="sxs-lookup"><span data-stu-id="f39d5-132">Share Name</span></span>

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

### <span data-ttu-id="f39d5-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="f39d5-133">-QuotaGiB</span></span>
<span data-ttu-id="f39d5-134">Поделиться квотой в Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="f39d5-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="f39d5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39d5-135">-ResourceGroupName</span></span>
<span data-ttu-id="f39d5-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f39d5-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="f39d5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f39d5-137">-ResourceId</span></span>
<span data-ttu-id="f39d5-138">Ввести ИД ресурса для обмена файлами.</span><span class="sxs-lookup"><span data-stu-id="f39d5-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="f39d5-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f39d5-139">-StorageAccount</span></span>
<span data-ttu-id="f39d5-140">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f39d5-140">Storage account object</span></span>

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

### <span data-ttu-id="f39d5-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f39d5-141">-StorageAccountName</span></span>
<span data-ttu-id="f39d5-142">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f39d5-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="f39d5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f39d5-143">-Confirm</span></span>
<span data-ttu-id="f39d5-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39d5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39d5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39d5-145">-WhatIf</span></span>
<span data-ttu-id="f39d5-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f39d5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39d5-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f39d5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39d5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39d5-148">CommonParameters</span></span>
<span data-ttu-id="f39d5-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39d5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39d5-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39d5-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39d5-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f39d5-151">INPUTS</span></span>

### <span data-ttu-id="f39d5-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f39d5-152">System.String</span></span>

### <span data-ttu-id="f39d5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f39d5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f39d5-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="f39d5-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f39d5-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f39d5-155">OUTPUTS</span></span>

### <span data-ttu-id="f39d5-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="f39d5-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f39d5-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f39d5-157">NOTES</span></span>

## <span data-ttu-id="f39d5-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f39d5-158">RELATED LINKS</span></span>
