---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406095"
---
# <span data-ttu-id="f364b-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="f364b-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="f364b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f364b-102">SYNOPSIS</span></span>
<span data-ttu-id="f364b-103">Инициирует подготовку к набору ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="f364b-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="f364b-104">Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.</span><span class="sxs-lookup"><span data-stu-id="f364b-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="f364b-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="f364b-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="f364b-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f364b-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f364b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f364b-107">DESCRIPTION</span></span>
<span data-ttu-id="f364b-108">Инициирует подготовку к набору ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="f364b-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="f364b-109">Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.</span><span class="sxs-lookup"><span data-stu-id="f364b-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="f364b-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="f364b-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="f364b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f364b-111">EXAMPLES</span></span>

### <span data-ttu-id="f364b-112">Пример 1. Проверка зависимовлений перед подготовкой к ресурсам</span><span class="sxs-lookup"><span data-stu-id="f364b-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
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

<span data-ttu-id="f364b-113">Прежде чем приготовьтесь к ресурсам, проверьте необходимые возможности.</span><span class="sxs-lookup"><span data-stu-id="f364b-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="f364b-114">Пример 2. Инициировать подготовку к набору ресурсов в коллекции перемещения с использованием имени MoveResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="f364b-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="f364b-115">Инициировать подготовку к набору ресурсов в коллекции перемещения, используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="f364b-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="f364b-116">Пример 3. Инициировать подготовку к набору ресурсов в коллекции "Перемещение" с помощью "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="f364b-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
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

<span data-ttu-id="f364b-117">Инициировать подготовку к набору ресурсов в коллекции "Перемещение" с помощью "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="f364b-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="f364b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f364b-118">PARAMETERS</span></span>

### <span data-ttu-id="f364b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f364b-119">-AsJob</span></span>
<span data-ttu-id="f364b-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f364b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="f364b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f364b-121">-DefaultProfile</span></span>
<span data-ttu-id="f364b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f364b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f364b-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="f364b-123">-MoveCollectionName</span></span>
<span data-ttu-id="f364b-124">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="f364b-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="f364b-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="f364b-125">-MoveResource</span></span>
<span data-ttu-id="f364b-126">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="f364b-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="f364b-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="f364b-127">-MoveResourceInputType</span></span>
<span data-ttu-id="f364b-128">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="f364b-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="f364b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f364b-129">-NoWait</span></span>
<span data-ttu-id="f364b-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f364b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f364b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f364b-131">-ResourceGroupName</span></span>
<span data-ttu-id="f364b-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f364b-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f364b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f364b-133">-SubscriptionId</span></span>
<span data-ttu-id="f364b-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="f364b-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="f364b-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="f364b-135">-ValidateOnly</span></span>
<span data-ttu-id="f364b-136">Возвращает или задает значение, указывающее, требуется ли только предварительный запуск операции.</span><span class="sxs-lookup"><span data-stu-id="f364b-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="f364b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f364b-137">-Confirm</span></span>
<span data-ttu-id="f364b-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f364b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f364b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f364b-139">-WhatIf</span></span>
<span data-ttu-id="f364b-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f364b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f364b-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f364b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f364b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f364b-142">CommonParameters</span></span>
<span data-ttu-id="f364b-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f364b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f364b-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f364b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f364b-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f364b-145">INPUTS</span></span>

## <span data-ttu-id="f364b-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f364b-146">OUTPUTS</span></span>

### <span data-ttu-id="f364b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f364b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="f364b-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f364b-148">NOTES</span></span>

<span data-ttu-id="f364b-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f364b-149">ALIASES</span></span>

## <span data-ttu-id="f364b-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f364b-150">RELATED LINKS</span></span>

