---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077507"
---
# <span data-ttu-id="72c5a-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="72c5a-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="72c5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="72c5a-103">Восстановление удаленного общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="72c5a-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="72c5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72c5a-104">SYNTAX</span></span>

### <span data-ttu-id="72c5a-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72c5a-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72c5a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="72c5a-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c5a-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="72c5a-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72c5a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72c5a-108">DESCRIPTION</span></span>
<span data-ttu-id="72c5a-109">Командлет **RESTORE-AzRmStorageShare** восстанавливает удаленную общую папку в течение допустимых дней хранения, если включено программное удаление общего доступа.</span><span class="sxs-lookup"><span data-stu-id="72c5a-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="72c5a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72c5a-110">EXAMPLES</span></span>

### <span data-ttu-id="72c5a-111">Пример 1: удаление и восстановление общего доступа</span><span class="sxs-lookup"><span data-stu-id="72c5a-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="72c5a-112">Эта команда сначала удаляет файловый ресурс, а затем список общих ресурсов и просмотр удаленной версии общего доступа, а затем снова восстановите ее в обычном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="72c5a-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="72c5a-113">Перед удалением общего доступа необходимо включить программное удаление с помощью Update-AzStorageFileServiceProperty.</span><span class="sxs-lookup"><span data-stu-id="72c5a-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="72c5a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72c5a-114">PARAMETERS</span></span>

### <span data-ttu-id="72c5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c5a-115">-DefaultProfile</span></span>
<span data-ttu-id="72c5a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72c5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72c5a-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="72c5a-117">-DeletedShareVersion</span></span>
<span data-ttu-id="72c5a-118">Удалена версия общего доступа, из которой будет восстановлено.</span><span class="sxs-lookup"><span data-stu-id="72c5a-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72c5a-119">-InputObject</span></span>
<span data-ttu-id="72c5a-120">Объект общего доступа удален</span><span class="sxs-lookup"><span data-stu-id="72c5a-120">Deleted Share object</span></span>

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

### <span data-ttu-id="72c5a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72c5a-121">-Name</span></span>
<span data-ttu-id="72c5a-122">Удаленное имя общего доступа, которое будет восстановлено.</span><span class="sxs-lookup"><span data-stu-id="72c5a-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="72c5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="72c5a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72c5a-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="72c5a-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="72c5a-125">-StorageAccount</span></span>
<span data-ttu-id="72c5a-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="72c5a-126">Storage account object</span></span>

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

### <span data-ttu-id="72c5a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="72c5a-127">-StorageAccountName</span></span>
<span data-ttu-id="72c5a-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="72c5a-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="72c5a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72c5a-129">-Confirm</span></span>
<span data-ttu-id="72c5a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72c5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72c5a-131">-WhatIf</span></span>
<span data-ttu-id="72c5a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72c5a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72c5a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72c5a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c5a-134">CommonParameters</span></span>
<span data-ttu-id="72c5a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72c5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c5a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c5a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c5a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72c5a-137">INPUTS</span></span>

### <span data-ttu-id="72c5a-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="72c5a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="72c5a-139">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="72c5a-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="72c5a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72c5a-140">OUTPUTS</span></span>

### <span data-ttu-id="72c5a-141">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="72c5a-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="72c5a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="72c5a-142">NOTES</span></span>

## <span data-ttu-id="72c5a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72c5a-143">RELATED LINKS</span></span>
