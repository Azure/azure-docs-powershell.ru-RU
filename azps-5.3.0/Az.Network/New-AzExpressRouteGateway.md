---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505540"
---
# <span data-ttu-id="d7446-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d7446-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="d7446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7446-102">SYNOPSIS</span></span>
<span data-ttu-id="d7446-103">Создает шлюз ExpressRoute в масштабируемом масштабе.</span><span class="sxs-lookup"><span data-stu-id="d7446-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="d7446-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7446-104">SYNTAX</span></span>

### <span data-ttu-id="d7446-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7446-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7446-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d7446-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7446-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d7446-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7446-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7446-108">DESCRIPTION</span></span>

<span data-ttu-id="d7446-109">New-AzExpressRouteGateway создает масштабируемый шлюз ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d7446-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="d7446-110">Это программное обеспечение, определяемое подключение локально к Azure в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d7446-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="d7446-111">Масштаб этого шлюза можно масштабировать с учетом единицы, заданной в этом или Set-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="d7446-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="d7446-112">Подключение устанавливается из локального контура ExpressRoute к масштабируемого шлюзу.</span><span class="sxs-lookup"><span data-stu-id="d7446-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="d7446-113">ExpressRouteGateway будет расположен в том же расположении, что и на нее.</span><span class="sxs-lookup"><span data-stu-id="d7446-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="d7446-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7446-114">EXAMPLES</span></span>

### <span data-ttu-id="d7446-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7446-115">Example 1</span></span>

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

<span data-ttu-id="d7446-116">Выше будет создаваться группа ресурсов Virtual WAN, Виртуальная сеть, Виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="d7446-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="d7446-117">В этом примере в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="d7446-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="d7446-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7446-118">PARAMETERS</span></span>

### <span data-ttu-id="d7446-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7446-119">-AsJob</span></span>
<span data-ttu-id="d7446-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d7446-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7446-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7446-121">-DefaultProfile</span></span>
<span data-ttu-id="d7446-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7446-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7446-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="d7446-123">-MaxScaleUnits</span></span>
<span data-ttu-id="d7446-124">Максимальное количество единиц масштаба для этой темы ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="d7446-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="d7446-125">Допустимый > 2</span><span class="sxs-lookup"><span data-stu-id="d7446-125">Valid range > 2</span></span>

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

### <span data-ttu-id="d7446-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="d7446-126">-MinScaleUnits</span></span>
<span data-ttu-id="d7446-127">Минимальное количество единиц масштаба для этой темы ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="d7446-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="d7446-128">Допустимый > 2</span><span class="sxs-lookup"><span data-stu-id="d7446-128">Valid range > 2</span></span>

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

### <span data-ttu-id="d7446-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d7446-129">-Name</span></span>
<span data-ttu-id="d7446-130">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7446-130">The resource name.</span></span>

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

### <span data-ttu-id="d7446-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7446-131">-ResourceGroupName</span></span>
<span data-ttu-id="d7446-132">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7446-132">The resource name.</span></span>

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

### <span data-ttu-id="d7446-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7446-133">-Tag</span></span>
<span data-ttu-id="d7446-134">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="d7446-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d7446-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d7446-135">-VirtualHub</span></span>
<span data-ttu-id="d7446-136">VirtualHub, с данным VpnGateway, должен быть связан.</span><span class="sxs-lookup"><span data-stu-id="d7446-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d7446-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d7446-137">-VirtualHubId</span></span>
<span data-ttu-id="d7446-138">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="d7446-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d7446-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="d7446-139">-VirtualHubName</span></span>
<span data-ttu-id="d7446-140">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="d7446-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="d7446-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7446-141">-Confirm</span></span>
<span data-ttu-id="d7446-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d7446-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7446-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7446-143">-WhatIf</span></span>
<span data-ttu-id="d7446-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7446-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7446-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d7446-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7446-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7446-146">CommonParameters</span></span>
<span data-ttu-id="d7446-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7446-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7446-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7446-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7446-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7446-149">INPUTS</span></span>

### <span data-ttu-id="d7446-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d7446-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d7446-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d7446-151">System.String</span></span>

## <span data-ttu-id="d7446-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7446-152">OUTPUTS</span></span>

### <span data-ttu-id="d7446-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="d7446-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="d7446-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7446-154">NOTES</span></span>

## <span data-ttu-id="d7446-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7446-155">RELATED LINKS</span></span>
