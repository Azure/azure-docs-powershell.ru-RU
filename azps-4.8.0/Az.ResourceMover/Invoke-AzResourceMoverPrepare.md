---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079353"
---
# <span data-ttu-id="60613-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="60613-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="60613-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60613-102">SYNOPSIS</span></span>
<span data-ttu-id="60613-103">Инициирует подготовку к набору ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="60613-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="60613-104">Операция подготовки находится на moveResources, которая находится в moveState "PreparePending" или "PrepareFailed", после успешного завершения moveResource moveState выполняет переход к MovePending.</span><span class="sxs-lookup"><span data-stu-id="60613-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="60613-105">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="60613-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="60613-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60613-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60613-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60613-107">DESCRIPTION</span></span>
<span data-ttu-id="60613-108">Инициирует подготовку к набору ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="60613-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="60613-109">Операция подготовки находится на moveResources, которая находится в moveState "PreparePending" или "PrepareFailed", после успешного завершения moveResource moveState выполняет переход к MovePending.</span><span class="sxs-lookup"><span data-stu-id="60613-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="60613-110">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="60613-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="60613-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60613-111">EXAMPLES</span></span>

### <span data-ttu-id="60613-112">Пример 1: Проверка Dependecies перед тем, как подготовиться к ресурсам</span><span class="sxs-lookup"><span data-stu-id="60613-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="60613-113">Проверьте Dependecies перед тем, как подготовиться к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="60613-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="60613-114">Пример 2: initiate подготовка для набора ресурсов в коллекции Move с помощью "MoveResource Name" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="60613-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="60613-115">Инициируйте подготовку к набору ресурсов в коллекции перемещения, используя в качестве входных данных "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="60613-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="60613-116">Пример 3: initiate подготовка для набора ресурсов в коллекции Move с помощью "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="60613-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="60613-117">Инициируйте подготовку к набору ресурсов в коллекции перемещения с помощью "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="60613-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="60613-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60613-118">PARAMETERS</span></span>

### <span data-ttu-id="60613-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60613-119">-AsJob</span></span>
<span data-ttu-id="60613-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="60613-120">Run the command as a job</span></span>

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

### <span data-ttu-id="60613-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60613-121">-DefaultProfile</span></span>
<span data-ttu-id="60613-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60613-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60613-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="60613-123">-MoveCollectionName</span></span>
<span data-ttu-id="60613-124">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="60613-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="60613-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="60613-125">-MoveResource</span></span>
<span data-ttu-id="60613-126">Возвращает или задает список идентификаторов ресурсов по умолчанию, который принимает идентификатор ресурса Move, если только тип ввода не переключается с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="60613-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60613-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="60613-127">-MoveResourceInputType</span></span>
<span data-ttu-id="60613-128">Определяет тип ввода ресурсов перемещения.</span><span class="sxs-lookup"><span data-stu-id="60613-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60613-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="60613-129">-NoWait</span></span>
<span data-ttu-id="60613-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="60613-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="60613-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60613-131">-ResourceGroupName</span></span>
<span data-ttu-id="60613-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60613-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="60613-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60613-133">-SubscriptionId</span></span>
<span data-ttu-id="60613-134">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="60613-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="60613-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="60613-135">-ValidateOnly</span></span>
<span data-ttu-id="60613-136">Возвращает или задает значение, показывающее, требуется ли операции запуск только предварительных требований.</span><span class="sxs-lookup"><span data-stu-id="60613-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="60613-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60613-137">-Confirm</span></span>
<span data-ttu-id="60613-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60613-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60613-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60613-139">-WhatIf</span></span>
<span data-ttu-id="60613-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60613-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60613-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60613-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60613-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60613-142">CommonParameters</span></span>
<span data-ttu-id="60613-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60613-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60613-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60613-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60613-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60613-145">INPUTS</span></span>

## <span data-ttu-id="60613-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60613-146">OUTPUTS</span></span>

### <span data-ttu-id="60613-147">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="60613-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="60613-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="60613-148">NOTES</span></span>

<span data-ttu-id="60613-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="60613-149">ALIASES</span></span>

## <span data-ttu-id="60613-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60613-150">RELATED LINKS</span></span>

