---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232484"
---
# <span data-ttu-id="58963-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="58963-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="58963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58963-102">SYNOPSIS</span></span>
<span data-ttu-id="58963-103">Удаляет указанную политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58963-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="58963-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58963-104">SYNTAX</span></span>

### <span data-ttu-id="58963-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58963-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58963-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="58963-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58963-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="58963-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58963-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58963-108">DESCRIPTION</span></span>
<span data-ttu-id="58963-109">Для удаления указанной политики репликации объектов из учетной записи хранения удаляется cmdlet **Remove-AzStorageObjectReplicationPolicy.**</span><span class="sxs-lookup"><span data-stu-id="58963-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="58963-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58963-110">EXAMPLES</span></span>

### <span data-ttu-id="58963-111">Пример 1. Удаление политики репликации объектов с определенным ид политики из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58963-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="58963-112">Эта команда удаляет из учетной записи хранения политику репликации объектов с определенным ид политики.</span><span class="sxs-lookup"><span data-stu-id="58963-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="58963-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58963-113">PARAMETERS</span></span>

### <span data-ttu-id="58963-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58963-114">-DefaultProfile</span></span>
<span data-ttu-id="58963-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58963-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58963-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58963-116">-InputObject</span></span>
<span data-ttu-id="58963-117">Объект политики репликации объектов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="58963-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="58963-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58963-118">-PassThru</span></span>
<span data-ttu-id="58963-119">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="58963-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="58963-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="58963-120">-PolicyId</span></span>
<span data-ttu-id="58963-121">ИД политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="58963-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="58963-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58963-122">-ResourceGroupName</span></span>
<span data-ttu-id="58963-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58963-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="58963-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="58963-124">-StorageAccount</span></span>
<span data-ttu-id="58963-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="58963-125">Storage account object</span></span>

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

### <span data-ttu-id="58963-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="58963-126">-StorageAccountName</span></span>
<span data-ttu-id="58963-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="58963-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="58963-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58963-128">-Confirm</span></span>
<span data-ttu-id="58963-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58963-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58963-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58963-130">-WhatIf</span></span>
<span data-ttu-id="58963-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58963-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58963-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="58963-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58963-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58963-133">CommonParameters</span></span>
<span data-ttu-id="58963-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58963-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58963-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58963-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58963-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58963-136">INPUTS</span></span>

### <span data-ttu-id="58963-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58963-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="58963-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="58963-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="58963-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58963-139">OUTPUTS</span></span>

### <span data-ttu-id="58963-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58963-140">System.Boolean</span></span>

## <span data-ttu-id="58963-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58963-141">NOTES</span></span>

## <span data-ttu-id="58963-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58963-142">RELATED LINKS</span></span>
