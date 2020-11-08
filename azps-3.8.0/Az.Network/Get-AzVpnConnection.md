---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: c52aec45b71510c508ad56359b0ea87c98bef4dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074859"
---
# <span data-ttu-id="88694-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88694-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="88694-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88694-102">SYNOPSIS</span></span>
<span data-ttu-id="88694-103">Возвращает VPN-подключение по имени или список всех VPN-подключений, подключенных к VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="88694-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="88694-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88694-104">SYNTAX</span></span>

### <span data-ttu-id="88694-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88694-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88694-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="88694-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88694-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="88694-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88694-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88694-108">DESCRIPTION</span></span>
<span data-ttu-id="88694-109">Возвращает VPN-подключение по имени или список всех VPN-подключений, подключенных к VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="88694-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="88694-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88694-110">EXAMPLES</span></span>

### <span data-ttu-id="88694-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88694-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="88694-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="88694-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="88694-113">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="88694-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="88694-114">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="88694-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="88694-115">Затем он получает подключение, используя имя подключения.</span><span class="sxs-lookup"><span data-stu-id="88694-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="88694-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88694-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
```

<span data-ttu-id="88694-117">Этот командлет получает все подключения, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="88694-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="88694-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88694-118">PARAMETERS</span></span>

### <span data-ttu-id="88694-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88694-119">-DefaultProfile</span></span>
<span data-ttu-id="88694-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88694-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88694-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88694-121">-Name</span></span>
<span data-ttu-id="88694-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="88694-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88694-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="88694-123">-ParentObject</span></span>
<span data-ttu-id="88694-124">Родительский VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="88694-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88694-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="88694-125">-ParentResourceId</span></span>
<span data-ttu-id="88694-126">Идентификатор ресурса родительского VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="88694-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88694-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="88694-127">-ParentResourceName</span></span>
<span data-ttu-id="88694-128">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="88694-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88694-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88694-129">-ResourceGroupName</span></span>
<span data-ttu-id="88694-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88694-130">The resource group name.</span></span>

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

### <span data-ttu-id="88694-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88694-131">CommonParameters</span></span>
<span data-ttu-id="88694-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88694-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88694-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88694-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88694-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88694-134">INPUTS</span></span>

### <span data-ttu-id="88694-135">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="88694-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="88694-136">System. String</span><span class="sxs-lookup"><span data-stu-id="88694-136">System.String</span></span>

## <span data-ttu-id="88694-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88694-137">OUTPUTS</span></span>

### <span data-ttu-id="88694-138">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88694-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="88694-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="88694-139">NOTES</span></span>

## <span data-ttu-id="88694-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88694-140">RELATED LINKS</span></span>

[<span data-ttu-id="88694-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88694-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="88694-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88694-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="88694-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="88694-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
