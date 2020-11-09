---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317645"
---
# <span data-ttu-id="c501c-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="c501c-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="c501c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c501c-102">SYNOPSIS</span></span>
<span data-ttu-id="c501c-103">Удаляет ресурс перемещения из коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="c501c-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="c501c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c501c-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c501c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c501c-105">DESCRIPTION</span></span>
<span data-ttu-id="c501c-106">Удаляет ресурс перемещения из коллекции Move.</span><span class="sxs-lookup"><span data-stu-id="c501c-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="c501c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c501c-107">EXAMPLES</span></span>

### <span data-ttu-id="c501c-108">Пример 1: Удаление ресурса из коллекции Move</span><span class="sxs-lookup"><span data-stu-id="c501c-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="c501c-109">Удаление ресурса из коллекции Move в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="c501c-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="c501c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c501c-110">PARAMETERS</span></span>

### <span data-ttu-id="c501c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c501c-111">-AsJob</span></span>
<span data-ttu-id="c501c-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c501c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c501c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c501c-113">-DefaultProfile</span></span>
<span data-ttu-id="c501c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c501c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c501c-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c501c-115">-MoveCollectionName</span></span>
<span data-ttu-id="c501c-116">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="c501c-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c501c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c501c-117">-Name</span></span>
<span data-ttu-id="c501c-118">Имя ресурса для перемещения.</span><span class="sxs-lookup"><span data-stu-id="c501c-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c501c-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="c501c-119">-NoWait</span></span>
<span data-ttu-id="c501c-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c501c-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c501c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c501c-121">-PassThru</span></span>
<span data-ttu-id="c501c-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c501c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c501c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c501c-123">-ResourceGroupName</span></span>
<span data-ttu-id="c501c-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c501c-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c501c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c501c-125">-SubscriptionId</span></span>
<span data-ttu-id="c501c-126">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c501c-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="c501c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c501c-127">-Confirm</span></span>
<span data-ttu-id="c501c-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c501c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c501c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c501c-129">-WhatIf</span></span>
<span data-ttu-id="c501c-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c501c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c501c-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c501c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c501c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c501c-132">CommonParameters</span></span>
<span data-ttu-id="c501c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c501c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c501c-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c501c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c501c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c501c-135">INPUTS</span></span>

## <span data-ttu-id="c501c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c501c-136">OUTPUTS</span></span>

### <span data-ttu-id="c501c-137">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="c501c-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="c501c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c501c-138">NOTES</span></span>

<span data-ttu-id="c501c-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c501c-139">ALIASES</span></span>

## <span data-ttu-id="c501c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c501c-140">RELATED LINKS</span></span>

