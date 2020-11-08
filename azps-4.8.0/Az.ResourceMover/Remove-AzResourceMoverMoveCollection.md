---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244007"
---
# <span data-ttu-id="dc9a4-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="dc9a4-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="dc9a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9a4-103">Удаляет коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-103">Deletes a move collection.</span></span>

## <span data-ttu-id="dc9a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc9a4-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc9a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc9a4-105">DESCRIPTION</span></span>
<span data-ttu-id="dc9a4-106">Удаляет коллекцию Move.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-106">Deletes a move collection.</span></span>

## <span data-ttu-id="dc9a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc9a4-107">EXAMPLES</span></span>

### <span data-ttu-id="dc9a4-108">Пример 1: Удаление коллекции Move из указанной подписки</span><span class="sxs-lookup"><span data-stu-id="dc9a4-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="dc9a4-109">Удаление коллекции Move из указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="dc9a4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc9a4-110">PARAMETERS</span></span>

### <span data-ttu-id="dc9a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc9a4-111">-AsJob</span></span>
<span data-ttu-id="dc9a4-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="dc9a4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="dc9a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9a4-113">-DefaultProfile</span></span>
<span data-ttu-id="dc9a4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc9a4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc9a4-115">-Name</span></span>
<span data-ttu-id="dc9a4-116">Имя перемещения коллекции.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="dc9a4-117">-Wait</span><span class="sxs-lookup"><span data-stu-id="dc9a4-117">-NoWait</span></span>
<span data-ttu-id="dc9a4-118">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="dc9a4-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc9a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc9a4-119">-PassThru</span></span>
<span data-ttu-id="dc9a4-120">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc9a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc9a4-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="dc9a4-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc9a4-123">-SubscriptionId</span></span>
<span data-ttu-id="dc9a4-124">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="dc9a4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc9a4-125">-Confirm</span></span>
<span data-ttu-id="dc9a4-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc9a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc9a4-127">-WhatIf</span></span>
<span data-ttu-id="dc9a4-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc9a4-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc9a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9a4-130">CommonParameters</span></span>
<span data-ttu-id="dc9a4-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc9a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9a4-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc9a4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9a4-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc9a4-133">INPUTS</span></span>

## <span data-ttu-id="dc9a4-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc9a4-134">OUTPUTS</span></span>

### <span data-ttu-id="dc9a4-135">Microsoft. Azure. PowerShell. командлеты. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="dc9a4-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="dc9a4-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc9a4-136">NOTES</span></span>

<span data-ttu-id="dc9a4-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="dc9a4-137">ALIASES</span></span>

## <span data-ttu-id="dc9a4-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc9a4-138">RELATED LINKS</span></span>

