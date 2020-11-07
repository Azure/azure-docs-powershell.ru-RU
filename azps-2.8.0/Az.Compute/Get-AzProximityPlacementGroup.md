---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 9ec2760ba50d4ed97ebf36f5bab7c02d110d77ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727468"
---
# <span data-ttu-id="8cac6-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8cac6-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="8cac6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cac6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cac6-103">Получение или перечисление ресурсов группы размещения близких слов (ов).</span><span class="sxs-lookup"><span data-stu-id="8cac6-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="8cac6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cac6-104">SYNTAX</span></span>

### <span data-ttu-id="8cac6-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cac6-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cac6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8cac6-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cac6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cac6-107">DESCRIPTION</span></span>
<span data-ttu-id="8cac6-108">Этот командлет получит или перечислит ресурсы группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="8cac6-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="8cac6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cac6-109">EXAMPLES</span></span>

### <span data-ttu-id="8cac6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8cac6-110">Example 1</span></span>
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

<span data-ttu-id="8cac6-111">Эта команда получает группу размещения близких.</span><span class="sxs-lookup"><span data-stu-id="8cac6-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="8cac6-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8cac6-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="8cac6-113">В этой команде перечислены все группы размещения близкого взаимодействия в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8cac6-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="8cac6-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8cac6-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="8cac6-115">В этой команде перечислены все группы размещения близких подписок в подписке.</span><span class="sxs-lookup"><span data-stu-id="8cac6-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="8cac6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cac6-116">PARAMETERS</span></span>

### <span data-ttu-id="8cac6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cac6-117">-DefaultProfile</span></span>
<span data-ttu-id="8cac6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cac6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cac6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cac6-119">-Name</span></span>
<span data-ttu-id="8cac6-120">Имя группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="8cac6-120">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="8cac6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cac6-121">-ResourceGroupName</span></span>
<span data-ttu-id="8cac6-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8cac6-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cac6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cac6-123">-ResourceId</span></span>
<span data-ttu-id="8cac6-124">Идентификатор ресурса для группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="8cac6-124">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="8cac6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cac6-125">CommonParameters</span></span>
<span data-ttu-id="8cac6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cac6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cac6-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cac6-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cac6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cac6-128">INPUTS</span></span>

### <span data-ttu-id="8cac6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8cac6-129">System.String</span></span>

## <span data-ttu-id="8cac6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cac6-130">OUTPUTS</span></span>

### <span data-ttu-id="8cac6-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8cac6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="8cac6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cac6-132">NOTES</span></span>

## <span data-ttu-id="8cac6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cac6-133">RELATED LINKS</span></span>
