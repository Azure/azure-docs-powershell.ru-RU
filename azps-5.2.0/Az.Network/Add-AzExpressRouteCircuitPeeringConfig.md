---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407940"
---
# <span data-ttu-id="1456f-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1456f-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1456f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1456f-102">SYNOPSIS</span></span>
<span data-ttu-id="1456f-103">Добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1456f-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1456f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1456f-104">SYNTAX</span></span>

### <span data-ttu-id="1456f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1456f-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1456f-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="1456f-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1456f-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="1456f-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1456f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1456f-108">DESCRIPTION</span></span>
<span data-ttu-id="1456f-109">Cmdlet **Add-AzExpressRouteCircuitPeeringConfig** добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1456f-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="1456f-110">Схемы ExpressRoute подключают вашу локальное сеть к Microsoft Cloud с помощью поставщика услуг подключения, а не через общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="1456f-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="1456f-111">Обратите внимание, что после запуска **Add-AzExpressRouteCircuitPeeringConfig** необходимо вызвать Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1456f-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="1456f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1456f-112">EXAMPLES</span></span>

### <span data-ttu-id="1456f-113">Пример 1. Добавление одноранга в существующий канал ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1456f-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="1456f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1456f-114">PARAMETERS</span></span>

### <span data-ttu-id="1456f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1456f-115">-DefaultProfile</span></span>
<span data-ttu-id="1456f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1456f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1456f-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1456f-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1456f-118">Канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1456f-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="1456f-119">Это объект Azure, возвращенный **cmdlet Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="1456f-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="1456f-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="1456f-120">-LegacyMode</span></span>
<span data-ttu-id="1456f-121">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="1456f-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="1456f-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="1456f-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="1456f-123">Для пиринга MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявлять в сеансе BGP.</span><span class="sxs-lookup"><span data-stu-id="1456f-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="1456f-124">Принимаются только префиксы общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="1456f-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="1456f-125">Если вы планируете отправить набор префиксов, вы можете отправить список с разделительными запятами.</span><span class="sxs-lookup"><span data-stu-id="1456f-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="1456f-126">Эти префиксы должны быть зарегистрированы в имени реестра routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="1456f-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="1456f-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="1456f-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="1456f-128">Если вы рекламируете префиксы, которые не зарегистрированы для номера пиринга AS, вы можете указать номер AS, на который они зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="1456f-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="1456f-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="1456f-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="1456f-130">Имя реестра routing (RIR/IRR), на которое зарегистрировано число AS и префиксы.</span><span class="sxs-lookup"><span data-stu-id="1456f-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="1456f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1456f-131">-Name</span></span>
<span data-ttu-id="1456f-132">Имя добавляемого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="1456f-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="1456f-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1456f-133">-PeerAddressType</span></span>
<span data-ttu-id="1456f-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1456f-134">PeerAddressType</span></span>

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

### <span data-ttu-id="1456f-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="1456f-135">-PeerASN</span></span>
<span data-ttu-id="1456f-136">As number of your ExpressRoute circuit.</span><span class="sxs-lookup"><span data-stu-id="1456f-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="1456f-137">Это должен быть общедоступный ASN, если пирингОм является AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="1456f-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="1456f-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1456f-138">-PeeringType</span></span>
<span data-ttu-id="1456f-139">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1456f-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1456f-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1456f-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="1456f-141">Это диапазон IP-адресов для основного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="1456f-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="1456f-142">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="1456f-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1456f-143">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="1456f-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1456f-144">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="1456f-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="1456f-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1456f-145">-RouteFilter</span></span>
<span data-ttu-id="1456f-146">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1456f-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="1456f-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="1456f-147">-RouteFilterId</span></span>
<span data-ttu-id="1456f-148">Это ид ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1456f-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="1456f-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1456f-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="1456f-150">Это диапазон IP-адресов для дополнительного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="1456f-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="1456f-151">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="1456f-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1456f-152">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="1456f-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1456f-153">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="1456f-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="1456f-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1456f-154">-SharedKey</span></span>
<span data-ttu-id="1456f-155">Это необязательный hash MD5, который используется в качестве преду общих ключей для конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="1456f-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="1456f-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="1456f-156">-VlanId</span></span>
<span data-ttu-id="1456f-157">Это номер ID-номера VLAN, назначенного для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="1456f-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="1456f-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1456f-158">CommonParameters</span></span>
<span data-ttu-id="1456f-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1456f-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1456f-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1456f-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1456f-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1456f-161">INPUTS</span></span>

### <span data-ttu-id="1456f-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1456f-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="1456f-163">System.String</span><span class="sxs-lookup"><span data-stu-id="1456f-163">System.String</span></span>

### <span data-ttu-id="1456f-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1456f-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="1456f-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1456f-165">System.Boolean</span></span>

## <span data-ttu-id="1456f-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1456f-166">OUTPUTS</span></span>

### <span data-ttu-id="1456f-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1456f-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1456f-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1456f-168">NOTES</span></span>

## <span data-ttu-id="1456f-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1456f-169">RELATED LINKS</span></span>

[<span data-ttu-id="1456f-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1456f-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1456f-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1456f-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1456f-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1456f-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1456f-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1456f-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
