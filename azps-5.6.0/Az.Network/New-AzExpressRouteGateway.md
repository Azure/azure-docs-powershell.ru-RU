---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: df81d3df31ad1d04914164d04321151e0df2dfdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974771"
---
# <span data-ttu-id="f817f-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f817f-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="f817f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f817f-102">SYNOPSIS</span></span>
<span data-ttu-id="f817f-103">Создает шлюз ExpressRoute в масштабируемом масштабе.</span><span class="sxs-lookup"><span data-stu-id="f817f-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="f817f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f817f-104">SYNTAX</span></span>

### <span data-ttu-id="f817f-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f817f-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f817f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="f817f-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f817f-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="f817f-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f817f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f817f-108">DESCRIPTION</span></span>

<span data-ttu-id="f817f-109">New-AzExpressRouteGateway создает масштабируемый шлюз ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f817f-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="f817f-110">Это программное обеспечение, определяемое подключением локально к Azure в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="f817f-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="f817f-111">Масштаб этого шлюза можно масштабировать с учетом единицы, указанной в этом или Set-AzExpressRouteGateway этом проекте.</span><span class="sxs-lookup"><span data-stu-id="f817f-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="f817f-112">Подключение устанавливается из локального контура ExpressRoute к масштабируемого шлюзу.</span><span class="sxs-lookup"><span data-stu-id="f817f-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="f817f-113">ExpressRouteGateway будет расположен в том же расположении, что и на нее.</span><span class="sxs-lookup"><span data-stu-id="f817f-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="f817f-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f817f-114">EXAMPLES</span></span>

### <span data-ttu-id="f817f-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f817f-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="f817f-116">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="f817f-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="f817f-117">В этом примере в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="f817f-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="f817f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f817f-118">PARAMETERS</span></span>

### <span data-ttu-id="f817f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f817f-119">-AsJob</span></span>
<span data-ttu-id="f817f-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f817f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f817f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f817f-121">-DefaultProfile</span></span>
<span data-ttu-id="f817f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f817f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f817f-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="f817f-123">-MaxScaleUnits</span></span>
<span data-ttu-id="f817f-124">Максимальное количество единиц масштаба для этой темы ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="f817f-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="f817f-125">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="f817f-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f817f-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="f817f-126">-MinScaleUnits</span></span>
<span data-ttu-id="f817f-127">Минимальное количество единиц масштаба для этой темы ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="f817f-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="f817f-128">Допустимый диапазон > 2</span><span class="sxs-lookup"><span data-stu-id="f817f-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f817f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f817f-129">-Name</span></span>
<span data-ttu-id="f817f-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f817f-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f817f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f817f-131">-ResourceGroupName</span></span>
<span data-ttu-id="f817f-132">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f817f-132">The resource name.</span></span>

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

### <span data-ttu-id="f817f-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f817f-133">-Tag</span></span>
<span data-ttu-id="f817f-134">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="f817f-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f817f-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f817f-135">-VirtualHub</span></span>
<span data-ttu-id="f817f-136">VirtualHub, с данным VpnGateway, должен быть связан.</span><span class="sxs-lookup"><span data-stu-id="f817f-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f817f-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="f817f-137">-VirtualHubId</span></span>
<span data-ttu-id="f817f-138">С ИД VirtualHub этого VpnGateway необходимо связан.</span><span class="sxs-lookup"><span data-stu-id="f817f-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f817f-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="f817f-139">-VirtualHubName</span></span>
<span data-ttu-id="f817f-140">С ИД VirtualHub этого VpnGateway необходимо связан.</span><span class="sxs-lookup"><span data-stu-id="f817f-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f817f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f817f-141">-Confirm</span></span>
<span data-ttu-id="f817f-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f817f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f817f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f817f-143">-WhatIf</span></span>
<span data-ttu-id="f817f-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f817f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f817f-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f817f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f817f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f817f-146">CommonParameters</span></span>
<span data-ttu-id="f817f-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f817f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f817f-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f817f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f817f-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f817f-149">INPUTS</span></span>

### <span data-ttu-id="f817f-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f817f-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="f817f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f817f-151">System.String</span></span>

## <span data-ttu-id="f817f-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f817f-152">OUTPUTS</span></span>

### <span data-ttu-id="f817f-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="f817f-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="f817f-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f817f-154">NOTES</span></span>

## <span data-ttu-id="f817f-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f817f-155">RELATED LINKS</span></span>
