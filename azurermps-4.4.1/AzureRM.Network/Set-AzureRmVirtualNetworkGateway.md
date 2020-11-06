---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565222"
---
# <span data-ttu-id="3eb8a-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="3eb8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3eb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb8a-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3eb8a-104">SYNTAX</span></span>

### <span data-ttu-id="3eb8a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3eb8a-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb8a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eb8a-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb8a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eb8a-107">DESCRIPTION</span></span>
<span data-ttu-id="3eb8a-108">Командлет **Set-AzureRmVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="3eb8a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3eb8a-109">EXAMPLES</span></span>

### <span data-ttu-id="3eb8a-110">Пример 1: Установка состояния цели для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="3eb8a-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="3eb8a-111">Первая команда получает шлюз виртуальной сети с именем Gateway01, принадлежащий группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="3eb8a-112">Вторая команда задает состояние цели для шлюза виртуальной сети, сохраненного в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="3eb8a-113">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="3eb8a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3eb8a-114">PARAMETERS</span></span>

### <span data-ttu-id="3eb8a-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="3eb8a-115">-Asn</span></span>
<span data-ttu-id="3eb8a-116">Задает номер автономной системы шлюза виртуальной сети (ASN), который используется для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="3eb8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb8a-117">-DefaultProfile</span></span>
<span data-ttu-id="3eb8a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="3eb8a-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3eb8a-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="3eb8a-120">Отключение активного активного компонента.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-120">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="3eb8a-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="3eb8a-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="3eb8a-122">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-122">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="3eb8a-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="3eb8a-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="3eb8a-124">Указывает сайт по умолчанию, который будет использоваться для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="3eb8a-125">Если указан сайт по умолчанию, весь Интернет-трафик от виртуальной частной сети (VPN) шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="3eb8a-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="3eb8a-126">-GatewaySku</span></span>
<span data-ttu-id="3eb8a-127">Задает единицу хранения (SKU) шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="3eb8a-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3eb8a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3eb8a-129">Базового</span><span class="sxs-lookup"><span data-stu-id="3eb8a-129">Basic</span></span>
- <span data-ttu-id="3eb8a-130">Стандартная</span><span class="sxs-lookup"><span data-stu-id="3eb8a-130">Standard</span></span>
- <span data-ttu-id="3eb8a-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="3eb8a-131">HighPerformance</span></span>
- <span data-ttu-id="3eb8a-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="3eb8a-132">VpnGw1</span></span>
- <span data-ttu-id="3eb8a-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="3eb8a-133">VpnGw2</span></span>
- <span data-ttu-id="3eb8a-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="3eb8a-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb8a-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3eb8a-135">-PeerWeight</span></span>
<span data-ttu-id="3eb8a-136">Указывает вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="3eb8a-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="3eb8a-137">-RadiusServerAddress</span></span>
<span data-ttu-id="3eb8a-138">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-138">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="3eb8a-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="3eb8a-139">-RadiusServerSecret</span></span>
<span data-ttu-id="3eb8a-140">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-140">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="3eb8a-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="3eb8a-142">Указывает объект шлюза виртуальной сети, для которого изменяются базовые изменения.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="3eb8a-143">Вы можете использовать командлет Get-AzureRmVirtualNetworkGateway, чтобы получить объект шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="3eb8a-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="3eb8a-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="3eb8a-145">Указывает адресное пространство, используемое этим командлетом для выделения IP-адресов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="3eb8a-146">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="3eb8a-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="3eb8a-147">-VpnClientProtocol</span></span>
<span data-ttu-id="3eb8a-148">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="3eb8a-148">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb8a-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="3eb8a-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="3eb8a-150">Указывает список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="3eb8a-151">VPN-клиент, выступающий сертификат, совпадающий с одним из них, удаляется.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="3eb8a-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="3eb8a-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="3eb8a-153">Указывает список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="3eb8a-154">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="3eb8a-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eb8a-155">-Confirm</span></span>
<span data-ttu-id="3eb8a-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb8a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb8a-157">-WhatIf</span></span>
<span data-ttu-id="3eb8a-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3eb8a-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb8a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb8a-160">CommonParameters</span></span>
<span data-ttu-id="3eb8a-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb8a-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb8a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb8a-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3eb8a-163">INPUTS</span></span>

### <span data-ttu-id="3eb8a-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="3eb8a-165">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3eb8a-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="3eb8a-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eb8a-166">OUTPUTS</span></span>

### <span data-ttu-id="3eb8a-167">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="3eb8a-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="3eb8a-168">NOTES</span></span>
* <span data-ttu-id="3eb8a-169">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="3eb8a-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3eb8a-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3eb8a-170">RELATED LINKS</span></span>

[<span data-ttu-id="3eb8a-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3eb8a-172">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3eb8a-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3eb8a-174">Сброс — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="3eb8a-175">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3eb8a-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


