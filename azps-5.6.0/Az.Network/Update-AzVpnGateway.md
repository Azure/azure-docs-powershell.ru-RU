---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnGateway.md
ms.openlocfilehash: d04c665bce4c37425564e4eb65ff46da3b39fa8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951459"
---
# <span data-ttu-id="bd7e6-101">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd7e6-101">Update-AzVpnGateway</span></span>

## <span data-ttu-id="bd7e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7e6-103">Обновляет масштабируемый VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-103">Updates a scalable VPN gateway.</span></span>

## <span data-ttu-id="bd7e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd7e6-104">SYNTAX</span></span>

### <span data-ttu-id="bd7e6-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd7e6-105">ByVpnGatewayName (Default)</span></span>
```
Update-AzVpnGateway -ResourceGroupName <String> -Name <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd7e6-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="bd7e6-106">ByVpnGatewayObject</span></span>
```
Update-AzVpnGateway -InputObject <PSVpnGateway> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd7e6-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7e6-107">ByVpnGatewayResourceId</span></span>
```
Update-AzVpnGateway -ResourceId <String> [-VpnConnection <PSVpnConnection[]>]
 [-VpnGatewayNatRule <PSVpnGatewayNatRule[]>] [-VpnGatewayScaleUnit <UInt32>]
 [-BgpPeeringAddress <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd7e6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd7e6-108">DESCRIPTION</span></span>
<span data-ttu-id="bd7e6-109">С **помощью cmdlet Update-AzVpnGateway** можно обновить VPN-шлюз в масштабируемом масштабе.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-109">The **Update-AzVpnGateway** cmdlet updates a scalable VPN gateway.</span></span>  
<span data-ttu-id="bd7e6-110">VPN-шлюз Azure — это программное обеспечение, определяемое подключением сайта к подключениям к сайтам в VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-110">An Azure VPN gateway is a software defined connectivity for site to site connections inside the VirtualHub.</span></span> <span data-ttu-id="bd7e6-111">Масштаб этого шлюза будет меняться в зависимости от единицы, указанной пользователем.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-111">This gateway resizes and scales based on the scale unit specified by the user.</span></span> <span data-ttu-id="bd7e6-112">Подключение можно настроить из филиала или сайта, который называется VPN-сайтом, к масштабируемой шлюзу.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-112">A connection can be set up from a branch/site known as VPN site to the scalable gateway.</span></span> <span data-ttu-id="bd7e6-113">Каждое подключение состоит из 2 Active-Active туннельов.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-113">Each connection comprises of 2 Active-Active tunnels</span></span>

## <span data-ttu-id="bd7e6-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd7e6-114">EXAMPLES</span></span>

### <span data-ttu-id="bd7e6-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd7e6-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VpnGatewayScaleUnit 3

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="bd7e6-116">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="bd7e6-117">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-117">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="bd7e6-118">После создания шлюза с помощью Update-AzVpnGateway его можно обновить до трехблоков.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-118">After the gateway has been created, it uses  Update-AzVpnGateway to upgrade the gateway to 3 scale units.</span></span>

### <span data-ttu-id="bd7e6-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd7e6-119">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> $vpnGateway = New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\>$ipconfigurationId1 = 'Instance0'
PS C:\>$addresslist1 = @('169.254.21.5')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>$ipconfigurationId2 = 'Instance1'
PS C:\>$addresslist2 = @('169.254.21.10')
PS C:\>$gw1ipconfBgp2 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId2 -CustomAddress $addresslist2
PS C:\>$gw = Get-AzVpnGateway -ResourceGroupName testRg -Name testgw
PS C:\> Update-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -BgpPeeringAddress @($gw1ipconfBgp1,$gw1ipconfBgp2)

ResourceGroupName   : testRG
Name                : testvpngw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnGateways/testvpngw
Location            : West US
VpnGatewayScaleUnit : 3
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/Ali_pS_Test/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/vpnGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="bd7e6-120">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-120">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="bd7e6-121">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-121">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="bd7e6-122">После создания шлюза с помощью Set-AzVpnGateway BgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-122">After the gateway has been created, it uses Set-AzVpnGateway to update BgpPeeringAddress.</span></span>

## <span data-ttu-id="bd7e6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd7e6-123">PARAMETERS</span></span>

### <span data-ttu-id="bd7e6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd7e6-124">-AsJob</span></span>
<span data-ttu-id="bd7e6-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd7e6-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd7e6-126">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="bd7e6-126">-BgpPeeringAddress</span></span>
<span data-ttu-id="bd7e6-127">Адреса пиринга BGP для этого Bgpsettings VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-127">The BGP peering addresses for this VpnGateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7e6-128">-DefaultProfile</span></span>
<span data-ttu-id="bd7e6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd7e6-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd7e6-130">-InputObject</span></span>
<span data-ttu-id="bd7e6-131">Объект VPN-шлюза, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="bd7e6-131">The vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="bd7e6-132">-Name</span></span>
<span data-ttu-id="bd7e6-133">Имя vpn-шлюза.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-133">The vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd7e6-134">-ResourceGroupName</span></span>
<span data-ttu-id="bd7e6-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e6-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7e6-136">-ResourceId</span></span>
<span data-ttu-id="bd7e6-137">ИД ресурсов Azure для VpnGateway, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-137">The Azure resource ID of the VpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e6-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd7e6-138">-Tag</span></span>
<span data-ttu-id="bd7e6-139">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-139">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="bd7e6-140">-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bd7e6-140">-VpnConnection</span></span>
<span data-ttu-id="bd7e6-141">Список VPNConnections, необходимых для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-141">The list of VpnConnections that this VpnGateway needs to have.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e6-142">-VpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="bd7e6-142">-VpnGatewayNatRule</span></span>
<span data-ttu-id="bd7e6-143">Список VpnGatewayNatRules, связанных с этим VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-143">The list of VpnGatewayNatRules that are associated with this VpnGateway.</span></span>

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

### <span data-ttu-id="bd7e6-144">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bd7e6-144">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="bd7e6-145">Единица масштаба для этого VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-145">The scale unit for this VpnGateway.</span></span>

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

### <span data-ttu-id="bd7e6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd7e6-146">-Confirm</span></span>
<span data-ttu-id="bd7e6-147">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd7e6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7e6-148">-WhatIf</span></span>
<span data-ttu-id="bd7e6-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd7e6-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd7e6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7e6-151">CommonParameters</span></span>
<span data-ttu-id="bd7e6-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7e6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7e6-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd7e6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7e6-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd7e6-154">INPUTS</span></span>

### <span data-ttu-id="bd7e6-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd7e6-155">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="bd7e6-156">System.String</span><span class="sxs-lookup"><span data-stu-id="bd7e6-156">System.String</span></span>

## <span data-ttu-id="bd7e6-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd7e6-157">OUTPUTS</span></span>

### <span data-ttu-id="bd7e6-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd7e6-158">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="bd7e6-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd7e6-159">NOTES</span></span>

## <span data-ttu-id="bd7e6-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd7e6-160">RELATED LINKS</span></span>

[<span data-ttu-id="bd7e6-161">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd7e6-161">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="bd7e6-162">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd7e6-162">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="bd7e6-163">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="bd7e6-163">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)