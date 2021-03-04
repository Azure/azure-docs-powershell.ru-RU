---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 42a2ec1c3fb19647cc956c6b7321f52e6ad6e63e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952040"
---
# <span data-ttu-id="b7b6e-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b7b6e-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="b7b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b6e-103">Сохранение измененной конфигурации пиринга ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="b7b6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7b6e-104">SYNTAX</span></span>

### <span data-ttu-id="b7b6e-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7b6e-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7b6e-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="b7b6e-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7b6e-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="b7b6e-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b6e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7b6e-108">DESCRIPTION</span></span>
<span data-ttu-id="b7b6e-109">При **этом измененная** конфигурация пиринга ExpressRoute сохраняется в Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="b7b6e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7b6e-110">EXAMPLES</span></span>

### <span data-ttu-id="b7b6e-111">Пример 1. Изменение существующей конфигурации пиринга</span><span class="sxs-lookup"><span data-stu-id="b7b6e-111">Example 1: Change an existing peering configuration</span></span>
```powershell
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 201
}
Set-AzExpressRouteCircuitPeeringConfig @parameters
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

### <span data-ttu-id="b7b6e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b7b6e-112">Example 2</span></span>

<span data-ttu-id="b7b6e-113">Сохранение измененной конфигурации пиринга ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="b7b6e-114">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="b7b6e-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="b7b6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7b6e-115">PARAMETERS</span></span>

### <span data-ttu-id="b7b6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b6e-116">-DefaultProfile</span></span>
<span data-ttu-id="b7b6e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b6e-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7b6e-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b7b6e-119">Объект схемы ExpressRoute, содержащий конфигурацию пиринга, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="b7b6e-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="b7b6e-120">-LegacyMode</span></span>
<span data-ttu-id="b7b6e-121">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="b7b6e-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="b7b6e-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="b7b6e-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="b7b6e-123">Для пиринга MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявлять в сеансе BGP.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="b7b6e-124">Принимаются только префиксы общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="b7b6e-125">Если вы планируете отправить набор префиксов, вы можете отправить список с разделительными запятами.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="b7b6e-126">Эти префиксы должны быть зарегистрированы в домене реестра routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="b7b6e-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="b7b6e-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="b7b6e-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="b7b6e-128">Если вы рекламируете префиксы, которые не зарегистрированы для номера пиринга AS, вы можете указать номер AS, на который они зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="b7b6e-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="b7b6e-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="b7b6e-130">Имя реестра routing (RIR/IRR), на которое зарегистрировано число AS и префиксы.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="b7b6e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b7b6e-131">-Name</span></span>
<span data-ttu-id="b7b6e-132">Имя измененной конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="b7b6e-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b7b6e-133">-PeerAddressType</span></span>
<span data-ttu-id="b7b6e-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="b7b6e-134">PeerAddressType</span></span>

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

### <span data-ttu-id="b7b6e-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="b7b6e-135">-PeerASN</span></span>
<span data-ttu-id="b7b6e-136">As number of your ExpressRoute circuit.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="b7b6e-137">Это должен быть общедоступный ASN, если пирингОм является AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="b7b6e-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b7b6e-138">-PeeringType</span></span>
<span data-ttu-id="b7b6e-139">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b7b6e-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b7b6e-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b7b6e-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="b7b6e-141">Это диапазон IP-адресов для основного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="b7b6e-142">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b7b6e-143">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b7b6e-144">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b7b6e-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b7b6e-145">-RouteFilter</span></span>
<span data-ttu-id="b7b6e-146">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b7b6e-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="b7b6e-147">-RouteFilterId</span></span>
<span data-ttu-id="b7b6e-148">Это ид ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="b7b6e-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b7b6e-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="b7b6e-150">Это диапазон IP-адресов для дополнительного пути маршрутинга этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="b7b6e-151">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="b7b6e-152">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="b7b6e-153">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="b7b6e-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="b7b6e-154">-SharedKey</span></span>
<span data-ttu-id="b7b6e-155">Это необязательный hash MD5, который используется в качестве преду общих ключей для конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="b7b6e-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="b7b6e-156">-VlanId</span></span>
<span data-ttu-id="b7b6e-157">Это номер ID-номера VLAN, назначенного для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="b7b6e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b6e-158">CommonParameters</span></span>
<span data-ttu-id="b7b6e-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b6e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b6e-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b6e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b6e-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7b6e-161">INPUTS</span></span>

### <span data-ttu-id="b7b6e-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7b6e-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="b7b6e-163">System.String</span><span class="sxs-lookup"><span data-stu-id="b7b6e-163">System.String</span></span>

### <span data-ttu-id="b7b6e-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b7b6e-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="b7b6e-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7b6e-165">System.Boolean</span></span>

## <span data-ttu-id="b7b6e-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7b6e-166">OUTPUTS</span></span>

### <span data-ttu-id="b7b6e-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7b6e-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b7b6e-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7b6e-168">NOTES</span></span>

## <span data-ttu-id="b7b6e-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7b6e-169">RELATED LINKS</span></span>

[<span data-ttu-id="b7b6e-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b7b6e-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b7b6e-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7b6e-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7b6e-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b7b6e-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="b7b6e-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="b7b6e-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
