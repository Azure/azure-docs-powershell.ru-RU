---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnGateway.md
ms.openlocfilehash: 7e68e8e48ffa9d86222951b7ca2e076351872be6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984374"
---
# <span data-ttu-id="fe706-101">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe706-101">New-AzVpnGateway</span></span>

## <span data-ttu-id="fe706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe706-102">SYNOPSIS</span></span>
<span data-ttu-id="fe706-103">Создает масштабируемый VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="fe706-103">Creates a Scalable VPN Gateway.</span></span>

## <span data-ttu-id="fe706-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe706-104">SYNTAX</span></span>

### <span data-ttu-id="fe706-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe706-105">ByVirtualHubName (Default)</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe706-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="fe706-106">ByVirtualHubObject</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe706-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="fe706-107">ByVirtualHubResourceId</span></span>
```
New-AzVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnConnection <PSVpnConnection[]>] [-EnableRoutingPreferenceInternetFlag] [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe706-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe706-108">DESCRIPTION</span></span>
<span data-ttu-id="fe706-109">New-AzVpnGateway создает масштабируемый VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="fe706-109">New-AzVpnGateway creates a scalable VPN Gateway.</span></span>
<span data-ttu-id="fe706-110">Это программное обеспечение, определяемое подключением сайта к подключениям к сайтам внутри VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fe706-110">This is software defined connectivity for site to site connections inside the VirtualHub.</span></span>

<span data-ttu-id="fe706-111">Размер и масштаб этого шлюза меняются в зависимости от единицы, указанной в этом или Set-AzVpnGateway блоке.</span><span class="sxs-lookup"><span data-stu-id="fe706-111">This gateway resizes and scales based on the scale unit specified in this or the Set-AzVpnGateway cmdlet.</span></span>

<span data-ttu-id="fe706-112">Подключение устанавливается из ветви или сайта (VPNSite) к масштабируемой шлюзу.</span><span class="sxs-lookup"><span data-stu-id="fe706-112">A connection is set up from a branch/Site known as VPNSite to the scalable gateway.</span></span>
<span data-ttu-id="fe706-113">Каждое подключение состоит из 2 Active-Active.</span><span class="sxs-lookup"><span data-stu-id="fe706-113">Each connection comprises of 2 Active-Active tunnels.</span></span>

<span data-ttu-id="fe706-114">VpnGateway будет расположен в том же расположении, что и в VirtualHub, на который ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="fe706-114">The VpnGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="fe706-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe706-115">EXAMPLES</span></span>

### <span data-ttu-id="fe706-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe706-116">Example 1</span></span>
```
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2 -EnableRoutingPreferenceInternetFlag

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="fe706-117">Выше будет создаваться группа ресурсов Virtual WAN, Виртуальная сеть, Виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="fe706-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fe706-118">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="fe706-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="fe706-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe706-119">PARAMETERS</span></span>

### <span data-ttu-id="fe706-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe706-120">-AsJob</span></span>
<span data-ttu-id="fe706-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fe706-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe706-122">-DefaultProfile</span></span>
<span data-ttu-id="fe706-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe706-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fe706-124">-Name</span></span>
<span data-ttu-id="fe706-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe706-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe706-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe706-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe706-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe706-128">-Tag</span></span>
<span data-ttu-id="fe706-129">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="fe706-129">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-130">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="fe706-130">-VirtualHub</span></span>
<span data-ttu-id="fe706-131">VirtualHub, с данным VpnGateway, должен быть связан.</span><span class="sxs-lookup"><span data-stu-id="fe706-131">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-132">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="fe706-132">-VirtualHubId</span></span>
<span data-ttu-id="fe706-133">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="fe706-133">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-134">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="fe706-134">-VirtualHubName</span></span>
<span data-ttu-id="fe706-135">С ИД VirtualHub этого VpnGateway нужно будет связан.</span><span class="sxs-lookup"><span data-stu-id="fe706-135">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-136">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="fe706-136">-VpnConnection</span></span>
<span data-ttu-id="fe706-137">Список VPNConnections, необходимых для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fe706-137">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-138">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="fe706-138">-VpnGatewayNatRule</span></span>
<span data-ttu-id="fe706-139">Список VpnGatewayNatRules, связанных с этим VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fe706-139">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-140">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="fe706-140">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="fe706-141">Единица масштаба для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="fe706-141">The scale unit for this VpnGateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-142">-EnableRoutingPreferenceInternetFlag</span><span class="sxs-lookup"><span data-stu-id="fe706-142">-EnableRoutingPreferenceInternetFlag</span></span>
<span data-ttu-id="fe706-143">Пометить, чтобы включить параметры маршрутации Интернета в этой VPNGateway.</span><span class="sxs-lookup"><span data-stu-id="fe706-143">Flag to enable Routing Preference Internet on this VpnGateway.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe706-144">-Confirm</span></span>
<span data-ttu-id="fe706-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe706-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe706-146">-WhatIf</span></span>
<span data-ttu-id="fe706-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe706-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe706-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe706-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe706-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe706-149">CommonParameters</span></span>
<span data-ttu-id="fe706-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe706-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe706-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe706-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe706-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe706-152">INPUTS</span></span>

### <span data-ttu-id="fe706-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fe706-153">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
### <span data-ttu-id="fe706-154">System.String</span><span class="sxs-lookup"><span data-stu-id="fe706-154">System.String</span></span>
## <span data-ttu-id="fe706-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe706-155">OUTPUTS</span></span>

### <span data-ttu-id="fe706-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe706-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>
## <span data-ttu-id="fe706-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe706-157">NOTES</span></span>

## <span data-ttu-id="fe706-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe706-158">RELATED LINKS</span></span>

[<span data-ttu-id="fe706-159">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe706-159">Get-AzVpnGateway</span></span>]()

[<span data-ttu-id="fe706-160">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe706-160">Remove-AzVpnGateway</span></span>]()

[<span data-ttu-id="fe706-161">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="fe706-161">Update-AzVpnGateway</span></span>]()

