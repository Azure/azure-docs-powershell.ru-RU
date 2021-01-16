---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507885"
---
# <span data-ttu-id="9b41e-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="9b41e-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="9b41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b41e-102">SYNOPSIS</span></span> 
<span data-ttu-id="9b41e-103">Получить список состояния VPN-клиентского подключения виртуального сетевого шлюза Azure для vpn-клиентского подключения</span><span class="sxs-lookup"><span data-stu-id="9b41e-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="9b41e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b41e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="9b41e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b41e-105">DESCRIPTION</span></span>
<span data-ttu-id="9b41e-106">Укаймь все подключенные vpn-клиентские подключения.</span><span class="sxs-lookup"><span data-stu-id="9b41e-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="9b41e-107">К ним относятся: VPNConnectionId VPNConnectionDuration VPNConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="9b41e-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="9b41e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b41e-108">EXAMPLES</span></span>

### <span data-ttu-id="9b41e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b41e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName gatewayName -ResourceGroupName resourceGroup

VpnConnectionId           : OVPN_0085393D-B345-4846-0426-140616833F4C
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39672
PrivateIpAddress          : 10.1.1.131
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104084
EgressBytesTransferred    : 4059276
IngressPacketsTransferred : 1410
IngressBytesTransferred   : 67680
MaxPacketsPerSecond       : 1

VpnConnectionId           : OVPN_00F692AC-2D6F-DE7B-DCAF-07BE896233A0
VpnConnectionDuration     : 27878
VpnConnectionTime         : 05/30/2019 16:03:11
PublicIpAddress           : 13.78.148.224:39692
PrivateIpAddress          : 10.1.1.79
VpnUserName               : GWP2SChildCert
MaxBandwidth              : 48000000
EgressPacketsTransferred  : 104623
EgressBytesTransferred    : 4080297
IngressPacketsTransferred : 1416
IngressBytesTransferred   : 67968
MaxPacketsPerSecond       : 1
```

<span data-ttu-id="9b41e-110">Для виртуального сетевого шлюза Azure с именем шлюза в группе ресурсов resourceGroup извлекает подключенное vpn-подключение с помощью OpenVpn.</span><span class="sxs-lookup"><span data-stu-id="9b41e-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="9b41e-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9b41e-111">Example 2</span></span>

<span data-ttu-id="9b41e-112">Получите список состояния VPN-клиентского подключения для виртуального сетевого шлюза Azure для vpn-клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="9b41e-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="9b41e-113">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="9b41e-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="9b41e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b41e-114">PARAMETERS</span></span>

### <span data-ttu-id="9b41e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b41e-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b41e-116">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="9b41e-116">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b41e-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9b41e-117">-ResourceName</span></span>
<span data-ttu-id="9b41e-118">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="9b41e-118">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="9b41e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b41e-119">-ResourceId</span></span>
<span data-ttu-id="9b41e-120">ИД ресурса виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="9b41e-120">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b41e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b41e-121">-InputObject</span></span>
<span data-ttu-id="9b41e-122">Объект виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="9b41e-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b41e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b41e-123">-AsJob</span></span>
<span data-ttu-id="9b41e-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9b41e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b41e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b41e-125">CommonParameters</span></span>
<span data-ttu-id="9b41e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b41e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b41e-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b41e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b41e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b41e-128">INPUTS</span></span>

### <span data-ttu-id="9b41e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9b41e-129">System.String</span></span>

## <span data-ttu-id="9b41e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b41e-130">OUTPUTS</span></span>

### <span data-ttu-id="9b41e-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="9b41e-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="9b41e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b41e-132">NOTES</span></span>

## <span data-ttu-id="9b41e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b41e-133">RELATED LINKS</span></span>
