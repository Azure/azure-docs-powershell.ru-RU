---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999880"
---
# <span data-ttu-id="72270-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="72270-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="72270-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72270-102">SYNOPSIS</span></span>
<span data-ttu-id="72270-103">Удаляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="72270-103">Deletes a move collection.</span></span>

## <span data-ttu-id="72270-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72270-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="72270-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72270-105">DESCRIPTION</span></span>
<span data-ttu-id="72270-106">Удаляет коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="72270-106">Deletes a move collection.</span></span>

## <span data-ttu-id="72270-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72270-107">EXAMPLES</span></span>

### <span data-ttu-id="72270-108">Пример 1. Удаление коллекции "Перемещение".</span><span class="sxs-lookup"><span data-stu-id="72270-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="72270-109">Удалите коллекцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="72270-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="72270-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72270-110">PARAMETERS</span></span>

### <span data-ttu-id="72270-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72270-111">-AsJob</span></span>
<span data-ttu-id="72270-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="72270-112">Run the command as a job</span></span>

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

### <span data-ttu-id="72270-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72270-113">-DefaultProfile</span></span>
<span data-ttu-id="72270-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72270-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72270-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72270-115">-Name</span></span>
<span data-ttu-id="72270-116">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="72270-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="72270-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="72270-117">-NoWait</span></span>
<span data-ttu-id="72270-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="72270-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="72270-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72270-119">-PassThru</span></span>
<span data-ttu-id="72270-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="72270-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="72270-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72270-121">-ResourceGroupName</span></span>
<span data-ttu-id="72270-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72270-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="72270-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72270-123">-SubscriptionId</span></span>
<span data-ttu-id="72270-124">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="72270-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="72270-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72270-125">-Confirm</span></span>
<span data-ttu-id="72270-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72270-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72270-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72270-127">-WhatIf</span></span>
<span data-ttu-id="72270-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72270-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72270-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="72270-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72270-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72270-130">CommonParameters</span></span>
<span data-ttu-id="72270-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72270-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72270-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72270-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72270-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72270-133">INPUTS</span></span>

## <span data-ttu-id="72270-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72270-134">OUTPUTS</span></span>

### <span data-ttu-id="72270-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="72270-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="72270-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72270-136">NOTES</span></span>

<span data-ttu-id="72270-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="72270-137">ALIASES</span></span>

## <span data-ttu-id="72270-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72270-138">RELATED LINKS</span></span>

