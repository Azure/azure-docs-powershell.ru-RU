---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999939"
---
# <span data-ttu-id="ac6d0-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="ac6d0-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="ac6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6d0-103">Инициирует подготовку к набору ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="ac6d0-104">Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="ac6d0-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ac6d0-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac6d0-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac6d0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac6d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ac6d0-108">Инициирует подготовку к набору ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="ac6d0-109">Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="ac6d0-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ac6d0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac6d0-111">EXAMPLES</span></span>

### <span data-ttu-id="ac6d0-112">Пример 1. Проверка зависимовлений перед подготовкой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="ac6d0-113">Получите необходимые зависимые ресурсы, которые также должны быть подготовлены.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="ac6d0-114">Прежде чем приготовить ресурсы, проверьте необходимые проверки.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="ac6d0-115">Получите необходимые зависимые ресурсы, которые также должны быть подготовлены.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="ac6d0-116">Пример 2. Инициировать подготовку к набору ресурсов в коллекции перемещения, используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="ac6d0-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="ac6d0-117">Инициировать подготовку к набору ресурсов в коллекции перемещения, используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="ac6d0-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="ac6d0-118">Пример 3. Инициировать подготовку к набору ресурсов в коллекции "Перемещение" с помощью "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="ac6d0-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="ac6d0-119">Инициировать подготовку к набору ресурсов в коллекции "Перемещение" с помощью "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="ac6d0-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="ac6d0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac6d0-120">PARAMETERS</span></span>

### <span data-ttu-id="ac6d0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac6d0-121">-AsJob</span></span>
<span data-ttu-id="ac6d0-122">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ac6d0-122">Run the command as a job</span></span>

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

### <span data-ttu-id="ac6d0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6d0-123">-DefaultProfile</span></span>
<span data-ttu-id="ac6d0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac6d0-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ac6d0-125">-MoveCollectionName</span></span>
<span data-ttu-id="ac6d0-126">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ac6d0-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ac6d0-127">-MoveResource</span></span>
<span data-ttu-id="ac6d0-128">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ac6d0-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ac6d0-129">-MoveResourceInputType</span></span>
<span data-ttu-id="ac6d0-130">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-130">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ac6d0-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ac6d0-131">-NoWait</span></span>
<span data-ttu-id="ac6d0-132">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ac6d0-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac6d0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6d0-133">-ResourceGroupName</span></span>
<span data-ttu-id="ac6d0-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ac6d0-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac6d0-135">-SubscriptionId</span></span>
<span data-ttu-id="ac6d0-136">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="ac6d0-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ac6d0-137">-ValidateOnly</span></span>
<span data-ttu-id="ac6d0-138">Возвращает или задает значение, указывающее, требуется ли только предварительный запуск операции.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ac6d0-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac6d0-139">-Confirm</span></span>
<span data-ttu-id="ac6d0-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac6d0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac6d0-141">-WhatIf</span></span>
<span data-ttu-id="ac6d0-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac6d0-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac6d0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6d0-144">CommonParameters</span></span>
<span data-ttu-id="ac6d0-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6d0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6d0-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac6d0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6d0-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac6d0-147">INPUTS</span></span>

## <span data-ttu-id="ac6d0-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac6d0-148">OUTPUTS</span></span>

### <span data-ttu-id="ac6d0-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ac6d0-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="ac6d0-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac6d0-150">NOTES</span></span>

<span data-ttu-id="ac6d0-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ac6d0-151">ALIASES</span></span>

## <span data-ttu-id="ac6d0-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac6d0-152">RELATED LINKS</span></span>

