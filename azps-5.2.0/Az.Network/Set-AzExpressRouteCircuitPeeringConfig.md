---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: b41e7a0d6da67134cc1dd8842e0bd34c73128f58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327042"
---
# <span data-ttu-id="daff9-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="daff9-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="daff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daff9-102">SYNOPSIS</span></span>
<span data-ttu-id="daff9-103">Сохранение измененной конфигурации пиринга ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="daff9-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="daff9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="daff9-104">SYNTAX</span></span>

### <span data-ttu-id="daff9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="daff9-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daff9-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="daff9-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daff9-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="daff9-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daff9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="daff9-108">DESCRIPTION</span></span>
<span data-ttu-id="daff9-109">При **настройке Set-AzExpressRouteCircuitPeeringConfig** можно сохранить измененную конфигурацию пиринга ExpressRoute обратно в Azure.</span><span class="sxs-lookup"><span data-stu-id="daff9-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="daff9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="daff9-110">EXAMPLES</span></span>

### <span data-ttu-id="daff9-111">Пример 1. Изменение существующей конфигурации пиринга</span><span class="sxs-lookup"><span data-stu-id="daff9-111">Example 1: Change an existing peering configuration</span></span>
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

### <span data-ttu-id="daff9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="daff9-112">Example 2</span></span>

<span data-ttu-id="daff9-113">Сохранение измененной конфигурации пиринга ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="daff9-113">Saves a modified ExpressRoute peering configuration.</span></span> <span data-ttu-id="daff9-114">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="daff9-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzExpressRouteCircuitPeeringConfig -ExpressRouteCircuit <PSExpressRouteCircuit> -Name 'cert01' -PeerASN 100 -PeerAddressType IPv4 -PeeringType AzurePrivatePeering -PrimaryPeerAddressPrefix '123.0.0.0/30' -SecondaryPeerAddressPrefix '123.0.0.4/30' -VlanId 300
```

## <span data-ttu-id="daff9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daff9-115">PARAMETERS</span></span>

### <span data-ttu-id="daff9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daff9-116">-DefaultProfile</span></span>
<span data-ttu-id="daff9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="daff9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daff9-118">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="daff9-118">-ExpressRouteCircuit</span></span>
<span data-ttu-id="daff9-119">Объект схемы ExpressRoute, содержащий конфигурацию пиринга, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="daff9-119">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="daff9-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="daff9-120">-LegacyMode</span></span>
<span data-ttu-id="daff9-121">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="daff9-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="daff9-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="daff9-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="daff9-123">Для peeringType microsoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявлять в сеансе BGP.</span><span class="sxs-lookup"><span data-stu-id="daff9-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="daff9-124">Принимаются только префиксы общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="daff9-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="daff9-125">Если вы планируете отправить набор префиксов, вы можете отправить список с разделительными запятами.</span><span class="sxs-lookup"><span data-stu-id="daff9-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="daff9-126">Эти префиксы должны быть зарегистрированы в имени реестра routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="daff9-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="daff9-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="daff9-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="daff9-128">Если вы рекламируете префиксы, которые не зарегистрированы для номера пиринга AS, вы можете указать номер AS, на который они зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="daff9-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="daff9-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="daff9-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="daff9-130">Имя реестра routing (RIR/IRR), на которое зарегистрировано число AS и префиксы.</span><span class="sxs-lookup"><span data-stu-id="daff9-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="daff9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="daff9-131">-Name</span></span>
<span data-ttu-id="daff9-132">Имя измененной конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="daff9-132">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="daff9-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="daff9-133">-PeerAddressType</span></span>
<span data-ttu-id="daff9-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="daff9-134">PeerAddressType</span></span>

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

### <span data-ttu-id="daff9-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="daff9-135">-PeerASN</span></span>
<span data-ttu-id="daff9-136">As number of your ExpressRoute circuit.</span><span class="sxs-lookup"><span data-stu-id="daff9-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="daff9-137">Это должен быть общедоступный ASN, если пирингОм является AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="daff9-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="daff9-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="daff9-138">-PeeringType</span></span>
<span data-ttu-id="daff9-139">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="daff9-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="daff9-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="daff9-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="daff9-141">Это диапазон IP-адресов для основного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="daff9-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="daff9-142">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="daff9-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="daff9-143">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="daff9-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="daff9-144">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="daff9-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="daff9-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="daff9-145">-RouteFilter</span></span>
<span data-ttu-id="daff9-146">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="daff9-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="daff9-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="daff9-147">-RouteFilterId</span></span>
<span data-ttu-id="daff9-148">Это ид ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="daff9-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="daff9-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="daff9-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="daff9-150">Это диапазон IP-адресов для дополнительного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="daff9-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="daff9-151">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="daff9-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="daff9-152">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="daff9-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="daff9-153">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="daff9-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="daff9-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="daff9-154">-SharedKey</span></span>
<span data-ttu-id="daff9-155">Это необязательный hash MD5, который используется в качестве преду общих ключей для конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="daff9-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="daff9-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="daff9-156">-VlanId</span></span>
<span data-ttu-id="daff9-157">Это ИД VLAN, назначенного для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="daff9-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="daff9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daff9-158">CommonParameters</span></span>
<span data-ttu-id="daff9-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daff9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daff9-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daff9-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daff9-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="daff9-161">INPUTS</span></span>

### <span data-ttu-id="daff9-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="daff9-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="daff9-163">System.String</span><span class="sxs-lookup"><span data-stu-id="daff9-163">System.String</span></span>

### <span data-ttu-id="daff9-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="daff9-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="daff9-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="daff9-165">System.Boolean</span></span>

## <span data-ttu-id="daff9-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="daff9-166">OUTPUTS</span></span>

### <span data-ttu-id="daff9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="daff9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="daff9-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="daff9-168">NOTES</span></span>

## <span data-ttu-id="daff9-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="daff9-169">RELATED LINKS</span></span>

[<span data-ttu-id="daff9-170">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="daff9-170">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="daff9-171">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="daff9-171">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="daff9-172">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="daff9-172">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="daff9-173">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="daff9-173">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
