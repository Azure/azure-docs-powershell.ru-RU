---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729962"
---
# <span data-ttu-id="1a453-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="1a453-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a453-102">SYNOPSIS</span></span>
<span data-ttu-id="1a453-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a453-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="1a453-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a453-104">SYNTAX</span></span>

### <span data-ttu-id="1a453-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a453-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a453-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a453-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a453-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a453-107">DESCRIPTION</span></span>
<span data-ttu-id="1a453-108">Командлет **Set-AzVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a453-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="1a453-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a453-109">EXAMPLES</span></span>

### <span data-ttu-id="1a453-110">Пример 1: обновление ASN для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="1a453-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="1a453-111">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="1a453-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="1a453-112">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="1a453-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="1a453-113">Пример 2: Добавление политики IPsec к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="1a453-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="1a453-114">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда создает объект политики IP-безопасности VPN в соответствии с заданными параметрами IPsec.</span><span class="sxs-lookup"><span data-stu-id="1a453-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="1a453-115">Третья команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="1a453-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="1a453-116">Эта команда также задает настраиваемую политику IPSec для VPN, указанную в объекте $vpnclientipsecpolicy в шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a453-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="1a453-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a453-117">PARAMETERS</span></span>

### <span data-ttu-id="1a453-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a453-118">-AsJob</span></span>
<span data-ttu-id="1a453-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1a453-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a453-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="1a453-120">-Asn</span></span>
<span data-ttu-id="1a453-121">Задает номер автономной системы шлюза виртуальной сети (ASN), который используется для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="1a453-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="1a453-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a453-122">-DefaultProfile</span></span>
<span data-ttu-id="1a453-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a453-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a453-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1a453-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="1a453-125">Отключение активного активного компонента.</span><span class="sxs-lookup"><span data-stu-id="1a453-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="1a453-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1a453-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="1a453-127">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="1a453-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="1a453-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1a453-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="1a453-129">Указывает сайт по умолчанию, который будет использоваться для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="1a453-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="1a453-130">Если указан сайт по умолчанию, весь Интернет-трафик от виртуальной частной сети (VPN) шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="1a453-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="1a453-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="1a453-131">-GatewaySku</span></span>
<span data-ttu-id="1a453-132">Задает единицу хранения (SKU) шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a453-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="1a453-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1a453-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a453-134">Базового</span><span class="sxs-lookup"><span data-stu-id="1a453-134">Basic</span></span>
- <span data-ttu-id="1a453-135">Стандартная</span><span class="sxs-lookup"><span data-stu-id="1a453-135">Standard</span></span>
- <span data-ttu-id="1a453-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="1a453-136">HighPerformance</span></span>
- <span data-ttu-id="1a453-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="1a453-137">VpnGw1</span></span>
- <span data-ttu-id="1a453-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="1a453-138">VpnGw2</span></span>
- <span data-ttu-id="1a453-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="1a453-139">VpnGw3</span></span>
- <span data-ttu-id="1a453-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="1a453-140">VpnGw1AZ</span></span>
- <span data-ttu-id="1a453-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="1a453-141">VpnGw2AZ</span></span>
- <span data-ttu-id="1a453-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="1a453-142">VpnGw3AZ</span></span>
- <span data-ttu-id="1a453-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="1a453-143">ErGw1AZ</span></span>
- <span data-ttu-id="1a453-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="1a453-144">ErGw2AZ</span></span>
- <span data-ttu-id="1a453-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="1a453-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="1a453-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1a453-146">-PeerWeight</span></span>
<span data-ttu-id="1a453-147">Указывает вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a453-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="1a453-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1a453-148">-RadiusServerAddress</span></span>
<span data-ttu-id="1a453-149">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="1a453-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="1a453-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1a453-150">-RadiusServerSecret</span></span>
<span data-ttu-id="1a453-151">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="1a453-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="1a453-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1a453-153">Указывает объект шлюза виртуальной сети, для которого изменяются базовые изменения.</span><span class="sxs-lookup"><span data-stu-id="1a453-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="1a453-154">Вы можете использовать командлет Get-AzVirtualNetworkGateway, чтобы получить объект шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1a453-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="1a453-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="1a453-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="1a453-156">Указывает адресное пространство, используемое этим командлетом для выделения IP-адресов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="1a453-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="1a453-157">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="1a453-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a453-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1a453-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="1a453-159">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="1a453-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a453-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1a453-160">-VpnClientProtocol</span></span>
<span data-ttu-id="1a453-161">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="1a453-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a453-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="1a453-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="1a453-163">Указывает список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="1a453-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="1a453-164">VPN-клиент, выступающий сертификат, совпадающий с одним из них, удаляется.</span><span class="sxs-lookup"><span data-stu-id="1a453-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a453-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="1a453-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="1a453-166">Указывает список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="1a453-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="1a453-167">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1a453-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a453-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a453-168">-Confirm</span></span>
<span data-ttu-id="1a453-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a453-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a453-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a453-170">-WhatIf</span></span>
<span data-ttu-id="1a453-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a453-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a453-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a453-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a453-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a453-173">CommonParameters</span></span>
<span data-ttu-id="1a453-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a453-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a453-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a453-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a453-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a453-176">INPUTS</span></span>

### <span data-ttu-id="1a453-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1a453-178">System. String</span><span class="sxs-lookup"><span data-stu-id="1a453-178">System.String</span></span>

### <span data-ttu-id="1a453-179">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="1a453-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="1a453-180">System.String[]</span></span>

### <span data-ttu-id="1a453-181">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="1a453-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="1a453-182">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="1a453-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="1a453-183">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="1a453-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="1a453-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1a453-184">System.UInt32</span></span>

### <span data-ttu-id="1a453-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1a453-185">System.Int32</span></span>

### <span data-ttu-id="1a453-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1a453-186">System.Security.SecureString</span></span>

## <span data-ttu-id="1a453-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a453-187">OUTPUTS</span></span>

### <span data-ttu-id="1a453-188">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1a453-189">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a453-189">NOTES</span></span>
* <span data-ttu-id="1a453-190">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="1a453-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1a453-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a453-191">RELATED LINKS</span></span>

[<span data-ttu-id="1a453-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1a453-193">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1a453-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1a453-195">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1a453-196">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1a453-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
