---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235964"
---
# <span data-ttu-id="ed686-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="ed686-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="ed686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed686-102">SYNOPSIS</span></span>
<span data-ttu-id="ed686-103">Включает в себя набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="ed686-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="ed686-104">При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.</span><span class="sxs-lookup"><span data-stu-id="ed686-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="ed686-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="ed686-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ed686-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed686-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed686-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed686-107">DESCRIPTION</span></span>
<span data-ttu-id="ed686-108">Включает в себя набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="ed686-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="ed686-109">При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.</span><span class="sxs-lookup"><span data-stu-id="ed686-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="ed686-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="ed686-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ed686-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed686-111">EXAMPLES</span></span>

### <span data-ttu-id="ed686-112">Пример 1. Проверка зависимовлений перед их подтверждением</span><span class="sxs-lookup"><span data-stu-id="ed686-112">Example 1: Validate the dependecies before commit of the resources</span></span>
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

<span data-ttu-id="ed686-113">Прежде чем подтверждать, что ресурсы подтверждены, проверьте необходимые проверки.</span><span class="sxs-lookup"><span data-stu-id="ed686-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="ed686-114">Пример 2. Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "Имя MoveResource"</span><span class="sxs-lookup"><span data-stu-id="ed686-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="ed686-115">Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "Имя MoveResource"</span><span class="sxs-lookup"><span data-stu-id="ed686-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="ed686-116">Пример 3. Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="ed686-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="ed686-117">Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="ed686-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="ed686-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed686-118">PARAMETERS</span></span>

### <span data-ttu-id="ed686-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed686-119">-AsJob</span></span>
<span data-ttu-id="ed686-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ed686-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ed686-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed686-121">-DefaultProfile</span></span>
<span data-ttu-id="ed686-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed686-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed686-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ed686-123">-MoveCollectionName</span></span>
<span data-ttu-id="ed686-124">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="ed686-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ed686-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ed686-125">-MoveResource</span></span>
<span data-ttu-id="ed686-126">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если только тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="ed686-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ed686-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ed686-127">-MoveResourceInputType</span></span>
<span data-ttu-id="ed686-128">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="ed686-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ed686-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed686-129">-NoWait</span></span>
<span data-ttu-id="ed686-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ed686-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed686-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed686-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed686-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed686-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ed686-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed686-133">-SubscriptionId</span></span>
<span data-ttu-id="ed686-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="ed686-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="ed686-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ed686-135">-ValidateOnly</span></span>
<span data-ttu-id="ed686-136">Возвращает или задает значение, указывающее, требуется ли только предварительный запуск операции.</span><span class="sxs-lookup"><span data-stu-id="ed686-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ed686-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed686-137">-Confirm</span></span>
<span data-ttu-id="ed686-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed686-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed686-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed686-139">-WhatIf</span></span>
<span data-ttu-id="ed686-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed686-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed686-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed686-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed686-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed686-142">CommonParameters</span></span>
<span data-ttu-id="ed686-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed686-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed686-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed686-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed686-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed686-145">INPUTS</span></span>

## <span data-ttu-id="ed686-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed686-146">OUTPUTS</span></span>

### <span data-ttu-id="ed686-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ed686-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="ed686-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed686-148">NOTES</span></span>

<span data-ttu-id="ed686-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ed686-149">ALIASES</span></span>

## <span data-ttu-id="ed686-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed686-150">RELATED LINKS</span></span>

