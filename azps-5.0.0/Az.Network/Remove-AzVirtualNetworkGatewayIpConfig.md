---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 3287644b3f953c001490c7be207865a88b000e10
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248300"
---
# <span data-ttu-id="0fe37-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0fe37-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="0fe37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fe37-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe37-103">Удаление конфигурации IP из шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0fe37-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="0fe37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fe37-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fe37-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe37-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe37-106">Удаление конфигурации IP из шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0fe37-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="0fe37-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fe37-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe37-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="0fe37-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="0fe37-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fe37-109">PARAMETERS</span></span>

### <span data-ttu-id="0fe37-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe37-110">-DefaultProfile</span></span>
<span data-ttu-id="0fe37-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe37-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fe37-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fe37-112">-Name</span></span>
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

### <span data-ttu-id="0fe37-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe37-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="0fe37-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fe37-114">-Confirm</span></span>
<span data-ttu-id="0fe37-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fe37-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fe37-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fe37-116">-WhatIf</span></span>
<span data-ttu-id="0fe37-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fe37-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fe37-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fe37-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fe37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe37-119">CommonParameters</span></span>
<span data-ttu-id="0fe37-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fe37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe37-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe37-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe37-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fe37-122">INPUTS</span></span>

### <span data-ttu-id="0fe37-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe37-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0fe37-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe37-124">OUTPUTS</span></span>

### <span data-ttu-id="0fe37-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe37-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="0fe37-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fe37-126">NOTES</span></span>

## <span data-ttu-id="0fe37-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fe37-127">RELATED LINKS</span></span>

[<span data-ttu-id="0fe37-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0fe37-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="0fe37-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0fe37-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)
