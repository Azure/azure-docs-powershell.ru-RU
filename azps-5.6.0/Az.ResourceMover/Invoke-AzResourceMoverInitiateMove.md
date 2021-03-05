---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999944"
---
# <span data-ttu-id="0228c-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="0228c-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="0228c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0228c-102">SYNOPSIS</span></span>
<span data-ttu-id="0228c-103">Перемещает набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="0228c-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="0228c-104">Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource moveState сделает переход на CommitPending.</span><span class="sxs-lookup"><span data-stu-id="0228c-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="0228c-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="0228c-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="0228c-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0228c-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0228c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0228c-107">DESCRIPTION</span></span>
<span data-ttu-id="0228c-108">Перемещает набор ресурсов, включенных в запрос.</span><span class="sxs-lookup"><span data-stu-id="0228c-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="0228c-109">Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource moveState сделает переход на CommitPending.</span><span class="sxs-lookup"><span data-stu-id="0228c-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="0228c-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="0228c-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="0228c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0228c-111">EXAMPLES</span></span>

### <span data-ttu-id="0228c-112">Пример 1. Прежде чем инициировать перемещение ресурсов, проверьте инициировать их проверку.</span><span class="sxs-lookup"><span data-stu-id="0228c-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

<span data-ttu-id="0228c-113">Прежде чем инициировать перемещение ресурсов, проверьте необходимые проверки.</span><span class="sxs-lookup"><span data-stu-id="0228c-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="0228c-114">Пример 2. Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="0228c-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

<span data-ttu-id="0228c-115">Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "Имя MoveResource".</span><span class="sxs-lookup"><span data-stu-id="0228c-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="0228c-116">Пример 3. Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="0228c-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

<span data-ttu-id="0228c-117">Инициировать перемещение для набора ресурсов в коллекции "Перемещение", используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="0228c-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="0228c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0228c-118">PARAMETERS</span></span>

### <span data-ttu-id="0228c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0228c-119">-AsJob</span></span>
<span data-ttu-id="0228c-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0228c-120">Run the command as a job</span></span>

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

### <span data-ttu-id="0228c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0228c-121">-DefaultProfile</span></span>
<span data-ttu-id="0228c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0228c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0228c-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="0228c-123">-MoveCollectionName</span></span>
<span data-ttu-id="0228c-124">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="0228c-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="0228c-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="0228c-125">-MoveResource</span></span>
<span data-ttu-id="0228c-126">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="0228c-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="0228c-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="0228c-127">-MoveResourceInputType</span></span>
<span data-ttu-id="0228c-128">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="0228c-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="0228c-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0228c-129">-NoWait</span></span>
<span data-ttu-id="0228c-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0228c-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0228c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0228c-131">-ResourceGroupName</span></span>
<span data-ttu-id="0228c-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0228c-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="0228c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0228c-133">-SubscriptionId</span></span>
<span data-ttu-id="0228c-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="0228c-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="0228c-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="0228c-135">-ValidateOnly</span></span>
<span data-ttu-id="0228c-136">Возвращает или задает значение, указывающее, требуется ли только предварительный запуск операции.</span><span class="sxs-lookup"><span data-stu-id="0228c-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="0228c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0228c-137">-Confirm</span></span>
<span data-ttu-id="0228c-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0228c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0228c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0228c-139">-WhatIf</span></span>
<span data-ttu-id="0228c-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0228c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0228c-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0228c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0228c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0228c-142">CommonParameters</span></span>
<span data-ttu-id="0228c-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0228c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0228c-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0228c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0228c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0228c-145">INPUTS</span></span>

## <span data-ttu-id="0228c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0228c-146">OUTPUTS</span></span>

### <span data-ttu-id="0228c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="0228c-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="0228c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0228c-148">NOTES</span></span>

<span data-ttu-id="0228c-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0228c-149">ALIASES</span></span>

## <span data-ttu-id="0228c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0228c-150">RELATED LINKS</span></span>

