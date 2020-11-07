---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: 88cdb68da94f84dc1af977ba5b12b5bfb4d73914
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721838"
---
# <span data-ttu-id="dd19a-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dd19a-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="dd19a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd19a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd19a-103">Создайте ресурс группы размещения близких.</span><span class="sxs-lookup"><span data-stu-id="dd19a-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="dd19a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd19a-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd19a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd19a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd19a-106">Этот командлет создаст ресурс группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="dd19a-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="dd19a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd19a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd19a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd19a-108">Example 1</span></span>
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

<span data-ttu-id="dd19a-109">Эта команда создает группу места близкого взаимодействия в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="dd19a-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="dd19a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd19a-110">PARAMETERS</span></span>

### <span data-ttu-id="dd19a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd19a-111">-AsJob</span></span>
<span data-ttu-id="dd19a-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dd19a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd19a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd19a-113">-DefaultProfile</span></span>
<span data-ttu-id="dd19a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd19a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd19a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="dd19a-115">-Location</span></span>
<span data-ttu-id="dd19a-116">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="dd19a-116">Resource location</span></span>

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

### <span data-ttu-id="dd19a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd19a-117">-Name</span></span>
<span data-ttu-id="dd19a-118">Имя группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="dd19a-118">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="dd19a-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="dd19a-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="dd19a-120">Указывает тип группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="dd19a-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="dd19a-121">Возможные значения: Standard или Ultra.</span><span class="sxs-lookup"><span data-stu-id="dd19a-121">Possible values are: Standard or Ultra</span></span>

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

### <span data-ttu-id="dd19a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd19a-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd19a-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd19a-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="dd19a-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="dd19a-124">-Tag</span></span>
<span data-ttu-id="dd19a-125">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd19a-125">Resource tags</span></span>

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

### <span data-ttu-id="dd19a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd19a-126">-Confirm</span></span>
<span data-ttu-id="dd19a-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd19a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd19a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd19a-128">-WhatIf</span></span>
<span data-ttu-id="dd19a-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd19a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd19a-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd19a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd19a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd19a-131">CommonParameters</span></span>
<span data-ttu-id="dd19a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd19a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd19a-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd19a-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd19a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd19a-134">INPUTS</span></span>

### <span data-ttu-id="dd19a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dd19a-135">System.String</span></span>

## <span data-ttu-id="dd19a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd19a-136">OUTPUTS</span></span>

### <span data-ttu-id="dd19a-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dd19a-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="dd19a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd19a-138">NOTES</span></span>

## <span data-ttu-id="dd19a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd19a-139">RELATED LINKS</span></span>
