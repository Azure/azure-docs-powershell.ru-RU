---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: a35f9b776bcd0f7fcb206103cd20475fb18bd608
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074511"
---
# <span data-ttu-id="c9e2f-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="c9e2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e2f-103">Обновляет VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="c9e2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9e2f-104">SYNTAX</span></span>

### <span data-ttu-id="c9e2f-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9e2f-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9e2f-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="c9e2f-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9e2f-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c9e2f-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9e2f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9e2f-108">DESCRIPTION</span></span>
<span data-ttu-id="c9e2f-109">Командлет **Update-AzVpnConnection** ОБНОВЛЯЕТ подключение VPN.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="c9e2f-110">VPN-подключение создает подключение IPsec, которое подключает VPN-шлюз к удаленной ветви клиента, представленной в Azure, в качестве VPN-сайта.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="c9e2f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9e2f-111">EXAMPLES</span></span>

### <span data-ttu-id="c9e2f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9e2f-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="c9e2f-113">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c9e2f-114">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c9e2f-115">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="c9e2f-116">После этого соединение обновится и появится новая IpSecPolicy с помощью команды Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="c9e2f-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c9e2f-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="c9e2f-118">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c9e2f-119">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="c9e2f-120">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="c9e2f-121">После этого соединение обновится, чтобы создать общий ключ с помощью безопасной конструкции строки.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="c9e2f-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9e2f-122">PARAMETERS</span></span>

### <span data-ttu-id="c9e2f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9e2f-123">-AsJob</span></span>
<span data-ttu-id="c9e2f-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c9e2f-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="c9e2f-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="c9e2f-126">Пропускная способность, которая должна быть обработана этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e2f-127">-DefaultProfile</span></span>
<span data-ttu-id="c9e2f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c9e2f-129">-EnableBgp</span></span>
<span data-ttu-id="c9e2f-130">Включение BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="c9e2f-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c9e2f-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="c9e2f-132">Включить Интернет-безопасность для этого подключения</span><span class="sxs-lookup"><span data-stu-id="c9e2f-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9e2f-133">-InputObject</span></span>
<span data-ttu-id="c9e2f-134">Объект VpnConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e2f-135">-IpSecPolicy</span></span>
<span data-ttu-id="c9e2f-136">Пропускная способность, которая должна быть обработана этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9e2f-137">-Name</span></span>
<span data-ttu-id="c9e2f-138">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c9e2f-139">-ParentResourceName</span></span>
<span data-ttu-id="c9e2f-140">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e2f-141">-ResourceGroupName</span></span>
<span data-ttu-id="c9e2f-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9e2f-143">-ResourceId</span></span>
<span data-ttu-id="c9e2f-144">Идентификатор ресурса объекта VpnConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-145">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="c9e2f-145">-SharedKey</span></span>
<span data-ttu-id="c9e2f-146">Общий ключ, необходимый для настройки этого подключения.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-146">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-147">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="c9e2f-147">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="c9e2f-148">Использовать локальный IP-адрес Azure в качестве исходного адреса при инициализации подключения.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-148">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-149">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="c9e2f-149">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="c9e2f-150">Использование селекторов трафика на основе политики для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-150">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-151">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-151">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="c9e2f-152">Список VpnSiteLinkConnections, который должен иметь этот VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-152">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9e2f-153">-Confirm</span></span>
<span data-ttu-id="c9e2f-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e2f-155">-WhatIf</span></span>
<span data-ttu-id="c9e2f-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9e2f-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9e2f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e2f-158">CommonParameters</span></span>
<span data-ttu-id="c9e2f-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9e2f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e2f-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9e2f-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e2f-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9e2f-161">INPUTS</span></span>

### <span data-ttu-id="c9e2f-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c9e2f-162">System.String</span></span>

### <span data-ttu-id="c9e2f-163">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-163">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c9e2f-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9e2f-164">OUTPUTS</span></span>

### <span data-ttu-id="c9e2f-165">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="c9e2f-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9e2f-166">NOTES</span></span>

## <span data-ttu-id="c9e2f-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9e2f-167">RELATED LINKS</span></span>

[<span data-ttu-id="c9e2f-168">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-168">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="c9e2f-169">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-169">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="c9e2f-170">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="c9e2f-170">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)
