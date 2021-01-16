---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506713"
---
# <span data-ttu-id="f1e2f-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="f1e2f-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="f1e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e2f-103">Удаляет набор ресурсов, включенных в тело запроса.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="f1e2f-104">При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="f1e2f-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="f1e2f-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1e2f-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1e2f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="f1e2f-108">Удаляет набор ресурсов, включенных в тело запроса.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="f1e2f-109">При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="f1e2f-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="f1e2f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1e2f-111">EXAMPLES</span></span>

### <span data-ttu-id="f1e2f-112">Пример 1. Проверка зависимок перед удалением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="f1e2f-113">Проверьте зависимость перед удалением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="f1e2f-114">Пример 2. Удаляет перемещение ресурсов с использованием имени MoveResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="f1e2f-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="f1e2f-115">Отклоняет перемещение ресурсов с использованием в качестве входных данных MoveResource Name.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="f1e2f-116">Пример 3. Удаляет перемещение ресурсов, используя в качестве входных данных "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="f1e2f-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="f1e2f-117">Удаляет перемещение ресурсов, используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="f1e2f-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="f1e2f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1e2f-118">PARAMETERS</span></span>

### <span data-ttu-id="f1e2f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1e2f-119">-AsJob</span></span>
<span data-ttu-id="f1e2f-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="f1e2f-120">Run the command as a job</span></span>

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

### <span data-ttu-id="f1e2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e2f-121">-DefaultProfile</span></span>
<span data-ttu-id="f1e2f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1e2f-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="f1e2f-123">-MoveResource</span></span>
<span data-ttu-id="f1e2f-124">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="f1e2f-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="f1e2f-125">-MoveResourceInputType</span></span>
<span data-ttu-id="f1e2f-126">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="f1e2f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f1e2f-127">-Name</span></span>
<span data-ttu-id="f1e2f-128">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-128">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e2f-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1e2f-129">-NoWait</span></span>
<span data-ttu-id="f1e2f-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="f1e2f-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f1e2f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e2f-131">-ResourceGroupName</span></span>
<span data-ttu-id="f1e2f-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f1e2f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1e2f-133">-SubscriptionId</span></span>
<span data-ttu-id="f1e2f-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="f1e2f-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="f1e2f-135">-ValidateOnly</span></span>
<span data-ttu-id="f1e2f-136">Возвращает или задает значение, указывающее, требуется ли только предварительный запуск операции.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="f1e2f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1e2f-137">-Confirm</span></span>
<span data-ttu-id="f1e2f-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e2f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e2f-139">-WhatIf</span></span>
<span data-ttu-id="f1e2f-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e2f-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e2f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e2f-142">CommonParameters</span></span>
<span data-ttu-id="f1e2f-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e2f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e2f-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1e2f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e2f-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1e2f-145">INPUTS</span></span>

## <span data-ttu-id="f1e2f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1e2f-146">OUTPUTS</span></span>

### <span data-ttu-id="f1e2f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f1e2f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="f1e2f-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1e2f-148">NOTES</span></span>

<span data-ttu-id="f1e2f-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f1e2f-149">ALIASES</span></span>

## <span data-ttu-id="f1e2f-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1e2f-150">RELATED LINKS</span></span>

