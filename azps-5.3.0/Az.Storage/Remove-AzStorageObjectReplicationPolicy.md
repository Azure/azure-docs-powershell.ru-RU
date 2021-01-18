---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505665"
---
# <span data-ttu-id="71316-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="71316-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="71316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71316-102">SYNOPSIS</span></span>
<span data-ttu-id="71316-103">Удаляет указанную политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="71316-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="71316-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="71316-104">SYNTAX</span></span>

### <span data-ttu-id="71316-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71316-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71316-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="71316-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71316-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="71316-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71316-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71316-108">DESCRIPTION</span></span>
<span data-ttu-id="71316-109">Для удаления указанной политики репликации объектов из учетной записи хранения удаляется cmdlet **Remove-AzStorageObjectReplicationPolicy.**</span><span class="sxs-lookup"><span data-stu-id="71316-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="71316-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="71316-110">EXAMPLES</span></span>

### <span data-ttu-id="71316-111">Пример 1. Удаление политики репликации объектов с определенным ид политики из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="71316-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="71316-112">Эта команда удаляет из учетной записи хранения политику репликации объектов с определенным ид политики.</span><span class="sxs-lookup"><span data-stu-id="71316-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="71316-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71316-113">PARAMETERS</span></span>

### <span data-ttu-id="71316-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71316-114">-DefaultProfile</span></span>
<span data-ttu-id="71316-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71316-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71316-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71316-116">-InputObject</span></span>
<span data-ttu-id="71316-117">Объект политики репликации объектов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="71316-117">Object Replication Policy object to Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71316-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71316-118">-PassThru</span></span>
<span data-ttu-id="71316-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="71316-119">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71316-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="71316-120">-PolicyId</span></span>
<span data-ttu-id="71316-121">ИД политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="71316-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="71316-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71316-122">-ResourceGroupName</span></span>
<span data-ttu-id="71316-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71316-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="71316-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="71316-124">-StorageAccount</span></span>
<span data-ttu-id="71316-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="71316-125">Storage account object</span></span>

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

### <span data-ttu-id="71316-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="71316-126">-StorageAccountName</span></span>
<span data-ttu-id="71316-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="71316-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="71316-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71316-128">-Confirm</span></span>
<span data-ttu-id="71316-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="71316-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71316-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71316-130">-WhatIf</span></span>
<span data-ttu-id="71316-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71316-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71316-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="71316-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71316-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71316-133">CommonParameters</span></span>
<span data-ttu-id="71316-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71316-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71316-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71316-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71316-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71316-136">INPUTS</span></span>

### <span data-ttu-id="71316-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71316-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="71316-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="71316-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="71316-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="71316-139">OUTPUTS</span></span>

### <span data-ttu-id="71316-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71316-140">System.Boolean</span></span>

## <span data-ttu-id="71316-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="71316-141">NOTES</span></span>

## <span data-ttu-id="71316-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71316-142">RELATED LINKS</span></span>
