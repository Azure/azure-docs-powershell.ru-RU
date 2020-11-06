---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 8471ccd34ab5d13ad5012e9a2e29892659c297f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562892"
---
# <span data-ttu-id="7e647-101">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7e647-101">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="7e647-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e647-102">SYNOPSIS</span></span>
<span data-ttu-id="7e647-103">Создает новую конфигурацию пиринга, которую нужно добавить в цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e647-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e647-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e647-104">SYNTAX</span></span>

### <span data-ttu-id="7e647-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e647-105">SetByResource (Default)</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e647-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="7e647-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e647-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="7e647-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e647-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e647-108">DESCRIPTION</span></span>
<span data-ttu-id="7e647-109">Командлет **New-AzureRmExpressRouteCircuitPeeringConfig** добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e647-109">The **New-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="7e647-110">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="7e647-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="7e647-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e647-111">EXAMPLES</span></span>

### <span data-ttu-id="7e647-112">Пример 1: создание новой цепи ExpressRoute с помощью конфигурации пиринга</span><span class="sxs-lookup"><span data-stu-id="7e647-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzureRmExpressRouteCircuitPeeringConfig @parameters

$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    Peering=$PeerConfig
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="7e647-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e647-113">PARAMETERS</span></span>

### <span data-ttu-id="7e647-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e647-114">-DefaultProfile</span></span>
<span data-ttu-id="7e647-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e647-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e647-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="7e647-116">-LegacyMode</span></span>
<span data-ttu-id="7e647-117">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="7e647-117">The legacy mode of the Peering</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="7e647-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="7e647-119">Для PeeringType MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявить для сеанса BGP.</span><span class="sxs-lookup"><span data-stu-id="7e647-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="7e647-120">Принимаются только префиксы общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7e647-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="7e647-121">Вы можете отправить список с разделителями-запятыми, если вы собираетесь отправить набор префиксов.</span><span class="sxs-lookup"><span data-stu-id="7e647-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="7e647-122">Эти префиксы должны быть зарегистрированы в названии реестра маршрутизации (RIR/ВСД).</span><span class="sxs-lookup"><span data-stu-id="7e647-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="7e647-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="7e647-124">Если вы используете префиксы для рекламы, которые не зарегистрированы в качестве номера, вы можете указать номер, по которому они будут зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="7e647-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="7e647-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="7e647-126">Имя реестра маршрутизации (RIR/ВСД), для которого зарегистрированы номера и префиксы.</span><span class="sxs-lookup"><span data-stu-id="7e647-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e647-127">-Name</span></span>
<span data-ttu-id="7e647-128">Имя конфигурации пиринга, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="7e647-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="7e647-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7e647-129">-PeerAddressType</span></span>
<span data-ttu-id="7e647-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="7e647-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="7e647-131">-PeerASN</span></span>
<span data-ttu-id="7e647-132">Число в канале ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7e647-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="7e647-133">Это значение должно быть общедоступным ASN, когда PeeringType — AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="7e647-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7e647-134">-PeeringType</span></span>
<span data-ttu-id="7e647-135">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7e647-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7e647-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="7e647-137">Это диапазон IP-адресов для основного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="7e647-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="7e647-138">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="7e647-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7e647-139">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="7e647-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7e647-140">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="7e647-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7e647-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e647-141">-RouteFilter</span></span>
<span data-ttu-id="7e647-142">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="7e647-142">This is an existing RouteFilter object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="7e647-143">-RouteFilterId</span></span>
<span data-ttu-id="7e647-144">Это идентификатор ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="7e647-144">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7e647-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="7e647-146">Это диапазон IP-адресов для дополнительного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="7e647-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="7e647-147">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="7e647-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="7e647-148">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="7e647-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="7e647-149">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="7e647-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="7e647-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="7e647-150">-SharedKey</span></span>
<span data-ttu-id="7e647-151">Это необязательный хэш MD5, используемый в качестве предварительно общего ключа для настройки пиринга.</span><span class="sxs-lookup"><span data-stu-id="7e647-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="7e647-152">-VlanId</span></span>
<span data-ttu-id="7e647-153">Это идентификационный номер VLAN, назначенный для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="7e647-153">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e647-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e647-154">CommonParameters</span></span>
<span data-ttu-id="7e647-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e647-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e647-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e647-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e647-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e647-157">INPUTS</span></span>

### <span data-ttu-id="7e647-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7e647-158">System.String</span></span>

### <span data-ttu-id="7e647-159">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7e647-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="7e647-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e647-160">System.Boolean</span></span>

## <span data-ttu-id="7e647-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e647-161">OUTPUTS</span></span>

### <span data-ttu-id="7e647-162">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="7e647-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="7e647-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e647-163">NOTES</span></span>

## <span data-ttu-id="7e647-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e647-164">RELATED LINKS</span></span>

[<span data-ttu-id="7e647-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7e647-165">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7e647-166">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e647-166">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7e647-167">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7e647-167">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7e647-168">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7e647-168">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
