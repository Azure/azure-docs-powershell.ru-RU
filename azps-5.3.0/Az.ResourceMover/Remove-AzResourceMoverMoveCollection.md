---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505337"
---
# <span data-ttu-id="9d81d-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="9d81d-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="9d81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d81d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d81d-103">Удаляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="9d81d-103">Deletes a move collection.</span></span>

## <span data-ttu-id="9d81d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d81d-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d81d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d81d-105">DESCRIPTION</span></span>
<span data-ttu-id="9d81d-106">Удаляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="9d81d-106">Deletes a move collection.</span></span>

## <span data-ttu-id="9d81d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d81d-107">EXAMPLES</span></span>

### <span data-ttu-id="9d81d-108">Пример 1. Удаление коллекции для перемещения из указанной подписки</span><span class="sxs-lookup"><span data-stu-id="9d81d-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
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

<span data-ttu-id="9d81d-109">Удалите коллекцию "Переместить из указанной подписки".</span><span class="sxs-lookup"><span data-stu-id="9d81d-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="9d81d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d81d-110">PARAMETERS</span></span>

### <span data-ttu-id="9d81d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d81d-111">-AsJob</span></span>
<span data-ttu-id="9d81d-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9d81d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9d81d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d81d-113">-DefaultProfile</span></span>
<span data-ttu-id="9d81d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d81d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d81d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9d81d-115">-Name</span></span>
<span data-ttu-id="9d81d-116">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="9d81d-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9d81d-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9d81d-117">-NoWait</span></span>
<span data-ttu-id="9d81d-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9d81d-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d81d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d81d-119">-PassThru</span></span>
<span data-ttu-id="9d81d-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="9d81d-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9d81d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d81d-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d81d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d81d-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9d81d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d81d-123">-SubscriptionId</span></span>
<span data-ttu-id="9d81d-124">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="9d81d-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="9d81d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d81d-125">-Confirm</span></span>
<span data-ttu-id="9d81d-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d81d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d81d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d81d-127">-WhatIf</span></span>
<span data-ttu-id="9d81d-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d81d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d81d-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d81d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d81d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d81d-130">CommonParameters</span></span>
<span data-ttu-id="9d81d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d81d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d81d-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d81d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d81d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d81d-133">INPUTS</span></span>

## <span data-ttu-id="9d81d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d81d-134">OUTPUTS</span></span>

### <span data-ttu-id="9d81d-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="9d81d-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="9d81d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d81d-136">NOTES</span></span>

<span data-ttu-id="9d81d-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9d81d-137">ALIASES</span></span>

## <span data-ttu-id="9d81d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d81d-138">RELATED LINKS</span></span>

