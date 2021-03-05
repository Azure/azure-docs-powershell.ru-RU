---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999976"
---
# <span data-ttu-id="4e4be-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="4e4be-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="4e4be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e4be-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4be-103">Включает в себя набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="4e4be-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="4e4be-104">При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.</span><span class="sxs-lookup"><span data-stu-id="4e4be-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="4e4be-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="4e4be-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="4e4be-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e4be-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e4be-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e4be-107">DESCRIPTION</span></span>
<span data-ttu-id="4e4be-108">Включает в себя набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="4e4be-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="4e4be-109">При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.</span><span class="sxs-lookup"><span data-stu-id="4e4be-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="4e4be-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="4e4be-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="4e4be-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e4be-111">EXAMPLES</span></span>

### <span data-ttu-id="4e4be-112">Пример 1. Проверка зависимофиксов перед их подтверждением.</span><span class="sxs-lookup"><span data-stu-id="4e4be-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="4e4be-113">Прежде чем подтверждать, что ресурсы подтверждены, проверьте необходимые проверки.</span><span class="sxs-lookup"><span data-stu-id="4e4be-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="4e4be-114">Пример 2. Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="4e4be-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="4e4be-115">Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных moveResource Name.</span><span class="sxs-lookup"><span data-stu-id="4e4be-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="4e4be-116">Пример 3. Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="4e4be-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="4e4be-117">Зафиксировать набор ресурсов в коллекции перемещения, используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="4e4be-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="4e4be-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e4be-118">PARAMETERS</span></span>

### <span data-ttu-id="4e4be-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e4be-119">-AsJob</span></span>
<span data-ttu-id="4e4be-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4e4be-120">Run the command as a job</span></span>

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

### <span data-ttu-id="4e4be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4be-121">-DefaultProfile</span></span>
<span data-ttu-id="4e4be-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4be-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4be-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4e4be-123">-MoveCollectionName</span></span>
<span data-ttu-id="4e4be-124">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e4be-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4e4be-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="4e4be-125">-MoveResource</span></span>
<span data-ttu-id="4e4be-126">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если только тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="4e4be-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="4e4be-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="4e4be-127">-MoveResourceInputType</span></span>
<span data-ttu-id="4e4be-128">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e4be-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="4e4be-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e4be-129">-NoWait</span></span>
<span data-ttu-id="4e4be-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="4e4be-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e4be-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e4be-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e4be-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e4be-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4e4be-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e4be-133">-SubscriptionId</span></span>
<span data-ttu-id="4e4be-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="4e4be-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="4e4be-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="4e4be-135">-ValidateOnly</span></span>
<span data-ttu-id="4e4be-136">Возвращает или задает значение, указывающее, требуется ли выполнить только предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="4e4be-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="4e4be-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e4be-137">-Confirm</span></span>
<span data-ttu-id="4e4be-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4be-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4be-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4be-139">-WhatIf</span></span>
<span data-ttu-id="4e4be-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4be-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4be-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e4be-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4be-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4be-142">CommonParameters</span></span>
<span data-ttu-id="4e4be-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4be-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4be-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e4be-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4be-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e4be-145">INPUTS</span></span>

## <span data-ttu-id="4e4be-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e4be-146">OUTPUTS</span></span>

### <span data-ttu-id="4e4be-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4e4be-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="4e4be-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e4be-148">NOTES</span></span>

<span data-ttu-id="4e4be-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e4be-149">ALIASES</span></span>

## <span data-ttu-id="4e4be-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e4be-150">RELATED LINKS</span></span>

