---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 0ce045df6e19a964cf92d5550cfb94e30c808a3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007539"
---
# <span data-ttu-id="d6dee-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d6dee-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="d6dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6dee-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dee-103">Восстановление удаленной файловой папки.</span><span class="sxs-lookup"><span data-stu-id="d6dee-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="d6dee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d6dee-104">SYNTAX</span></span>

### <span data-ttu-id="d6dee-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6dee-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6dee-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d6dee-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6dee-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="d6dee-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6dee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6dee-108">DESCRIPTION</span></span>
<span data-ttu-id="d6dee-109">С **его учетом** можно восстановить удаленную папку в течение допустимого дня хранения, если совместное удаление включено.</span><span class="sxs-lookup"><span data-stu-id="d6dee-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="d6dee-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d6dee-110">EXAMPLES</span></span>

### <span data-ttu-id="d6dee-111">Пример 1. Удаление и восстановление делиться</span><span class="sxs-lookup"><span data-stu-id="d6dee-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="d6dee-112">Эта команда сначала удаляет файл, а затем делится списком и видит удаленную версию, а затем возвращает ее в обычный файл.</span><span class="sxs-lookup"><span data-stu-id="d6dee-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="d6dee-113">Требуется включить неявное удаление с помощью Update-AzStorageFileServiceProperty, прежде чем удалять ее.</span><span class="sxs-lookup"><span data-stu-id="d6dee-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="d6dee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6dee-114">PARAMETERS</span></span>

### <span data-ttu-id="d6dee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dee-115">-DefaultProfile</span></span>
<span data-ttu-id="d6dee-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6dee-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="d6dee-117">-DeletedShareVersion</span></span>
<span data-ttu-id="d6dee-118">Удалена версия "Поделиться", из которой будет восстановлена версия.</span><span class="sxs-lookup"><span data-stu-id="d6dee-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="d6dee-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6dee-119">-InputObject</span></span>
<span data-ttu-id="d6dee-120">Удаленный объект "Поделиться"</span><span class="sxs-lookup"><span data-stu-id="d6dee-120">Deleted Share object</span></span>

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

### <span data-ttu-id="d6dee-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d6dee-121">-Name</span></span>
<span data-ttu-id="d6dee-122">Удалено имя для обмена, которое будет восстановлено.</span><span class="sxs-lookup"><span data-stu-id="d6dee-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="d6dee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6dee-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6dee-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d6dee-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6dee-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6dee-125">-StorageAccount</span></span>
<span data-ttu-id="d6dee-126">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d6dee-126">Storage account object</span></span>

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

### <span data-ttu-id="d6dee-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6dee-127">-StorageAccountName</span></span>
<span data-ttu-id="d6dee-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d6dee-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="d6dee-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6dee-129">-Confirm</span></span>
<span data-ttu-id="d6dee-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d6dee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6dee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6dee-131">-WhatIf</span></span>
<span data-ttu-id="d6dee-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6dee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6dee-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d6dee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6dee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dee-134">CommonParameters</span></span>
<span data-ttu-id="d6dee-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dee-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dee-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dee-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6dee-137">INPUTS</span></span>

### <span data-ttu-id="d6dee-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6dee-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d6dee-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="d6dee-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="d6dee-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6dee-140">OUTPUTS</span></span>

### <span data-ttu-id="d6dee-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="d6dee-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="d6dee-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d6dee-142">NOTES</span></span>

## <span data-ttu-id="d6dee-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6dee-143">RELATED LINKS</span></span>
