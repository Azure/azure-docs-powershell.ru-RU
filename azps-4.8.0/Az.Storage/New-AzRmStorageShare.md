---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 81e380f6b6d4b1c35a6cff98093dfedf94119a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078589"
---
# <span data-ttu-id="abf17-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf17-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="abf17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abf17-102">SYNOPSIS</span></span>
<span data-ttu-id="abf17-103">Создание общего файлового файла хранилища.</span><span class="sxs-lookup"><span data-stu-id="abf17-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="abf17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abf17-104">SYNTAX</span></span>

### <span data-ttu-id="abf17-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="abf17-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abf17-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="abf17-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf17-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abf17-107">DESCRIPTION</span></span>
<span data-ttu-id="abf17-108">Командлет **New-AzRmStorageShare** создает файловый общий доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="abf17-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="abf17-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abf17-109">EXAMPLES</span></span>

### <span data-ttu-id="abf17-110">Пример 1. Создайте общую файловую систему хранения данных с именем учетной записи хранения и именем общего доступа, используя метаданные и общую квоту в качестве 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="abf17-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="abf17-111">Эта команда создает общую файловую систему хранилища с метаданными и общей квотой в формате 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="abf17-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="abf17-112">Пример 2: создание общей файловой системы хранения с помощью объекта учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="abf17-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="abf17-113">Эта команда создает общую файловую систему хранилища с объектом учетной записи хранения и именем общего доступа.</span><span class="sxs-lookup"><span data-stu-id="abf17-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="abf17-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abf17-114">PARAMETERS</span></span>

### <span data-ttu-id="abf17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf17-115">-DefaultProfile</span></span>
<span data-ttu-id="abf17-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abf17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf17-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="abf17-117">-Metadata</span></span>
<span data-ttu-id="abf17-118">Общий доступ к метаданным</span><span class="sxs-lookup"><span data-stu-id="abf17-118">Share Metadata</span></span>

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

### <span data-ttu-id="abf17-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="abf17-119">-Name</span></span>
<span data-ttu-id="abf17-120">Имя общего файлового файла Azure</span><span class="sxs-lookup"><span data-stu-id="abf17-120">Azure File share name</span></span>

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

### <span data-ttu-id="abf17-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="abf17-121">-QuotaGiB</span></span>
<span data-ttu-id="abf17-122">Предоставление общего доступа к квоте в Gibibyte.</span><span class="sxs-lookup"><span data-stu-id="abf17-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="abf17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf17-123">-ResourceGroupName</span></span>
<span data-ttu-id="abf17-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="abf17-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="abf17-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf17-125">-StorageAccount</span></span>
<span data-ttu-id="abf17-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="abf17-126">Storage account object</span></span>

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

### <span data-ttu-id="abf17-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="abf17-127">-StorageAccountName</span></span>
<span data-ttu-id="abf17-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="abf17-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="abf17-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abf17-129">-Confirm</span></span>
<span data-ttu-id="abf17-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="abf17-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf17-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf17-131">-WhatIf</span></span>
<span data-ttu-id="abf17-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="abf17-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf17-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="abf17-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf17-134">CommonParameters</span></span>
<span data-ttu-id="abf17-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abf17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf17-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf17-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf17-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abf17-137">INPUTS</span></span>

### <span data-ttu-id="abf17-138">System. String</span><span class="sxs-lookup"><span data-stu-id="abf17-138">System.String</span></span>

### <span data-ttu-id="abf17-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf17-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="abf17-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abf17-140">OUTPUTS</span></span>

### <span data-ttu-id="abf17-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="abf17-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="abf17-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="abf17-142">NOTES</span></span>

## <span data-ttu-id="abf17-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abf17-143">RELATED LINKS</span></span>
