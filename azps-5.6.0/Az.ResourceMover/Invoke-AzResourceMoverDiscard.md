---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: 5e54501e6337943561489a80adf4e8789a55a394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999955"
---
# <span data-ttu-id="003e6-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="003e6-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="003e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="003e6-102">SYNOPSIS</span></span>
<span data-ttu-id="003e6-103">Удаляет набор ресурсов, включенных в тело запроса.</span><span class="sxs-lookup"><span data-stu-id="003e6-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="003e6-104">При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.</span><span class="sxs-lookup"><span data-stu-id="003e6-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="003e6-105">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="003e6-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="003e6-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="003e6-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="003e6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="003e6-107">DESCRIPTION</span></span>
<span data-ttu-id="003e6-108">Удаляет набор ресурсов, включенных в тело запроса.</span><span class="sxs-lookup"><span data-stu-id="003e6-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="003e6-109">При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.</span><span class="sxs-lookup"><span data-stu-id="003e6-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="003e6-110">Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.</span><span class="sxs-lookup"><span data-stu-id="003e6-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="003e6-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="003e6-111">EXAMPLES</span></span>

### <span data-ttu-id="003e6-112">Пример 1. Проверка зависимок перед удалением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="003e6-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:39:48 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:39:37 PM
Status         : Succeeded

```

<span data-ttu-id="003e6-113">Проверьте зависимость перед удалением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="003e6-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="003e6-114">Пример 2. Удаляет перемещение ресурсов с использованием имени MoveResource в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="003e6-114">Example 2: Discards the move of the resources using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:56:33 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:55:21 PM
Status         : Succeeded

```

<span data-ttu-id="003e6-115">Отклоняет перемещение ресурсов, используя в качестве входных данных moveResource Name.</span><span class="sxs-lookup"><span data-stu-id="003e6-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="003e6-116">Пример 3. Удаляет перемещение ресурсов, используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="003e6-116">Example 3: Discards the move of the resources using "SourceARMID" as input.</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:01:32 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:00:00 PM
Status         : Succeeded


```

<span data-ttu-id="003e6-117">Удаляет перемещение ресурсов, используя в качестве входных данных "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="003e6-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="003e6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="003e6-118">PARAMETERS</span></span>

### <span data-ttu-id="003e6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="003e6-119">-AsJob</span></span>
<span data-ttu-id="003e6-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="003e6-120">Run the command as a job</span></span>

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

### <span data-ttu-id="003e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003e6-121">-DefaultProfile</span></span>
<span data-ttu-id="003e6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="003e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="003e6-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="003e6-123">-MoveResource</span></span>
<span data-ttu-id="003e6-124">Возвращает или задает список ИД ресурсов, по умолчанию он принимает перемещение ид ресурса, если тип ввода не был переключен с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="003e6-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="003e6-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="003e6-125">-MoveResourceInputType</span></span>
<span data-ttu-id="003e6-126">Определяет тип ввода для перемещения ресурса.</span><span class="sxs-lookup"><span data-stu-id="003e6-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="003e6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="003e6-127">-Name</span></span>
<span data-ttu-id="003e6-128">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="003e6-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="003e6-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="003e6-129">-NoWait</span></span>
<span data-ttu-id="003e6-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="003e6-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="003e6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003e6-131">-ResourceGroupName</span></span>
<span data-ttu-id="003e6-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="003e6-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="003e6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="003e6-133">-SubscriptionId</span></span>
<span data-ttu-id="003e6-134">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="003e6-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="003e6-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="003e6-135">-ValidateOnly</span></span>
<span data-ttu-id="003e6-136">Возвращает или задает значение, указывающее, требуется ли выполнить только предварительные требования.</span><span class="sxs-lookup"><span data-stu-id="003e6-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="003e6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="003e6-137">-Confirm</span></span>
<span data-ttu-id="003e6-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003e6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="003e6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003e6-139">-WhatIf</span></span>
<span data-ttu-id="003e6-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003e6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003e6-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="003e6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="003e6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003e6-142">CommonParameters</span></span>
<span data-ttu-id="003e6-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003e6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003e6-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="003e6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003e6-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="003e6-145">INPUTS</span></span>

## <span data-ttu-id="003e6-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="003e6-146">OUTPUTS</span></span>

### <span data-ttu-id="003e6-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="003e6-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="003e6-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="003e6-148">NOTES</span></span>

<span data-ttu-id="003e6-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="003e6-149">ALIASES</span></span>

## <span data-ttu-id="003e6-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="003e6-150">RELATED LINKS</span></span>

