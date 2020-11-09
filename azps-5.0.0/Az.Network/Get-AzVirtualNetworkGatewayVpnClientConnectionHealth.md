---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayvpnclientconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayVpnClientConnectionHealth.md
ms.openlocfilehash: 21529e75ab32cf4dde0434b9e2d4de8951beeb39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316115"
---
# <span data-ttu-id="3c532-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3c532-101">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>

## <span data-ttu-id="3c532-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c532-102">SYNOPSIS</span></span> 
<span data-ttu-id="3c532-103">Получение списка работоспособности подключения VPN-клиента к шлюзу виртуальной сети Azure для подключения VPN-клиента</span><span class="sxs-lookup"><span data-stu-id="3c532-103">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection</span></span>

## <span data-ttu-id="3c532-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c532-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId>
 [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="3c532-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c532-105">DESCRIPTION</span></span>
<span data-ttu-id="3c532-106">Список всех подключенных подключений VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="3c532-106">List  all connected vpn client connection health.</span></span> <span data-ttu-id="3c532-107">Сюда относятся: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span><span class="sxs-lookup"><span data-stu-id="3c532-107">This includes: vpnConnectionId vpnConnectionDuration vpnConnectionTime publicIpAddress privateIpAddress vpnUserName maxBandwidth egressPacketsTransferred egressBytesTransferred ingressPacketsTransferred ingressBytesTransferred maxPacketsPerSecond</span></span>

## <span data-ttu-id="3c532-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c532-108">EXAMPLES</span></span>

### <span data-ttu-id="3c532-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c532-109">Example 1</span></span>
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

<span data-ttu-id="3c532-110">Для шлюза виртуальной сети Azure с именем gatewayname в группе ресурсов "resourceGroup" выберите подключение VPN-клиента, подключенное в настоящее время с помощью OpenVpn.</span><span class="sxs-lookup"><span data-stu-id="3c532-110">For the Azure virtual network gateway named gatewayname in resource group resourceGroup, retrieves the currently connected vpn client connection by using OpenVpn.</span></span> 

### <span data-ttu-id="3c532-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3c532-111">Example 2</span></span>

<span data-ttu-id="3c532-112">Получение списка работоспособности подключения VPN-клиента к шлюзу виртуальной сети Azure для подключения VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="3c532-112">Get the list of vpn client connection health of an Azure virtual network gateway for per vpn client connection.</span></span> <span data-ttu-id="3c532-113">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="3c532-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzVirtualNetworkGatewayVpnClientConnectionHealth -ResourceGroupName resourceGroup -VirtualNetworkGatewayName 'ContosoVirtualNetwork'
```

## <span data-ttu-id="3c532-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c532-114">PARAMETERS</span></span>

### <span data-ttu-id="3c532-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c532-115">-ResourceGroupName</span></span>
<span data-ttu-id="3c532-116">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3c532-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="3c532-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3c532-117">-ResourceName</span></span>
<span data-ttu-id="3c532-118">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3c532-118">Virtual network gateway name</span></span>

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
### <span data-ttu-id="3c532-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c532-119">-ResourceId</span></span>
<span data-ttu-id="3c532-120">Идентификатор ресурса шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3c532-120">Virtual network gateway resource Id</span></span>

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

### <span data-ttu-id="3c532-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c532-121">-InputObject</span></span>
<span data-ttu-id="3c532-122">Объект шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3c532-122">Virtual network gateway object</span></span>

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

### <span data-ttu-id="3c532-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c532-123">-AsJob</span></span>
<span data-ttu-id="3c532-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3c532-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c532-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c532-125">CommonParameters</span></span>
<span data-ttu-id="3c532-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c532-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c532-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c532-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c532-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c532-128">INPUTS</span></span>

### <span data-ttu-id="3c532-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3c532-129">System.String</span></span>

## <span data-ttu-id="3c532-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c532-130">OUTPUTS</span></span>

### <span data-ttu-id="3c532-131">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="3c532-131">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="3c532-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c532-132">NOTES</span></span>

## <span data-ttu-id="3c532-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c532-133">RELATED LINKS</span></span>
