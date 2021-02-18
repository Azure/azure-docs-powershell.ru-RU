---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231617"
---
# <span data-ttu-id="bc4b9-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bc4b9-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="bc4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4b9-103">Создается файл хранилища.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="bc4b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc4b9-104">SYNTAX</span></span>

### <span data-ttu-id="bc4b9-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc4b9-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc4b9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bc4b9-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc4b9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc4b9-107">DESCRIPTION</span></span>
<span data-ttu-id="bc4b9-108">Для создания файловой папки Создается папка хранилища с этим cmdlet- и более новых данных **AzRmStorageShare.**</span><span class="sxs-lookup"><span data-stu-id="bc4b9-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="bc4b9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc4b9-109">EXAMPLES</span></span>

### <span data-ttu-id="bc4b9-110">Пример 1. Создайте файл хранилища с именем учетной записи хранения и именем, метаданными и квотой в 100 ГБ.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="bc4b9-111">Эта команда создает файл хранилища с метаданными и квотой в 100 ГБ.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="bc4b9-112">Пример 2. Создание папки хранения с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bc4b9-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="bc4b9-113">Эта команда создает папку хранилища с объектом учетной записи хранения и именем.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="bc4b9-114">Пример 3. Создание папки хранения с помощью accesstier Hot</span><span class="sxs-lookup"><span data-stu-id="bc4b9-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="bc4b9-115">Эта команда создает обойму для файлов хранилища с помощью accesstier Hot.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="bc4b9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc4b9-116">PARAMETERS</span></span>

### <span data-ttu-id="bc4b9-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="bc4b9-117">-AccessTier</span></span>
<span data-ttu-id="bc4b9-118">Уровень доступа для определенного уровня доступа.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-118">Access tier for specific share.</span></span> <span data-ttu-id="bc4b9-119">Учетная запись StorageV2 может выбрать между TransactionOptimized (по умолчанию), Hot и Cool.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="bc4b9-120">Для учетной записи FileStorage можно выбрать premium.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="bc4b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4b9-121">-DefaultProfile</span></span>
<span data-ttu-id="bc4b9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc4b9-123">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="bc4b9-123">-Metadata</span></span>
<span data-ttu-id="bc4b9-124">Совместноеирование метаданных</span><span class="sxs-lookup"><span data-stu-id="bc4b9-124">Share Metadata</span></span>

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

### <span data-ttu-id="bc4b9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bc4b9-125">-Name</span></span>
<span data-ttu-id="bc4b9-126">Имя файла в Azure</span><span class="sxs-lookup"><span data-stu-id="bc4b9-126">Azure File share name</span></span>

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

### <span data-ttu-id="bc4b9-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="bc4b9-127">-QuotaGiB</span></span>
<span data-ttu-id="bc4b9-128">Поделиться квотой в Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="bc4b9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4b9-129">-ResourceGroupName</span></span>
<span data-ttu-id="bc4b9-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="bc4b9-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bc4b9-131">-StorageAccount</span></span>
<span data-ttu-id="bc4b9-132">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bc4b9-132">Storage account object</span></span>

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

### <span data-ttu-id="bc4b9-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bc4b9-133">-StorageAccountName</span></span>
<span data-ttu-id="bc4b9-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="bc4b9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc4b9-135">-Confirm</span></span>
<span data-ttu-id="bc4b9-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4b9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4b9-137">-WhatIf</span></span>
<span data-ttu-id="bc4b9-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc4b9-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4b9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4b9-140">CommonParameters</span></span>
<span data-ttu-id="bc4b9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc4b9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4b9-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc4b9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4b9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc4b9-143">INPUTS</span></span>

### <span data-ttu-id="bc4b9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bc4b9-144">System.String</span></span>

### <span data-ttu-id="bc4b9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bc4b9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bc4b9-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc4b9-146">OUTPUTS</span></span>

### <span data-ttu-id="bc4b9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="bc4b9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="bc4b9-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc4b9-148">NOTES</span></span>

## <span data-ttu-id="bc4b9-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc4b9-149">RELATED LINKS</span></span>
