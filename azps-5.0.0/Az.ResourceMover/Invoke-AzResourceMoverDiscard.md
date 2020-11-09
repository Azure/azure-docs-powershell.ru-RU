---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317660"
---
# <span data-ttu-id="c22f5-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="c22f5-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="c22f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c22f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c22f5-103">Удаляет набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="c22f5-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="c22f5-104">Операция отмены вызывается для moveResources в moveState "CommitPending" или "DiscardFailed", после успешного завершения которого moveResource moveState выполняет переход к MovePending.</span><span class="sxs-lookup"><span data-stu-id="c22f5-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="c22f5-105">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="c22f5-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="c22f5-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c22f5-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c22f5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c22f5-107">DESCRIPTION</span></span>
<span data-ttu-id="c22f5-108">Удаляет набор ресурсов, включенных в текст запроса.</span><span class="sxs-lookup"><span data-stu-id="c22f5-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="c22f5-109">Операция отмены вызывается для moveResources в moveState "CommitPending" или "DiscardFailed", после успешного завершения которого moveResource moveState выполняет переход к MovePending.</span><span class="sxs-lookup"><span data-stu-id="c22f5-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="c22f5-110">Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="c22f5-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="c22f5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c22f5-111">EXAMPLES</span></span>

### <span data-ttu-id="c22f5-112">Пример 1: Проверка Dependecies перед удалением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c22f5-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
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

<span data-ttu-id="c22f5-113">Проверка Dependecies перед удалением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c22f5-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="c22f5-114">Пример 2: отмена перемещения ресурсов с помощью "MoveResource Name" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="c22f5-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="c22f5-115">Отменяет перемещение ресурсов, используя в качестве входных данных "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="c22f5-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="c22f5-116">Пример 3: отмена перемещения ресурсов с помощью "SourceARMID" в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="c22f5-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
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

<span data-ttu-id="c22f5-117">Отменяет перемещение ресурсов, используя "SourceARMID" в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="c22f5-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="c22f5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c22f5-118">PARAMETERS</span></span>

### <span data-ttu-id="c22f5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c22f5-119">-AsJob</span></span>
<span data-ttu-id="c22f5-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c22f5-120">Run the command as a job</span></span>

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

### <span data-ttu-id="c22f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22f5-121">-DefaultProfile</span></span>
<span data-ttu-id="c22f5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c22f5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c22f5-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="c22f5-123">-MoveResource</span></span>
<span data-ttu-id="c22f5-124">Возвращает или задает список идентификаторов ресурсов по умолчанию, который принимает идентификатор ресурса Move, если только тип ввода не переключается с помощью свойства moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="c22f5-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="c22f5-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="c22f5-125">-MoveResourceInputType</span></span>
<span data-ttu-id="c22f5-126">Определяет тип ввода ресурсов перемещения.</span><span class="sxs-lookup"><span data-stu-id="c22f5-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="c22f5-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c22f5-127">-Name</span></span>
<span data-ttu-id="c22f5-128">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="c22f5-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c22f5-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="c22f5-129">-NoWait</span></span>
<span data-ttu-id="c22f5-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c22f5-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c22f5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22f5-131">-ResourceGroupName</span></span>
<span data-ttu-id="c22f5-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c22f5-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c22f5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c22f5-133">-SubscriptionId</span></span>
<span data-ttu-id="c22f5-134">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c22f5-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="c22f5-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="c22f5-135">-ValidateOnly</span></span>
<span data-ttu-id="c22f5-136">Возвращает или задает значение, показывающее, требуется ли операции запуск только предварительных требований.</span><span class="sxs-lookup"><span data-stu-id="c22f5-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="c22f5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c22f5-137">-Confirm</span></span>
<span data-ttu-id="c22f5-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c22f5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c22f5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c22f5-139">-WhatIf</span></span>
<span data-ttu-id="c22f5-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c22f5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c22f5-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c22f5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c22f5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22f5-142">CommonParameters</span></span>
<span data-ttu-id="c22f5-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c22f5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22f5-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c22f5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22f5-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c22f5-145">INPUTS</span></span>

## <span data-ttu-id="c22f5-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c22f5-146">OUTPUTS</span></span>

### <span data-ttu-id="c22f5-147">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="c22f5-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="c22f5-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c22f5-148">NOTES</span></span>

<span data-ttu-id="c22f5-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c22f5-149">ALIASES</span></span>

## <span data-ttu-id="c22f5-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c22f5-150">RELATED LINKS</span></span>

