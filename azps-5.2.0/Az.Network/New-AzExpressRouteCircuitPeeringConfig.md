---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5E9C02BE-9DCC-4865-95D2-6B69D373BE77
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 6561faf00104bf0892747ac97c09b5d8fc2c6f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407692"
---
# <span data-ttu-id="9a6fe-101">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="9a6fe-101">New-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="9a6fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6fe-103">Создает новую конфигурацию пиринга, которая будет добавлена в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-103">Creates a new peering configuration to be added to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="9a6fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a6fe-104">SYNTAX</span></span>

### <span data-ttu-id="9a6fe-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a6fe-105">SetByResource (Default)</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a6fe-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="9a6fe-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a6fe-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="9a6fe-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
New-AzExpressRouteCircuitPeeringConfig -Name <String> -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a6fe-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a6fe-108">DESCRIPTION</span></span>
<span data-ttu-id="9a6fe-109">Cmdlet **New-AzExpressRouteCircuitPeeringConfig** добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-109">The **New-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="9a6fe-110">С помощью каналов ExpressRoute ваша локальной сети подключается к Облаку Майкрософт с помощью поставщика услуг подключения, а не открытого Интернета.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span>

## <span data-ttu-id="9a6fe-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a6fe-111">EXAMPLES</span></span>

### <span data-ttu-id="9a6fe-112">Пример 1. Создание схемы ExpressRoute с конфигурацией пиринга</span><span class="sxs-lookup"><span data-stu-id="9a6fe-112">Example 1: Create a new ExpressRoute circuit with a peering configuration</span></span>
```powershell
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
$PeerConfig = New-AzExpressRouteCircuitPeeringConfig @parameters

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
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="9a6fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a6fe-113">PARAMETERS</span></span>

### <span data-ttu-id="9a6fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6fe-114">-DefaultProfile</span></span>
<span data-ttu-id="9a6fe-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a6fe-116">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="9a6fe-116">-LegacyMode</span></span>
<span data-ttu-id="9a6fe-117">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="9a6fe-117">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="9a6fe-118">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="9a6fe-118">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="9a6fe-119">Для peeringType microsoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявлять в сеансе BGP.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="9a6fe-120">Принимаются только префиксы общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="9a6fe-121">Если вы планируете отправить набор префиксов, вы можете отправить список с разделительными запятами.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="9a6fe-122">Эти префиксы должны быть зарегистрированы в имени реестра routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="9a6fe-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6fe-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="9a6fe-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="9a6fe-124">Если вы рекламируете префиксы, которые не зарегистрированы для номера пиринга AS, вы можете указать номер AS, на который они зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="9a6fe-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="9a6fe-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="9a6fe-126">Имя реестра routing (RIR/IRR), на которое зарегистрировано число AS и префиксы.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="9a6fe-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9a6fe-127">-Name</span></span>
<span data-ttu-id="9a6fe-128">Имя созда создаемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-128">The name of the peering configuration to be created.</span></span>

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

### <span data-ttu-id="9a6fe-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="9a6fe-129">-PeerAddressType</span></span>
<span data-ttu-id="9a6fe-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="9a6fe-130">PeerAddressType</span></span>

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

### <span data-ttu-id="9a6fe-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="9a6fe-131">-PeerASN</span></span>
<span data-ttu-id="9a6fe-132">As number of your ExpressRoute circuit.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-132">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="9a6fe-133">Это должен быть общедоступный ASN, если пирингОм является AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="9a6fe-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="9a6fe-134">-PeeringType</span></span>
<span data-ttu-id="9a6fe-135">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="9a6fe-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="9a6fe-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9a6fe-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="9a6fe-137">Это диапазон IP-адресов для основного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="9a6fe-138">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="9a6fe-139">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="9a6fe-140">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="9a6fe-141">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a6fe-141">-RouteFilter</span></span>
<span data-ttu-id="9a6fe-142">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-142">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="9a6fe-143">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="9a6fe-143">-RouteFilterId</span></span>
<span data-ttu-id="9a6fe-144">Это ид ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-144">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="9a6fe-145">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9a6fe-145">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="9a6fe-146">Это диапазон IP-адресов для дополнительного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-146">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="9a6fe-147">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-147">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="9a6fe-148">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-148">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="9a6fe-149">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-149">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="9a6fe-150">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9a6fe-150">-SharedKey</span></span>
<span data-ttu-id="9a6fe-151">Это необязательный hash MD5, который используется в качестве преду общих ключей для конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-151">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="9a6fe-152">-VlanId</span><span class="sxs-lookup"><span data-stu-id="9a6fe-152">-VlanId</span></span>
<span data-ttu-id="9a6fe-153">Это ИД VLAN, назначенного для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-153">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="9a6fe-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6fe-154">CommonParameters</span></span>
<span data-ttu-id="9a6fe-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a6fe-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6fe-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6fe-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6fe-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a6fe-157">INPUTS</span></span>

### <span data-ttu-id="9a6fe-158">System.String</span><span class="sxs-lookup"><span data-stu-id="9a6fe-158">System.String</span></span>

### <span data-ttu-id="9a6fe-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9a6fe-159">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="9a6fe-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a6fe-160">System.Boolean</span></span>

## <span data-ttu-id="9a6fe-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a6fe-161">OUTPUTS</span></span>

### <span data-ttu-id="9a6fe-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9a6fe-162">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="9a6fe-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a6fe-163">NOTES</span></span>

## <span data-ttu-id="9a6fe-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a6fe-164">RELATED LINKS</span></span>

[<span data-ttu-id="9a6fe-165">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="9a6fe-165">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="9a6fe-166">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9a6fe-166">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9a6fe-167">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="9a6fe-167">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="9a6fe-168">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9a6fe-168">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
