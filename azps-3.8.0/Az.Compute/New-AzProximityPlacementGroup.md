---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065922"
---
# <span data-ttu-id="6e8ad-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6e8ad-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="6e8ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8ad-103">Создайте ресурс группы размещения близких.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="6e8ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e8ad-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e8ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e8ad-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8ad-106">Этот командлет создаст ресурс группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="6e8ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e8ad-107">EXAMPLES</span></span>

### <span data-ttu-id="6e8ad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e8ad-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="6e8ad-109">Эта команда создает группу места близкого взаимодействия в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="6e8ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e8ad-110">PARAMETERS</span></span>

### <span data-ttu-id="6e8ad-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e8ad-111">-AsJob</span></span>
<span data-ttu-id="6e8ad-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6e8ad-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e8ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8ad-113">-DefaultProfile</span></span>
<span data-ttu-id="6e8ad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e8ad-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6e8ad-115">-Location</span></span>
<span data-ttu-id="6e8ad-116">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="6e8ad-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ad-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e8ad-117">-Name</span></span>
<span data-ttu-id="6e8ad-118">Имя группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ad-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="6e8ad-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="6e8ad-120">Указывает тип группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="6e8ad-121">Возможные значения: Standard или Ultra.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e8ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e8ad-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ad-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="6e8ad-124">-Tag</span></span>
<span data-ttu-id="6e8ad-125">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="6e8ad-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ad-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e8ad-126">-Confirm</span></span>
<span data-ttu-id="6e8ad-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e8ad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e8ad-128">-WhatIf</span></span>
<span data-ttu-id="6e8ad-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e8ad-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e8ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8ad-131">CommonParameters</span></span>
<span data-ttu-id="6e8ad-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e8ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8ad-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e8ad-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8ad-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e8ad-134">INPUTS</span></span>

### <span data-ttu-id="6e8ad-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6e8ad-135">System.String</span></span>

## <span data-ttu-id="6e8ad-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e8ad-136">OUTPUTS</span></span>

### <span data-ttu-id="6e8ad-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6e8ad-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="6e8ad-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e8ad-138">NOTES</span></span>

## <span data-ttu-id="6e8ad-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e8ad-139">RELATED LINKS</span></span>
