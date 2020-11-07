---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnConnection.md
ms.openlocfilehash: 8b7d0845e6a8fce2d6c496573a493dfd187c34af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734339"
---
# <span data-ttu-id="5a6d6-101">New-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5a6d6-101">New-AzureRmVpnConnection</span></span>

## <span data-ttu-id="5a6d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6d6-103">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a6d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a6d6-104">SYNTAX</span></span>

### <span data-ttu-id="5a6d6-105">ByVpnGatewayNameByVpnSiteObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a6d6-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6d6-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5a6d6-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSiteId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6d6-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="5a6d6-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6d6-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5a6d6-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6d6-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="5a6d6-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6d6-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="5a6d6-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzureRmVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6d6-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a6d6-111">DESCRIPTION</span></span>
<span data-ttu-id="5a6d6-112">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="5a6d6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a6d6-113">EXAMPLES</span></span>

### <span data-ttu-id="5a6d6-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a6d6-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

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

<span data-ttu-id="5a6d6-115">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5a6d6-116">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5a6d6-117">После создания шлюза он подключается к VpnSite с помощью команды New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

## <span data-ttu-id="5a6d6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a6d6-118">PARAMETERS</span></span>

### <span data-ttu-id="5a6d6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a6d6-119">-AsJob</span></span>
<span data-ttu-id="5a6d6-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5a6d6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a6d6-121">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="5a6d6-121">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="5a6d6-122">Берем, который должен обрабатываться этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-122">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="5a6d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6d6-123">-DefaultProfile</span></span>
<span data-ttu-id="5a6d6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6d6-125">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5a6d6-125">-EnableBgp</span></span>
<span data-ttu-id="5a6d6-126">Включение BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="5a6d6-126">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="5a6d6-127">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6d6-127">-IpSecPolicy</span></span>
<span data-ttu-id="5a6d6-128">Берем, который должен обрабатываться этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-128">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="5a6d6-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a6d6-129">-Name</span></span>
<span data-ttu-id="5a6d6-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-130">The resource name.</span></span>

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

### <span data-ttu-id="5a6d6-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a6d6-131">-ParentObject</span></span>
<span data-ttu-id="5a6d6-132">Родительский VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-132">The parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="5a6d6-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5a6d6-133">-ParentResourceId</span></span>
<span data-ttu-id="5a6d6-134">Идентификатор ресурса родительского VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-134">The resource id of the parent VpnGateway for this connection.</span></span>

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

### <span data-ttu-id="5a6d6-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5a6d6-135">-ParentResourceName</span></span>
<span data-ttu-id="5a6d6-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-136">The resource group name.</span></span>

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

### <span data-ttu-id="5a6d6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6d6-137">-ResourceGroupName</span></span>
<span data-ttu-id="5a6d6-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-138">The resource group name.</span></span>

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

### <span data-ttu-id="5a6d6-139">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="5a6d6-139">-SharedKey</span></span>
<span data-ttu-id="5a6d6-140">Общий ключ, необходимый для настройки этого подключения.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-140">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="5a6d6-141">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="5a6d6-141">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="5a6d6-142">Протокол подключения к шлюзу: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="5a6d6-142">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="5a6d6-143">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5a6d6-143">-VpnSite</span></span>
<span data-ttu-id="5a6d6-144">Удаленный сайт VPN, к которому подключено данное виртуальное сетевое подключение к этому концентратору.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-144">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="5a6d6-145">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="5a6d6-145">-VpnSiteId</span></span>
<span data-ttu-id="5a6d6-146">Удаленный сайт VPN, к которому подключено данное виртуальное сетевое подключение к этому концентратору.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-146">The remote vpn site to which this hub virtual network connection is connected.</span></span>

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

### <span data-ttu-id="5a6d6-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a6d6-147">-Confirm</span></span>
<span data-ttu-id="5a6d6-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6d6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6d6-149">-WhatIf</span></span>
<span data-ttu-id="5a6d6-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6d6-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6d6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6d6-152">CommonParameters</span></span>
<span data-ttu-id="5a6d6-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a6d6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6d6-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a6d6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6d6-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a6d6-155">INPUTS</span></span>

### <span data-ttu-id="5a6d6-156">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="5a6d6-156">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="5a6d6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5a6d6-157">System.String</span></span>

## <span data-ttu-id="5a6d6-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a6d6-158">OUTPUTS</span></span>

### <span data-ttu-id="5a6d6-159">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5a6d6-159">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="5a6d6-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a6d6-160">NOTES</span></span>

## <span data-ttu-id="5a6d6-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a6d6-161">RELATED LINKS</span></span>
