---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214004"
---
# <span data-ttu-id="bc9e6-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc9e6-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="bc9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9e6-103">Добавляет конфигурацию IP-адреса к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="bc9e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc9e6-104">SYNTAX</span></span>

### <span data-ttu-id="bc9e6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc9e6-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc9e6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bc9e6-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc9e6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc9e6-107">DESCRIPTION</span></span>
<span data-ttu-id="bc9e6-108">Командлет **Add-AzVirtualNetworkGatewayIpConfig** добавляет конфигурацию IP-адреса к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="bc9e6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc9e6-109">EXAMPLES</span></span>

### <span data-ttu-id="bc9e6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc9e6-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="bc9e6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc9e6-111">PARAMETERS</span></span>

### <span data-ttu-id="bc9e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9e6-112">-DefaultProfile</span></span>
<span data-ttu-id="bc9e6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc9e6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bc9e6-114">-Name</span></span>
<span data-ttu-id="bc9e6-115">Указывает имя добавляемой конфигурации IP-адреса шлюза.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="bc9e6-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc9e6-116">-PrivateIpAddress</span></span>
<span data-ttu-id="bc9e6-117">Указывает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="bc9e6-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bc9e6-118">-PublicIpAddress</span></span>
<span data-ttu-id="bc9e6-119">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="bc9e6-120">-PublicIpAddressId</span></span>
<span data-ttu-id="bc9e6-121">Определяет ИД общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="bc9e6-122">-Subnet</span></span>
<span data-ttu-id="bc9e6-123">Указывает объект **PSSubnet.**</span><span class="sxs-lookup"><span data-stu-id="bc9e6-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="bc9e6-124">-SubnetId</span></span>
<span data-ttu-id="bc9e6-125">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc9e6-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bc9e6-127">Указывает объект **PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="bc9e6-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="bc9e6-128">Этот командлет изменяет задаваемый объект **PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="bc9e6-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="bc9e6-129">Для получения объекта **PSVirtualNetworkGateway** можно использовать командлет Get-AzVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc9e6-130">-Confirm</span></span>
<span data-ttu-id="bc9e6-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc9e6-132">-WhatIf</span></span>
<span data-ttu-id="bc9e6-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc9e6-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc9e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9e6-135">CommonParameters</span></span>
<span data-ttu-id="bc9e6-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc9e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9e6-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc9e6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9e6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc9e6-138">INPUTS</span></span>

### <span data-ttu-id="bc9e6-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc9e6-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bc9e6-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc9e6-140">OUTPUTS</span></span>

### <span data-ttu-id="bc9e6-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc9e6-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bc9e6-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc9e6-142">NOTES</span></span>

## <span data-ttu-id="bc9e6-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc9e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="bc9e6-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc9e6-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="bc9e6-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc9e6-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="bc9e6-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bc9e6-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
