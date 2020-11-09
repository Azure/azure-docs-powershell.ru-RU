---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317657"
---
# <span data-ttu-id="a1efd-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="a1efd-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="a1efd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1efd-102">SYNOPSIS</span></span>
<span data-ttu-id="a1efd-103">Перемещает набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="a1efd-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="a1efd-104">Операция перемещения активируется после того, как moveResources находится в moveState "MovePending" или "MoveFailed", после успешного завершения moveResource moveState выполняет переход к CommitPending.</span><span class="sxs-lookup"><span data-stu-id="a1efd-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="a1efd-105">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a1efd-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="a1efd-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1efd-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1efd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1efd-107">DESCRIPTION</span></span>
<span data-ttu-id="a1efd-108">Перемещает набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="a1efd-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="a1efd-109">Операция перемещения активируется после того, как moveResources находится в moveState "MovePending" или "MoveFailed", после успешного завершения moveResource moveState выполняет переход к CommitPending.</span><span class="sxs-lookup"><span data-stu-id="a1efd-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="a1efd-110">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a1efd-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="a1efd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1efd-111">EXAMPLES</span></span>

### <span data-ttu-id="a1efd-112">Пример 1: Проверка Dependecies перед запуском Move для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1efd-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="a1efd-113">Проверка Dependecies перед инициированием перемещения для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1efd-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="a1efd-114">Пример 2: initiate Move для набора ресурсов в коллекции Move с использованием "MoveResource Name" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="a1efd-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="a1efd-115">Инициация перемещения для набора ресурсов в коллекции Move с помощью "MoveResource Name" в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a1efd-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="a1efd-116">Пример 3: Начало перемещения для набора ресурсов в коллекции Move с помощью "SourceARMID" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="a1efd-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="a1efd-117">Инициация перемещения для набора ресурсов в коллекции Move с использованием "SourceARMID" в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a1efd-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="a1efd-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1efd-118">PARAMETERS</span></span>

### <span data-ttu-id="a1efd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1efd-119">-AsJob</span></span>
<span data-ttu-id="a1efd-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a1efd-120">Run the command as a job</span></span>

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

### <span data-ttu-id="a1efd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1efd-121">-DefaultProfile</span></span>
<span data-ttu-id="a1efd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1efd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1efd-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="a1efd-123">-MoveCollectionName</span></span>
<span data-ttu-id="a1efd-124">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="a1efd-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="a1efd-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="a1efd-125">-MoveResource</span></span>
<span data-ttu-id="a1efd-126">Возвращает или задает список идентификаторов ресурсов по умолчанию, который принимает идентификатор ресурса Move, если только тип ввода не переключается с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="a1efd-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="a1efd-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="a1efd-127">-MoveResourceInputType</span></span>
<span data-ttu-id="a1efd-128">Определяет тип ввода ресурсов перемещения.</span><span class="sxs-lookup"><span data-stu-id="a1efd-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="a1efd-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="a1efd-129">-NoWait</span></span>
<span data-ttu-id="a1efd-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a1efd-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a1efd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1efd-131">-ResourceGroupName</span></span>
<span data-ttu-id="a1efd-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1efd-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a1efd-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1efd-133">-SubscriptionId</span></span>
<span data-ttu-id="a1efd-134">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a1efd-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="a1efd-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="a1efd-135">-ValidateOnly</span></span>
<span data-ttu-id="a1efd-136">Возвращает или задает значение, показывающее, требуется ли операции запуск только предварительных требований.</span><span class="sxs-lookup"><span data-stu-id="a1efd-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="a1efd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1efd-137">-Confirm</span></span>
<span data-ttu-id="a1efd-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1efd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1efd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1efd-139">-WhatIf</span></span>
<span data-ttu-id="a1efd-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1efd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1efd-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1efd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1efd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1efd-142">CommonParameters</span></span>
<span data-ttu-id="a1efd-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1efd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1efd-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1efd-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1efd-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1efd-145">INPUTS</span></span>

## <span data-ttu-id="a1efd-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1efd-146">OUTPUTS</span></span>

### <span data-ttu-id="a1efd-147">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a1efd-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="a1efd-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1efd-148">NOTES</span></span>

<span data-ttu-id="a1efd-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a1efd-149">ALIASES</span></span>

## <span data-ttu-id="a1efd-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1efd-150">RELATED LINKS</span></span>

