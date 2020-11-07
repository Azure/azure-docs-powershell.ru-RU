---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelinkconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLinkConnection.md
ms.openlocfilehash: e62e697deec0d7e3894e7eaf787790f64d72641b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903549"
---
# <span data-ttu-id="16ee8-101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="16ee8-101">New-AzVpnSiteLinkConnection</span></span>

## <span data-ttu-id="16ee8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="16ee8-103">Создает объект Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="16ee8-103">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="16ee8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16ee8-104">SYNTAX</span></span>

```
New-AzVpnSiteLinkConnection -Name <String> -VpnSiteLink <PSVpnSiteLink> [-SharedKey <SecureString>]
 [-ConnectionBandwidth <UInt32>] [-RoutingWeight <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ee8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16ee8-105">DESCRIPTION</span></span>
<span data-ttu-id="16ee8-106">Создает объект Azure VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="16ee8-106">Creates an Azure VpnSiteLinkConnection object.</span></span>

## <span data-ttu-id="16ee8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16ee8-107">EXAMPLES</span></span>

### <span data-ttu-id="16ee8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16ee8-108">Example 1</span></span>
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

<span data-ttu-id="16ee8-109">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite с 1 VpnSiteLinks (Западная часть США) в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="16ee8-109">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="16ee8-110">После этого на виртуальном концентраторе будет создан шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="16ee8-110">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="16ee8-111">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection с 1 VpnSiteLinkConnections VpnSiteLink VpnSite.</span><span class="sxs-lookup"><span data-stu-id="16ee8-111">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="16ee8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16ee8-112">PARAMETERS</span></span>

### <span data-ttu-id="16ee8-113">-ConnectionBandwidth</span><span class="sxs-lookup"><span data-stu-id="16ee8-113">-ConnectionBandwidth</span></span>
<span data-ttu-id="16ee8-114">Пропускная способность, которая должна быть обработана этим подключением для связи в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="16ee8-114">The bandwidth that needs to be handled by this link connection in mbps.</span></span>

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

### <span data-ttu-id="16ee8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ee8-115">-DefaultProfile</span></span>
<span data-ttu-id="16ee8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16ee8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ee8-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="16ee8-117">-EnableBgp</span></span>
<span data-ttu-id="16ee8-118">Включение BGP для этого подключения по ссылке</span><span class="sxs-lookup"><span data-stu-id="16ee8-118">Enable BGP for this link connection</span></span>

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

### <span data-ttu-id="16ee8-119">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="16ee8-119">-IpSecPolicy</span></span>
<span data-ttu-id="16ee8-120">Политика IpSec, которая будет учитываться при подключении по ссылке.</span><span class="sxs-lookup"><span data-stu-id="16ee8-120">IpSec Policy to be considered for this link connection.</span></span>

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

### <span data-ttu-id="16ee8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16ee8-121">-Name</span></span>
<span data-ttu-id="16ee8-122">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="16ee8-122">Name</span></span>

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

### <span data-ttu-id="16ee8-123">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="16ee8-123">-RoutingWeight</span></span>
<span data-ttu-id="16ee8-124">Вес маршрута</span><span class="sxs-lookup"><span data-stu-id="16ee8-124">Routing Weight</span></span>

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

### <span data-ttu-id="16ee8-125">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="16ee8-125">-SharedKey</span></span>
<span data-ttu-id="16ee8-126">Общий ключ, необходимый для настройки подключения к ссылке.</span><span class="sxs-lookup"><span data-stu-id="16ee8-126">The shared key required to set this link connection up.</span></span>

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

### <span data-ttu-id="16ee8-127">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="16ee8-127">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="16ee8-128">Использовать локальный IP-адрес Azure в качестве исходного IP-адреса для этого подключения ссылки.</span><span class="sxs-lookup"><span data-stu-id="16ee8-128">Use local azure ip address as source ip for this link connection.</span></span>

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

### <span data-ttu-id="16ee8-129">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="16ee8-129">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="16ee8-130">Использование селекторов трафика на основе политики для этого соединения по каналу.</span><span class="sxs-lookup"><span data-stu-id="16ee8-130">Use policy based traffic selectors for this link connection.</span></span>

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

### <span data-ttu-id="16ee8-131">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="16ee8-131">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="16ee8-132">Протокол подключения к шлюзу: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="16ee8-132">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="16ee8-133">-VpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="16ee8-133">-VpnSiteLink</span></span>
<span data-ttu-id="16ee8-134">Объект ссылки на VPN-сайт, к которому нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="16ee8-134">The vpn site link object to connect to.</span></span>

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

### <span data-ttu-id="16ee8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ee8-135">CommonParameters</span></span>
<span data-ttu-id="16ee8-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16ee8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ee8-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16ee8-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ee8-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16ee8-138">INPUTS</span></span>

### <span data-ttu-id="16ee8-139">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="16ee8-139">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="16ee8-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16ee8-140">OUTPUTS</span></span>

### <span data-ttu-id="16ee8-141">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="16ee8-141">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLinkConnection</span></span>

## <span data-ttu-id="16ee8-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="16ee8-142">NOTES</span></span>

## <span data-ttu-id="16ee8-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16ee8-143">RELATED LINKS</span></span>

[<span data-ttu-id="16ee8-144">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="16ee8-144">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)