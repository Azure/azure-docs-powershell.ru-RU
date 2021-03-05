---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: f8a50a7e9686a3e40f517992e6c4de9912e8671b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965107"
---
# <span data-ttu-id="34c95-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="34c95-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="34c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c95-102">SYNOPSIS</span></span>
<span data-ttu-id="34c95-103">Удалите руководство из подписки или группы управления.</span><span class="sxs-lookup"><span data-stu-id="34c95-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="34c95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34c95-104">SYNTAX</span></span>

### <span data-ttu-id="34c95-105">BySubscriptionAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34c95-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c95-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="34c95-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34c95-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="34c95-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c95-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c95-108">DESCRIPTION</span></span>
<span data-ttu-id="34c95-109">Удалите чертеж, который назначен подписке.</span><span class="sxs-lookup"><span data-stu-id="34c95-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="34c95-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34c95-110">EXAMPLES</span></span>

### <span data-ttu-id="34c95-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34c95-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="34c95-112">Удалите из указанной подписки название, указанное по имени.</span><span class="sxs-lookup"><span data-stu-id="34c95-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="34c95-113">Командлет запросит подтверждение перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="34c95-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="34c95-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34c95-114">PARAMETERS</span></span>

### <span data-ttu-id="34c95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c95-115">-DefaultProfile</span></span>
<span data-ttu-id="34c95-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34c95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c95-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34c95-117">-InputObject</span></span>
<span data-ttu-id="34c95-118">Объект назначения «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="34c95-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c95-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="34c95-119">-ManagementGroupId</span></span>
<span data-ttu-id="34c95-120">ИД группы управления, в которой сохранено назначение "Чертеж".</span><span class="sxs-lookup"><span data-stu-id="34c95-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c95-121">-Name</span><span class="sxs-lookup"><span data-stu-id="34c95-121">-Name</span></span>
<span data-ttu-id="34c95-122">Название задания «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="34c95-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c95-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34c95-123">-PassThru</span></span>
<span data-ttu-id="34c95-124">При этом будет возвращен объект, который представляет удаленное задание Blueprint.</span><span class="sxs-lookup"><span data-stu-id="34c95-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="34c95-125">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="34c95-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34c95-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34c95-126">-SubscriptionId</span></span>
<span data-ttu-id="34c95-127">Для этого развернется подписка с ИД чертежа.</span><span class="sxs-lookup"><span data-stu-id="34c95-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c95-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34c95-128">-Confirm</span></span>
<span data-ttu-id="34c95-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="34c95-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34c95-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c95-130">-WhatIf</span></span>
<span data-ttu-id="34c95-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34c95-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34c95-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34c95-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34c95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c95-133">CommonParameters</span></span>
<span data-ttu-id="34c95-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34c95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c95-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34c95-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c95-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34c95-136">INPUTS</span></span>

### <span data-ttu-id="34c95-137">System.String</span><span class="sxs-lookup"><span data-stu-id="34c95-137">System.String</span></span>

### <span data-ttu-id="34c95-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="34c95-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="34c95-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34c95-139">OUTPUTS</span></span>

### <span data-ttu-id="34c95-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="34c95-140">System.Object</span></span>
## <span data-ttu-id="34c95-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34c95-141">NOTES</span></span>

## <span data-ttu-id="34c95-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34c95-142">RELATED LINKS</span></span>
