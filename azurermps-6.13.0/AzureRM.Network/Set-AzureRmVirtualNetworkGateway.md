---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566437"
---
# <span data-ttu-id="cad4f-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="cad4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cad4f-102">SYNOPSIS</span></span>
<span data-ttu-id="cad4f-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cad4f-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cad4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cad4f-104">SYNTAX</span></span>

### <span data-ttu-id="cad4f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cad4f-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad4f-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cad4f-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad4f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cad4f-107">DESCRIPTION</span></span>
<span data-ttu-id="cad4f-108">Командлет **Set-AzureRmVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cad4f-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="cad4f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cad4f-109">EXAMPLES</span></span>

### <span data-ttu-id="cad4f-110">Пример 1: Установка состояния цели для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cad4f-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="cad4f-111">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда задает состояние цели для шлюза виртуальной сети, сохраненного в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="cad4f-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="cad4f-112">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="cad4f-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="cad4f-113">Пример 2: Установка состояния цели для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cad4f-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="cad4f-114">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда создает объект политики IP-безопасности VPN в соответствии с заданными параметрами IPsec.</span><span class="sxs-lookup"><span data-stu-id="cad4f-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="cad4f-115">Третья команда задает состояние цели для шлюза виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="cad4f-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="cad4f-116">Эта команда также задает настраиваемую политику IPSec для VPN, указанную в объекте $vpnclientipsecpolicy в шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cad4f-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="cad4f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cad4f-117">PARAMETERS</span></span>

### <span data-ttu-id="cad4f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cad4f-118">-AsJob</span></span>
<span data-ttu-id="cad4f-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cad4f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cad4f-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="cad4f-120">-Asn</span></span>
<span data-ttu-id="cad4f-121">Задает номер автономной системы шлюза виртуальной сети (ASN), который используется для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="cad4f-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad4f-122">-DefaultProfile</span></span>
<span data-ttu-id="cad4f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cad4f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cad4f-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="cad4f-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="cad4f-125">Отключение активного активного компонента.</span><span class="sxs-lookup"><span data-stu-id="cad4f-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="cad4f-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="cad4f-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="cad4f-127">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="cad4f-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="cad4f-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="cad4f-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="cad4f-129">Указывает сайт по умолчанию, который будет использоваться для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="cad4f-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="cad4f-130">Если указан сайт по умолчанию, весь Интернет-трафик от виртуальной частной сети (VPN) шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="cad4f-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="cad4f-131">-GatewaySku</span></span>
<span data-ttu-id="cad4f-132">Задает единицу хранения (SKU) шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cad4f-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="cad4f-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cad4f-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cad4f-134">Базового</span><span class="sxs-lookup"><span data-stu-id="cad4f-134">Basic</span></span>
- <span data-ttu-id="cad4f-135">Стандартная</span><span class="sxs-lookup"><span data-stu-id="cad4f-135">Standard</span></span>
- <span data-ttu-id="cad4f-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="cad4f-136">HighPerformance</span></span>
- <span data-ttu-id="cad4f-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="cad4f-137">VpnGw1</span></span>
- <span data-ttu-id="cad4f-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="cad4f-138">VpnGw2</span></span>
- <span data-ttu-id="cad4f-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="cad4f-139">VpnGw3</span></span>
- <span data-ttu-id="cad4f-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="cad4f-140">VpnGw1AZ</span></span>
- <span data-ttu-id="cad4f-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="cad4f-141">VpnGw2AZ</span></span>
- <span data-ttu-id="cad4f-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="cad4f-142">VpnGw3AZ</span></span>
- <span data-ttu-id="cad4f-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="cad4f-143">ErGw1AZ</span></span>
- <span data-ttu-id="cad4f-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="cad4f-144">ErGw2AZ</span></span>
- <span data-ttu-id="cad4f-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="cad4f-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="cad4f-146">-PeerWeight</span></span>
<span data-ttu-id="cad4f-147">Указывает вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cad4f-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="cad4f-148">-RadiusServerAddress</span></span>
<span data-ttu-id="cad4f-149">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="cad4f-149">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="cad4f-150">-RadiusServerSecret</span></span>
<span data-ttu-id="cad4f-151">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="cad4f-151">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="cad4f-153">Указывает объект шлюза виртуальной сети, для которого изменяются базовые изменения.</span><span class="sxs-lookup"><span data-stu-id="cad4f-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="cad4f-154">Вы можете использовать командлет Get-AzureRmVirtualNetworkGateway, чтобы получить объект шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cad4f-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="cad4f-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="cad4f-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="cad4f-156">Указывает адресное пространство, используемое этим командлетом для выделения IP-адресов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="cad4f-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="cad4f-157">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="cad4f-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="cad4f-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="cad4f-159">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="cad4f-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="cad4f-160">-VpnClientProtocol</span></span>
<span data-ttu-id="cad4f-161">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="cad4f-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="cad4f-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="cad4f-163">Указывает список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="cad4f-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="cad4f-164">VPN-клиент, выступающий сертификат, совпадающий с одним из них, удаляется.</span><span class="sxs-lookup"><span data-stu-id="cad4f-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="cad4f-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="cad4f-166">Указывает список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="cad4f-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="cad4f-167">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cad4f-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad4f-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cad4f-168">-Confirm</span></span>
<span data-ttu-id="cad4f-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cad4f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad4f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad4f-170">-WhatIf</span></span>
<span data-ttu-id="cad4f-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cad4f-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cad4f-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cad4f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad4f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad4f-173">CommonParameters</span></span>
<span data-ttu-id="cad4f-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cad4f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad4f-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cad4f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad4f-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cad4f-176">INPUTS</span></span>

### <span data-ttu-id="cad4f-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="cad4f-178">Параметры: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cad4f-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="cad4f-179">System. String</span><span class="sxs-lookup"><span data-stu-id="cad4f-179">System.String</span></span>

### <span data-ttu-id="cad4f-180">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="cad4f-181">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="cad4f-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="cad4f-182">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="cad4f-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cad4f-183">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="cad4f-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cad4f-184">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="cad4f-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cad4f-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="cad4f-185">System.UInt32</span></span>

### <span data-ttu-id="cad4f-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cad4f-186">System.Int32</span></span>

### <span data-ttu-id="cad4f-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="cad4f-187">System.Security.SecureString</span></span>

## <span data-ttu-id="cad4f-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cad4f-188">OUTPUTS</span></span>

### <span data-ttu-id="cad4f-189">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cad4f-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="cad4f-190">NOTES</span></span>
* <span data-ttu-id="cad4f-191">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="cad4f-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cad4f-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cad4f-192">RELATED LINKS</span></span>

[<span data-ttu-id="cad4f-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cad4f-194">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cad4f-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cad4f-196">Сброс — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cad4f-197">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cad4f-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


