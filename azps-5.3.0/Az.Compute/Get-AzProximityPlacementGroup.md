---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509201"
---
# <span data-ttu-id="9f0d9-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d9-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="9f0d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0d9-103">Получить или список ресурсов группы «Расположение расположения» или «Список»)</span><span class="sxs-lookup"><span data-stu-id="9f0d9-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="9f0d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f0d9-104">SYNTAX</span></span>

### <span data-ttu-id="9f0d9-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f0d9-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f0d9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9f0d9-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f0d9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f0d9-107">DESCRIPTION</span></span>
<span data-ttu-id="9f0d9-108">Этот cmdlet will get or list Proximity Placement Group resource(s) для группы расположения списка.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="9f0d9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f0d9-109">EXAMPLES</span></span>

### <span data-ttu-id="9f0d9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f0d9-110">Example 1</span></span>
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

<span data-ttu-id="9f0d9-111">Эта команда получает группу расположения расположения близости</span><span class="sxs-lookup"><span data-stu-id="9f0d9-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="9f0d9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f0d9-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="9f0d9-113">В этом списке команд даются все группы расположения с учетом расположения в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="9f0d9-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9f0d9-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="9f0d9-115">В этом списке находятся все группы расположения расположения в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="9f0d9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f0d9-116">PARAMETERS</span></span>

### <span data-ttu-id="9f0d9-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="9f0d9-117">-ColocationStatus</span></span>
<span data-ttu-id="9f0d9-118">Указывает состояние расположения ресурса в группе расположения расположения.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="9f0d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0d9-119">-DefaultProfile</span></span>
<span data-ttu-id="9f0d9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f0d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9f0d9-121">-Name</span></span>
<span data-ttu-id="9f0d9-122">Имя группы расположений близости.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="9f0d9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0d9-123">-ResourceGroupName</span></span>
<span data-ttu-id="9f0d9-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f0d9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f0d9-125">-ResourceId</span></span>
<span data-ttu-id="9f0d9-126">ИД ресурса для группы расположения расположения близости.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="9f0d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0d9-127">CommonParameters</span></span>
<span data-ttu-id="9f0d9-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0d9-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f0d9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0d9-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f0d9-130">INPUTS</span></span>

### <span data-ttu-id="9f0d9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9f0d9-131">System.String</span></span>

## <span data-ttu-id="9f0d9-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f0d9-132">OUTPUTS</span></span>

### <span data-ttu-id="9f0d9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="9f0d9-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f0d9-134">NOTES</span></span>

## <span data-ttu-id="9f0d9-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f0d9-135">RELATED LINKS</span></span>
