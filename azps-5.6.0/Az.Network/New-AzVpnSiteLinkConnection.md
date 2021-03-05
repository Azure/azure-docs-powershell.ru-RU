---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: 4f61bce910a2dc0f2b177423a5dc199103da378d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984307"
---
# <span data-ttu-id="24c1c-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="24c1c-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="24c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="24c1c-103">Создает объект Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="24c1c-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="24c1c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24c1c-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-IngressNatRule <PSResourceId[]>] [-EgressNatRule <PSResourceId[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c1c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="24c1c-106">Создает объект Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="24c1c-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="24c1c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="24c1c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24c1c-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)


PS C:\> $vpnSiteLinkConnection = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection)
```

<span data-ttu-id="24c1c-109">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора и VPNSite с 1 VpnSiteLinks на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="24c1c-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="24c1c-110">После этого в виртуальном центре будет создан VPN-шлюз.</span><span class="sxs-lookup"><span data-stu-id="24c1c-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="24c1c-111">После создания шлюз подключается к VPNSite с помощью команды New-AzVpnConnection 1 VpnSiteLinkConnections к VPNSiteLink.</span><span class="sxs-lookup"><span data-stu-id="24c1c-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="24c1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24c1c-112">PARAMETERS</span></span>

### <span data-ttu-id="24c1c-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="24c1c-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="24c1c-114">Пропускная способность, которая должна обрабатываться этим подключением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="24c1c-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="24c1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c1c-115">-DefaultProfile</span></span>
<span data-ttu-id="24c1c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24c1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24c1c-117">-EgressNatRule</span><span class="sxs-lookup"><span data-stu-id="24c1c-117">-EgressNatRule</span></span>
<span data-ttu-id="24c1c-118">Список правил NAT на регрессии, связанных с этой ссылкой Connection.</span><span class="sxs-lookup"><span data-stu-id="24c1c-118">The list of egress  NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c1c-119">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="24c1c-119">-EnableBgp</span></span>
<span data-ttu-id="24c1c-120">Включить BGP для этого подключения к ссылке</span><span class="sxs-lookup"><span data-stu-id="24c1c-120">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="24c1c-121">-IngressNatRule</span><span class="sxs-lookup"><span data-stu-id="24c1c-121">-IngressNatRule</span></span>
<span data-ttu-id="24c1c-122">Список правил NAT для регрессии, связанных с этой ссылкой Connection.</span><span class="sxs-lookup"><span data-stu-id="24c1c-122">The list of ingress NAT rules that are associated with this link Connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c1c-123">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="24c1c-123">-IpSecPolicy</span></span>
<span data-ttu-id="24c1c-124">Политика IpSec, которая будет рассматриваться для этого подключения к ссылке.</span><span class="sxs-lookup"><span data-stu-id="24c1c-124">IpSec Policy to be considered for this link connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c1c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="24c1c-125">-Name</span></span>
<span data-ttu-id="24c1c-126">Имя</span><span class="sxs-lookup"><span data-stu-id="24c1c-126">Name</span></span>

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

### <span data-ttu-id="24c1c-127">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="24c1c-127">-RoutingWeight</span></span>
<span data-ttu-id="24c1c-128">Routing Weight</span><span class="sxs-lookup"><span data-stu-id="24c1c-128">Routing Weight</span></span>

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

### <span data-ttu-id="24c1c-129">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="24c1c-129">-SharedKey</span></span>
<span data-ttu-id="24c1c-130">Общий ключ, необходимый для подключения к этой ссылке.</span><span class="sxs-lookup"><span data-stu-id="24c1c-130">The shared key required to set this link connection up.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c1c-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="24c1c-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="24c1c-132">Используйте локальный IP-адрес Azure в качестве ip-адреса источника для этого подключения к ссылке.</span><span class="sxs-lookup"><span data-stu-id="24c1c-132">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="24c1c-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="24c1c-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="24c1c-134">Используйте селекторы трафика, основанные на политике, для этого подключения к ссылке.</span><span class="sxs-lookup"><span data-stu-id="24c1c-134">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="24c1c-135">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="24c1c-135">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="24c1c-136">Протокол подключения шлюза:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="24c1c-136">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c1c-137">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="24c1c-137">-VpnSiteLink</span></span>
<span data-ttu-id="24c1c-138">Объект VPN-ссылка для подключения.</span><span class="sxs-lookup"><span data-stu-id="24c1c-138">The vpn site link object to connect to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c1c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c1c-139">CommonParameters</span></span>
<span data-ttu-id="24c1c-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c1c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c1c-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24c1c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c1c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24c1c-142">INPUTS</span></span>

### <span data-ttu-id="24c1c-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="24c1c-143">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="24c1c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24c1c-144">OUTPUTS</span></span>

### <span data-ttu-id="24c1c-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="24c1c-145">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="24c1c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24c1c-146">NOTES</span></span>

## <span data-ttu-id="24c1c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24c1c-147">RELATED LINKS</span></span>

[<span data-ttu-id="24c1c-148">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="24c1c-148">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)