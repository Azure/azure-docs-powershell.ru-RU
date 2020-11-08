---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247546"
---
# <span data-ttu-id="32b6c-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="32b6c-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="32b6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="32b6c-103">Вычисляет, обрабатывает и проверяет зависимости moveResources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="32b6c-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="32b6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32b6c-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="32b6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="32b6c-106">Вычисляет, обрабатывает и проверяет зависимости moveResources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="32b6c-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="32b6c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="32b6c-108">Пример 1: computes, разрешает и проверяют зависимости moveresources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="32b6c-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
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

<span data-ttu-id="32b6c-109">Вычисляет, обрабатывает и проверяет зависимости moveresources в коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="32b6c-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="32b6c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="32b6c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32b6c-111">-AsJob</span></span>
<span data-ttu-id="32b6c-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="32b6c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="32b6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b6c-113">-DefaultProfile</span></span>
<span data-ttu-id="32b6c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32b6c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b6c-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="32b6c-115">-MoveCollectionName</span></span>
<span data-ttu-id="32b6c-116">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="32b6c-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="32b6c-117">-Wait</span><span class="sxs-lookup"><span data-stu-id="32b6c-117">-NoWait</span></span>
<span data-ttu-id="32b6c-118">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="32b6c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="32b6c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b6c-119">-ResourceGroupName</span></span>
<span data-ttu-id="32b6c-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32b6c-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="32b6c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32b6c-121">-SubscriptionId</span></span>
<span data-ttu-id="32b6c-122">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="32b6c-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="32b6c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32b6c-123">-Confirm</span></span>
<span data-ttu-id="32b6c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32b6c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b6c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b6c-125">-WhatIf</span></span>
<span data-ttu-id="32b6c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32b6c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b6c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32b6c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b6c-128">CommonParameters</span></span>
<span data-ttu-id="32b6c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32b6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b6c-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32b6c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b6c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32b6c-131">INPUTS</span></span>

## <span data-ttu-id="32b6c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32b6c-132">OUTPUTS</span></span>

### <span data-ttu-id="32b6c-133">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="32b6c-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="32b6c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="32b6c-134">NOTES</span></span>

<span data-ttu-id="32b6c-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="32b6c-135">ALIASES</span></span>

## <span data-ttu-id="32b6c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32b6c-136">RELATED LINKS</span></span>

