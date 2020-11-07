---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913037"
---
# <span data-ttu-id="d2463-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d2463-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="d2463-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2463-102">SYNOPSIS</span></span>
<span data-ttu-id="d2463-103">Удалите ресурс группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d2463-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="d2463-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2463-104">SYNTAX</span></span>

### <span data-ttu-id="d2463-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2463-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2463-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d2463-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2463-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d2463-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2463-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2463-108">DESCRIPTION</span></span>
<span data-ttu-id="d2463-109">Этот командлет удалит ресурс группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d2463-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="d2463-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2463-110">EXAMPLES</span></span>

### <span data-ttu-id="d2463-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2463-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="d2463-112">Эта команда удаляет указанную группу размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d2463-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="d2463-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2463-113">PARAMETERS</span></span>

### <span data-ttu-id="d2463-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2463-114">-AsJob</span></span>
<span data-ttu-id="d2463-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d2463-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2463-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2463-116">-DefaultProfile</span></span>
<span data-ttu-id="d2463-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2463-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2463-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d2463-118">-Force</span></span>
<span data-ttu-id="d2463-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d2463-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2463-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2463-120">-InputObject</span></span>
<span data-ttu-id="d2463-121">Объект группы размещения близкого взаимодействия PS</span><span class="sxs-lookup"><span data-stu-id="d2463-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2463-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2463-122">-Name</span></span>
<span data-ttu-id="d2463-123">Имя группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d2463-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2463-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2463-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2463-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2463-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2463-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2463-126">-ResourceId</span></span>
<span data-ttu-id="d2463-127">Идентификатор ресурса для группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="d2463-127">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2463-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2463-128">-Confirm</span></span>
<span data-ttu-id="d2463-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2463-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2463-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2463-130">-WhatIf</span></span>
<span data-ttu-id="d2463-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2463-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2463-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2463-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2463-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2463-133">CommonParameters</span></span>
<span data-ttu-id="d2463-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2463-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2463-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2463-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2463-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2463-136">INPUTS</span></span>

### <span data-ttu-id="d2463-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d2463-137">System.String</span></span>

### <span data-ttu-id="d2463-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d2463-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="d2463-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2463-139">OUTPUTS</span></span>

### <span data-ttu-id="d2463-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d2463-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d2463-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2463-141">NOTES</span></span>

## <span data-ttu-id="d2463-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2463-142">RELATED LINKS</span></span>
