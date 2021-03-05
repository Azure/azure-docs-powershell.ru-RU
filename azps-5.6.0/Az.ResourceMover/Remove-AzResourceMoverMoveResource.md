---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999859"
---
# <span data-ttu-id="3b421-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="3b421-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="3b421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b421-102">SYNOPSIS</span></span>
<span data-ttu-id="3b421-103">Удаляет ресурс из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="3b421-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="3b421-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b421-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3b421-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b421-105">DESCRIPTION</span></span>
<span data-ttu-id="3b421-106">Удаляет ресурс из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="3b421-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="3b421-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b421-107">EXAMPLES</span></span>

### <span data-ttu-id="3b421-108">Пример 1. Удаление одного из данных Move Rresource из коллекции Move Collection.</span><span class="sxs-lookup"><span data-stu-id="3b421-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="3b421-109">Удалите один из данных Move Rresource из коллекции перемещения.</span><span class="sxs-lookup"><span data-stu-id="3b421-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="3b421-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b421-110">PARAMETERS</span></span>

### <span data-ttu-id="3b421-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b421-111">-AsJob</span></span>
<span data-ttu-id="3b421-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3b421-112">Run the command as a job</span></span>

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

### <span data-ttu-id="3b421-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b421-113">-DefaultProfile</span></span>
<span data-ttu-id="3b421-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b421-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b421-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3b421-115">-MoveCollectionName</span></span>
<span data-ttu-id="3b421-116">Имя коллекции для перемещения.</span><span class="sxs-lookup"><span data-stu-id="3b421-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3b421-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3b421-117">-Name</span></span>
<span data-ttu-id="3b421-118">Имя перемещение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b421-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="3b421-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b421-119">-NoWait</span></span>
<span data-ttu-id="3b421-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3b421-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b421-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b421-121">-PassThru</span></span>
<span data-ttu-id="3b421-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="3b421-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3b421-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b421-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b421-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b421-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3b421-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b421-125">-SubscriptionId</span></span>
<span data-ttu-id="3b421-126">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="3b421-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="3b421-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b421-127">-Confirm</span></span>
<span data-ttu-id="3b421-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b421-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b421-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b421-129">-WhatIf</span></span>
<span data-ttu-id="3b421-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b421-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b421-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3b421-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b421-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b421-132">CommonParameters</span></span>
<span data-ttu-id="3b421-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b421-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b421-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b421-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b421-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b421-135">INPUTS</span></span>

## <span data-ttu-id="3b421-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b421-136">OUTPUTS</span></span>

### <span data-ttu-id="3b421-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3b421-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="3b421-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b421-138">NOTES</span></span>

<span data-ttu-id="3b421-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3b421-139">ALIASES</span></span>

## <span data-ttu-id="3b421-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b421-140">RELATED LINKS</span></span>

