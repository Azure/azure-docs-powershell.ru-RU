---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505334"
---
# <span data-ttu-id="4430b-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="4430b-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="4430b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4430b-102">SYNOPSIS</span></span>
<span data-ttu-id="4430b-103">Вычисляет, устраняет и проверяет зависимости moveResources в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="4430b-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="4430b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4430b-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4430b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4430b-105">DESCRIPTION</span></span>
<span data-ttu-id="4430b-106">Вычисляет, устраняет и проверяет зависимости moveResources в коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="4430b-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="4430b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4430b-107">EXAMPLES</span></span>

### <span data-ttu-id="4430b-108">Пример 1. Вычисляет, устраняет и проверяет зависимости moveresources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="4430b-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="4430b-109">Вычисляет, устраняет и проверяет зависимости moveresources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="4430b-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="4430b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4430b-110">PARAMETERS</span></span>

### <span data-ttu-id="4430b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4430b-111">-AsJob</span></span>
<span data-ttu-id="4430b-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4430b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4430b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4430b-113">-DefaultProfile</span></span>
<span data-ttu-id="4430b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4430b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4430b-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4430b-115">-MoveCollectionName</span></span>
<span data-ttu-id="4430b-116">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="4430b-116">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4430b-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4430b-117">-NoWait</span></span>
<span data-ttu-id="4430b-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4430b-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4430b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4430b-119">-ResourceGroupName</span></span>
<span data-ttu-id="4430b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4430b-120">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4430b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4430b-121">-SubscriptionId</span></span>
<span data-ttu-id="4430b-122">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="4430b-122">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4430b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4430b-123">-Confirm</span></span>
<span data-ttu-id="4430b-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4430b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4430b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4430b-125">-WhatIf</span></span>
<span data-ttu-id="4430b-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4430b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4430b-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4430b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4430b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4430b-128">CommonParameters</span></span>
<span data-ttu-id="4430b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4430b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4430b-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4430b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4430b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4430b-131">INPUTS</span></span>

## <span data-ttu-id="4430b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4430b-132">OUTPUTS</span></span>

### <span data-ttu-id="4430b-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4430b-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="4430b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4430b-134">NOTES</span></span>

<span data-ttu-id="4430b-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4430b-135">ALIASES</span></span>

## <span data-ttu-id="4430b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4430b-136">RELATED LINKS</span></span>

