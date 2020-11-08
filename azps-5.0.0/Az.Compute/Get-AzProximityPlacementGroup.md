---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249080"
---
# <span data-ttu-id="a1e11-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a1e11-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="a1e11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1e11-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e11-103">Получение или перечисление ресурсов группы размещения близких слов (ов).</span><span class="sxs-lookup"><span data-stu-id="a1e11-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="a1e11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1e11-104">SYNTAX</span></span>

### <span data-ttu-id="a1e11-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1e11-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e11-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a1e11-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e11-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1e11-107">DESCRIPTION</span></span>
<span data-ttu-id="a1e11-108">Этот командлет получит или перечислит ресурсы группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a1e11-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="a1e11-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1e11-109">EXAMPLES</span></span>

### <span data-ttu-id="a1e11-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1e11-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="a1e11-111">Эта команда получает группу размещения близких.</span><span class="sxs-lookup"><span data-stu-id="a1e11-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="a1e11-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a1e11-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="a1e11-113">В этой команде перечислены все группы размещения близкого взаимодействия в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1e11-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="a1e11-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a1e11-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="a1e11-115">В этой команде перечислены все группы размещения близких подписок в подписке.</span><span class="sxs-lookup"><span data-stu-id="a1e11-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="a1e11-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1e11-116">PARAMETERS</span></span>

### <span data-ttu-id="a1e11-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="a1e11-117">-ColocationStatus</span></span>
<span data-ttu-id="a1e11-118">Показывает состояние соположения ресурса в группе размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a1e11-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e11-119">-DefaultProfile</span></span>
<span data-ttu-id="a1e11-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e11-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1e11-121">-Name</span></span>
<span data-ttu-id="a1e11-122">Имя группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a1e11-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a1e11-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e11-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1e11-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1e11-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a1e11-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e11-125">-ResourceId</span></span>
<span data-ttu-id="a1e11-126">Идентификатор ресурса для группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="a1e11-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="a1e11-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e11-127">CommonParameters</span></span>
<span data-ttu-id="a1e11-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1e11-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e11-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1e11-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e11-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1e11-130">INPUTS</span></span>

### <span data-ttu-id="a1e11-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e11-131">System.String</span></span>

## <span data-ttu-id="a1e11-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1e11-132">OUTPUTS</span></span>

### <span data-ttu-id="a1e11-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a1e11-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="a1e11-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1e11-134">NOTES</span></span>

## <span data-ttu-id="a1e11-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1e11-135">RELATED LINKS</span></span>
