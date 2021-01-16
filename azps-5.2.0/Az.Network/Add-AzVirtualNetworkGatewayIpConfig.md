---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410596"
---
# <span data-ttu-id="72225-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="72225-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="72225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72225-102">SYNOPSIS</span></span>
<span data-ttu-id="72225-103">Добавляет конфигурацию IP-адреса к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="72225-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="72225-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72225-104">SYNTAX</span></span>

### <span data-ttu-id="72225-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72225-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72225-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72225-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72225-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72225-107">DESCRIPTION</span></span>
<span data-ttu-id="72225-108">Командлет **Add-AzVirtualNetworkGatewayIpConfig** добавляет конфигурацию IP-адреса к виртуальному сетевому шлюзу.</span><span class="sxs-lookup"><span data-stu-id="72225-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="72225-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72225-109">EXAMPLES</span></span>

### <span data-ttu-id="72225-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72225-110">Example 1</span></span>
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

## <span data-ttu-id="72225-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72225-111">PARAMETERS</span></span>

### <span data-ttu-id="72225-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72225-112">-DefaultProfile</span></span>
<span data-ttu-id="72225-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72225-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72225-114">-Name</span><span class="sxs-lookup"><span data-stu-id="72225-114">-Name</span></span>
<span data-ttu-id="72225-115">Указывает имя добавляемой конфигурации IP-адреса шлюза.</span><span class="sxs-lookup"><span data-stu-id="72225-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="72225-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="72225-116">-PrivateIpAddress</span></span>
<span data-ttu-id="72225-117">Указывает частный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="72225-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="72225-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="72225-118">-PublicIpAddress</span></span>
<span data-ttu-id="72225-119">Указывает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="72225-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="72225-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="72225-120">-PublicIpAddressId</span></span>
<span data-ttu-id="72225-121">Определяет ИД общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="72225-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="72225-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="72225-122">-Subnet</span></span>
<span data-ttu-id="72225-123">Указывает объект **PSSubnet.**</span><span class="sxs-lookup"><span data-stu-id="72225-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="72225-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="72225-124">-SubnetId</span></span>
<span data-ttu-id="72225-125">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="72225-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="72225-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72225-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="72225-127">Указывает объект **PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="72225-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="72225-128">Этот командлет изменяет задаваемый объект **PSVirtualNetworkGateway.**</span><span class="sxs-lookup"><span data-stu-id="72225-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="72225-129">Для извлечения объекта **PSVirtualNetworkGateway** можно использовать Get-AzVirtualNetworkGateway командлет.</span><span class="sxs-lookup"><span data-stu-id="72225-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="72225-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72225-130">-Confirm</span></span>
<span data-ttu-id="72225-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72225-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72225-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72225-132">-WhatIf</span></span>
<span data-ttu-id="72225-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72225-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72225-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="72225-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72225-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72225-135">CommonParameters</span></span>
<span data-ttu-id="72225-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72225-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72225-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72225-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72225-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72225-138">INPUTS</span></span>

### <span data-ttu-id="72225-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72225-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="72225-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72225-140">OUTPUTS</span></span>

### <span data-ttu-id="72225-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72225-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="72225-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72225-142">NOTES</span></span>

## <span data-ttu-id="72225-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72225-143">RELATED LINKS</span></span>

[<span data-ttu-id="72225-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="72225-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="72225-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="72225-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="72225-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="72225-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)