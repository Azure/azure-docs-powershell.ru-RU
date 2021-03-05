---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4c1205599f048e33534f0ce0aa844da7b428b076
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011928"
---
# <span data-ttu-id="3435b-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3435b-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="3435b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3435b-102">SYNOPSIS</span></span>
<span data-ttu-id="3435b-103">Добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3435b-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="3435b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3435b-104">SYNTAX</span></span>

### <span data-ttu-id="3435b-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3435b-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="3435b-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="3435b-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3435b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3435b-108">DESCRIPTION</span></span>
<span data-ttu-id="3435b-109">Cmdlet **Add-AzExpressRouteCircuitPeeringConfig** добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3435b-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="3435b-110">С помощью каналов ExpressRoute ваша локальной сети подключается к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="3435b-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3435b-111">Обратите внимание, что после запуска **Add-AzExpressRouteCircuitPeeringConfig** необходимо вызвать Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3435b-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="3435b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3435b-112">EXAMPLES</span></span>

### <span data-ttu-id="3435b-113">Пример 1. Добавление одноранга в существующий канал ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3435b-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="3435b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3435b-114">PARAMETERS</span></span>

### <span data-ttu-id="3435b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3435b-115">-DefaultProfile</span></span>
<span data-ttu-id="3435b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3435b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3435b-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3435b-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="3435b-118">Канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3435b-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="3435b-119">Это объект Azure, возвращенный **cmdlet Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="3435b-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="3435b-120">-LegacyMode</span></span>
<span data-ttu-id="3435b-121">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="3435b-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="3435b-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="3435b-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="3435b-123">Для пиринга MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявлять в сеансе BGP.</span><span class="sxs-lookup"><span data-stu-id="3435b-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="3435b-124">Принимаются только префиксы общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3435b-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="3435b-125">Если вы планируете отправить набор префиксов, вы можете отправить список с разделительными запятами.</span><span class="sxs-lookup"><span data-stu-id="3435b-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="3435b-126">Эти префиксы должны быть зарегистрированы в имени реестра routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="3435b-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="3435b-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="3435b-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="3435b-128">Если вы рекламируете префиксы, которые не зарегистрированы для номера пиринга AS, вы можете указать номер AS, на который они зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="3435b-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="3435b-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="3435b-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="3435b-130">Имя реестра routing (RIR/IRR), на которое зарегистрировано число AS и префиксы.</span><span class="sxs-lookup"><span data-stu-id="3435b-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="3435b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="3435b-131">-Name</span></span>
<span data-ttu-id="3435b-132">Имя добавляемого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="3435b-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="3435b-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3435b-133">-PeerAddressType</span></span>
<span data-ttu-id="3435b-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="3435b-134">PeerAddressType</span></span>

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

### <span data-ttu-id="3435b-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="3435b-135">-PeerASN</span></span>
<span data-ttu-id="3435b-136">As number of your ExpressRoute circuit.</span><span class="sxs-lookup"><span data-stu-id="3435b-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="3435b-137">Это должен быть общедоступный ASN, если пирингОм является AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="3435b-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="3435b-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="3435b-138">-PeeringType</span></span>
<span data-ttu-id="3435b-139">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="3435b-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="3435b-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3435b-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="3435b-141">Это диапазон IP-адресов для основного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="3435b-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="3435b-142">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="3435b-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3435b-143">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3435b-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3435b-144">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="3435b-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3435b-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3435b-145">-RouteFilter</span></span>
<span data-ttu-id="3435b-146">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="3435b-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="3435b-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="3435b-147">-RouteFilterId</span></span>
<span data-ttu-id="3435b-148">Это ид ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="3435b-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="3435b-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3435b-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="3435b-150">Это диапазон IP-адресов для дополнительного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="3435b-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="3435b-151">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="3435b-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="3435b-152">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3435b-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="3435b-153">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="3435b-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="3435b-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="3435b-154">-SharedKey</span></span>
<span data-ttu-id="3435b-155">Это необязательный hash MD5, который используется в качестве преду общих ключей для конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="3435b-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="3435b-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="3435b-156">-VlanId</span></span>
<span data-ttu-id="3435b-157">Это ИД VLAN, назначенного для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="3435b-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="3435b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3435b-158">CommonParameters</span></span>
<span data-ttu-id="3435b-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3435b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3435b-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3435b-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3435b-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3435b-161">INPUTS</span></span>

### <span data-ttu-id="3435b-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3435b-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="3435b-163">System.String</span><span class="sxs-lookup"><span data-stu-id="3435b-163">System.String</span></span>

### <span data-ttu-id="3435b-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3435b-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="3435b-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3435b-165">System.Boolean</span></span>

## <span data-ttu-id="3435b-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3435b-166">OUTPUTS</span></span>

### <span data-ttu-id="3435b-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3435b-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3435b-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3435b-168">NOTES</span></span>

## <span data-ttu-id="3435b-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3435b-169">RELATED LINKS</span></span>

[<span data-ttu-id="3435b-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3435b-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3435b-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3435b-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3435b-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="3435b-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="3435b-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3435b-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
