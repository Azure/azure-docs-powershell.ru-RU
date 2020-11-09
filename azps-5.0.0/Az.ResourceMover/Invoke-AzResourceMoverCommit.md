---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317663"
---
# <span data-ttu-id="a05c2-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="a05c2-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="a05c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a05c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a05c2-103">Фиксирует набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="a05c2-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="a05c2-104">Операция Commit инициируется для moveResources в moveState "CommitPending" или "CommitFailed", после успешного завершения которого moveResource moveState выполняет переход на зафиксированный.</span><span class="sxs-lookup"><span data-stu-id="a05c2-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="a05c2-105">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a05c2-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="a05c2-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a05c2-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a05c2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a05c2-107">DESCRIPTION</span></span>
<span data-ttu-id="a05c2-108">Фиксирует набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="a05c2-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="a05c2-109">Операция Commit инициируется для moveResources в moveState "CommitPending" или "CommitFailed", после успешного завершения которого moveResource moveState выполняет переход на зафиксированный.</span><span class="sxs-lookup"><span data-stu-id="a05c2-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="a05c2-110">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a05c2-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="a05c2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a05c2-111">EXAMPLES</span></span>

### <span data-ttu-id="a05c2-112">Пример 1: Проверка Dependecies перед фиксацией ресурсов</span><span class="sxs-lookup"><span data-stu-id="a05c2-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="a05c2-113">Проверка Dependecies перед фиксацией ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a05c2-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="a05c2-114">Пример 2. Зафиксируйте набор ресурсов в коллекции Move с помощью "MoveResource Name" в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a05c2-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="a05c2-115">Зафиксируйте набор ресурсов в коллекции Move с помощью "MoveResource Name" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="a05c2-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="a05c2-116">Пример 3. Зафиксируйте набор ресурсов в коллекции Move с помощью "SourceARMID" в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="a05c2-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="a05c2-117">Фиксация набора ресурсов в коллекции Move с использованием "SourceARMID" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="a05c2-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="a05c2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a05c2-118">PARAMETERS</span></span>

### <span data-ttu-id="a05c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a05c2-119">-AsJob</span></span>
<span data-ttu-id="a05c2-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a05c2-120">Run the command as a job</span></span>

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

### <span data-ttu-id="a05c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05c2-121">-DefaultProfile</span></span>
<span data-ttu-id="a05c2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a05c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05c2-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="a05c2-123">-MoveCollectionName</span></span>
<span data-ttu-id="a05c2-124">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="a05c2-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="a05c2-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="a05c2-125">-MoveResource</span></span>
<span data-ttu-id="a05c2-126">Возвращает или задает список идентификаторов ресурсов по умолчанию, который принимает идентификатор ресурса Move, если только тип ввода не переключается с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="a05c2-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="a05c2-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="a05c2-127">-MoveResourceInputType</span></span>
<span data-ttu-id="a05c2-128">Определяет тип ввода ресурсов перемещения.</span><span class="sxs-lookup"><span data-stu-id="a05c2-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="a05c2-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="a05c2-129">-NoWait</span></span>
<span data-ttu-id="a05c2-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a05c2-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a05c2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05c2-131">-ResourceGroupName</span></span>
<span data-ttu-id="a05c2-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a05c2-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a05c2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a05c2-133">-SubscriptionId</span></span>
<span data-ttu-id="a05c2-134">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="a05c2-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="a05c2-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="a05c2-135">-ValidateOnly</span></span>
<span data-ttu-id="a05c2-136">Возвращает или задает значение, показывающее, требуется ли операции запуск только предварительных требований.</span><span class="sxs-lookup"><span data-stu-id="a05c2-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="a05c2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a05c2-137">-Confirm</span></span>
<span data-ttu-id="a05c2-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a05c2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05c2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05c2-139">-WhatIf</span></span>
<span data-ttu-id="a05c2-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a05c2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05c2-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a05c2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05c2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05c2-142">CommonParameters</span></span>
<span data-ttu-id="a05c2-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a05c2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05c2-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a05c2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05c2-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a05c2-145">INPUTS</span></span>

## <span data-ttu-id="a05c2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a05c2-146">OUTPUTS</span></span>

### <span data-ttu-id="a05c2-147">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a05c2-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="a05c2-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="a05c2-148">NOTES</span></span>

<span data-ttu-id="a05c2-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a05c2-149">ALIASES</span></span>

## <span data-ttu-id="a05c2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a05c2-150">RELATED LINKS</span></span>

