---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVpnConnection.md
ms.openlocfilehash: 08b1e18fcd15dfb2667d0aec2410e7e0d7ea7b99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564196"
---
# <span data-ttu-id="5bdfe-101">Update-AzureRmVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5bdfe-101">Update-AzureRmVpnConnection</span></span>

## <span data-ttu-id="5bdfe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bdfe-102">SYNOPSIS</span></span>
<span data-ttu-id="5bdfe-103">Обновляет объект VpnConnection до состояния цели.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-103">Updates a VpnConnection object to a goal state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bdfe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bdfe-104">SYNTAX</span></span>

### <span data-ttu-id="5bdfe-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5bdfe-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzureRmVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bdfe-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdfe-106">ByVpnConnectionResourceId</span></span>
```
Update-AzureRmVpnConnection -ResourceId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bdfe-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="5bdfe-107">ByVpnConnectionObject</span></span>
```
Update-AzureRmVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bdfe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bdfe-108">DESCRIPTION</span></span>
<span data-ttu-id="5bdfe-109">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-109">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="5bdfe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bdfe-110">EXAMPLES</span></span>

### <span data-ttu-id="5bdfe-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5bdfe-111">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="5bdfe-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5bdfe-113">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5bdfe-114">После создания шлюза он подключается к VpnSite с помощью команды New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="5bdfe-115">После этого соединение обновится и появится новая IpSecPolicy с помощью команды Set-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-115">The connection is then updated to have a new IpSecPolicy by using the Set-AzureRmVpnConnection command.</span></span>

### <span data-ttu-id="5bdfe-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5bdfe-116">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzureRmVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
```

<span data-ttu-id="5bdfe-117">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="5bdfe-118">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="5bdfe-119">После создания шлюза он подключается к VpnSite с помощью команды New-AzureRmVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="5bdfe-120">После этого соединение обновится, чтобы создать общий ключ с помощью безопасной конструкции строки.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-120">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="5bdfe-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bdfe-121">PARAMETERS</span></span>

### <span data-ttu-id="5bdfe-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bdfe-122">-AsJob</span></span>
<span data-ttu-id="5bdfe-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5bdfe-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bdfe-124">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="5bdfe-124">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="5bdfe-125">Берем, который должен обрабатываться этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-125">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="5bdfe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bdfe-126">-DefaultProfile</span></span>
<span data-ttu-id="5bdfe-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bdfe-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5bdfe-128">-EnableBgp</span></span>
<span data-ttu-id="5bdfe-129">Включение BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="5bdfe-129">Enable BGP for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdfe-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bdfe-130">-InputObject</span></span>
<span data-ttu-id="5bdfe-131">Объект VpnConenction, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-131">The VpnConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdfe-132">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="5bdfe-132">-IpSecPolicy</span></span>
<span data-ttu-id="5bdfe-133">Берем, который должен обрабатываться этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-133">The bandwith that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="5bdfe-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5bdfe-134">-Name</span></span>
<span data-ttu-id="5bdfe-135">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-135">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdfe-136">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5bdfe-136">-ParentResourceName</span></span>
<span data-ttu-id="5bdfe-137">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-137">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdfe-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bdfe-138">-ResourceGroupName</span></span>
<span data-ttu-id="5bdfe-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bdfe-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bdfe-140">-ResourceId</span></span>
<span data-ttu-id="5bdfe-141">Идентификатор ресурса объекта VpnConenction, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-141">The resource id of the VpnConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bdfe-142">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="5bdfe-142">-SharedKey</span></span>
<span data-ttu-id="5bdfe-143">Общий ключ, необходимый для настройки этого подключения.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-143">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="5bdfe-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bdfe-144">-Confirm</span></span>
<span data-ttu-id="5bdfe-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bdfe-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bdfe-146">-WhatIf</span></span>
<span data-ttu-id="5bdfe-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bdfe-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bdfe-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bdfe-149">CommonParameters</span></span>
<span data-ttu-id="5bdfe-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bdfe-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bdfe-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bdfe-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bdfe-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bdfe-152">INPUTS</span></span>

### <span data-ttu-id="5bdfe-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5bdfe-153">System.String</span></span>

### <span data-ttu-id="5bdfe-154">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5bdfe-154">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="5bdfe-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bdfe-155">OUTPUTS</span></span>

### <span data-ttu-id="5bdfe-156">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5bdfe-156">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="5bdfe-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bdfe-157">NOTES</span></span>

## <span data-ttu-id="5bdfe-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bdfe-158">RELATED LINKS</span></span>
