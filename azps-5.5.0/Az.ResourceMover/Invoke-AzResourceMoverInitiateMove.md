---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220596"
---
# <span data-ttu-id="ffb6c-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="ffb6c-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="ffb6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffb6c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb6c-103">Перемещает набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ffb6c-104">Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource moveState сделает переход на CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ffb6c-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ffb6c-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffb6c-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ffb6c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffb6c-107">DESCRIPTION</span></span>
<span data-ttu-id="ffb6c-108">Перемещает набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ffb6c-109">Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource MoveState сделает переход на CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ffb6c-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ffb6c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffb6c-111">EXAMPLES</span></span>

### <span data-ttu-id="ffb6c-112">Пример 1. Прежде чем инициировать перемещение ресурсов, проверьте инициировать их проверку.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
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

<span data-ttu-id="ffb6c-113">Прежде чем инициировать перемещение ресурсов, проверьте необходимые проверки.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="ffb6c-114">Пример 2. Инициировать перемещение для набора ресурсов в коллекции Move, используя в качестве входных данных "Имя MoveResource"</span><span class="sxs-lookup"><span data-stu-id="ffb6c-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="ffb6c-115">Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="ffb6c-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="ffb6c-116">Пример 3. Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="ffb6c-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="ffb6c-117">Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="ffb6c-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="ffb6c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffb6c-118">PARAMETERS</span></span>

### <span data-ttu-id="ffb6c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffb6c-119">-AsJob</span></span>
<span data-ttu-id="ffb6c-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ffb6c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ffb6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffb6c-121">-DefaultProfile</span></span>
<span data-ttu-id="ffb6c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffb6c-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ffb6c-123">-MoveCollectionName</span></span>
<span data-ttu-id="ffb6c-124">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ffb6c-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ffb6c-125">-MoveResource</span></span>
<span data-ttu-id="ffb6c-126">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если только тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ffb6c-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ffb6c-127">-MoveResourceInputType</span></span>
<span data-ttu-id="ffb6c-128">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ffb6c-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ffb6c-129">-NoWait</span></span>
<span data-ttu-id="ffb6c-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ffb6c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ffb6c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffb6c-131">-ResourceGroupName</span></span>
<span data-ttu-id="ffb6c-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ffb6c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ffb6c-133">-SubscriptionId</span></span>
<span data-ttu-id="ffb6c-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="ffb6c-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ffb6c-135">-ValidateOnly</span></span>
<span data-ttu-id="ffb6c-136">Возвращает или задает значение, указывающее, требуется ли только предварительный запуск операции.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ffb6c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffb6c-137">-Confirm</span></span>
<span data-ttu-id="ffb6c-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffb6c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffb6c-139">-WhatIf</span></span>
<span data-ttu-id="ffb6c-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffb6c-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffb6c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb6c-142">CommonParameters</span></span>
<span data-ttu-id="ffb6c-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffb6c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb6c-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffb6c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb6c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffb6c-145">INPUTS</span></span>

## <span data-ttu-id="ffb6c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffb6c-146">OUTPUTS</span></span>

### <span data-ttu-id="ffb6c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ffb6c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="ffb6c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffb6c-148">NOTES</span></span>

<span data-ttu-id="ffb6c-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ffb6c-149">ALIASES</span></span>

## <span data-ttu-id="ffb6c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffb6c-150">RELATED LINKS</span></span>

