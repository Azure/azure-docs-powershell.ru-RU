---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 750af3bf948345a22c7cb7a86b09e07d4e266f9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730242"
---
# <span data-ttu-id="21c90-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="21c90-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="21c90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21c90-102">SYNOPSIS</span></span>
<span data-ttu-id="21c90-103">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="21c90-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="21c90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21c90-104">SYNTAX</span></span>

### <span data-ttu-id="21c90-105">ByVpnGatewayNameByVpnSiteObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21c90-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c90-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="21c90-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c90-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="21c90-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c90-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="21c90-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c90-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="21c90-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c90-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="21c90-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c90-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21c90-111">DESCRIPTION</span></span>
<span data-ttu-id="21c90-112">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="21c90-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="21c90-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21c90-113">EXAMPLES</span></span>

### <span data-ttu-id="21c90-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21c90-114">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

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
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="21c90-115">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="21c90-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="21c90-116">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="21c90-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="21c90-117">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="21c90-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

## <span data-ttu-id="21c90-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21c90-118">PARAMETERS</span></span>

### <span data-ttu-id="21c90-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21c90-119">-AsJob</span></span>
<span data-ttu-id="21c90-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="21c90-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21c90-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="21c90-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="21c90-122">Берем, который должен обрабатываться этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="21c90-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="21c90-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c90-123">-DefaultProfile</span></span>
<span data-ttu-id="21c90-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21c90-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c90-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="21c90-125">-EnableBgp</span></span>
<span data-ttu-id="21c90-126">Включение BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="21c90-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="21c90-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="21c90-127">-IpSecPolicy</span></span>
<span data-ttu-id="21c90-128">Берем, который должен обрабатываться этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="21c90-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="21c90-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21c90-129">-Name</span></span>
<span data-ttu-id="21c90-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="21c90-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="21c90-131">-ParentObject</span></span>
<span data-ttu-id="21c90-132">Родительский VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="21c90-132">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="21c90-133">-ParentResourceId</span></span>
<span data-ttu-id="21c90-134">Идентификатор ресурса родительского VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="21c90-134">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="21c90-135">-ParentResourceName</span></span>
<span data-ttu-id="21c90-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21c90-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c90-137">-ResourceGroupName</span></span>
<span data-ttu-id="21c90-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21c90-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="21c90-139">-SharedKey</span></span>
<span data-ttu-id="21c90-140">Общий ключ, необходимый для настройки этого подключения.</span><span class="sxs-lookup"><span data-stu-id="21c90-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="21c90-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="21c90-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="21c90-142">Протокол подключения к шлюзу: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="21c90-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="21c90-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="21c90-143">-VpnSite</span></span>
<span data-ttu-id="21c90-144">Удаленный сайт VPN, к которому подключено данное виртуальное сетевое подключение к этому концентратору.</span><span class="sxs-lookup"><span data-stu-id="21c90-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="21c90-145">-VpnSiteId</span></span>
<span data-ttu-id="21c90-146">Удаленный сайт VPN, к которому подключено данное виртуальное сетевое подключение к этому концентратору.</span><span class="sxs-lookup"><span data-stu-id="21c90-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21c90-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21c90-147">-Confirm</span></span>
<span data-ttu-id="21c90-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21c90-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c90-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c90-149">-WhatIf</span></span>
<span data-ttu-id="21c90-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21c90-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c90-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21c90-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c90-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c90-152">CommonParameters</span></span>
<span data-ttu-id="21c90-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21c90-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c90-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c90-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c90-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21c90-155">INPUTS</span></span>

### <span data-ttu-id="21c90-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="21c90-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="21c90-157">System. String</span><span class="sxs-lookup"><span data-stu-id="21c90-157">System.String</span></span>

## <span data-ttu-id="21c90-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21c90-158">OUTPUTS</span></span>

### <span data-ttu-id="21c90-159">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="21c90-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="21c90-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="21c90-160">NOTES</span></span>

## <span data-ttu-id="21c90-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21c90-161">RELATED LINKS</span></span>

[<span data-ttu-id="21c90-162">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="21c90-162">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="21c90-163">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="21c90-163">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="21c90-164">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="21c90-164">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
