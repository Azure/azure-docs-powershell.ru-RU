---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C0281EC-4D23-4BD0-A268-4C278ABC7B1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: ffc605a9376864a0576c4f7a6ae69f157ab9bacc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065812"
---
# <span data-ttu-id="1dd5f-101">Set-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dd5f-101">Set-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1dd5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1dd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd5f-103">Сохранение измененной конфигурации пиринга ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-103">Saves a modified ExpressRoute peering configuration.</span></span>

## <span data-ttu-id="1dd5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1dd5f-104">SYNTAX</span></span>

### <span data-ttu-id="1dd5f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1dd5f-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dd5f-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="1dd5f-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dd5f-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="1dd5f-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Set-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dd5f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dd5f-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd5f-109">Командлеты **Set-AzExpressRouteCircuitPeeringConfig** сохраняют модифицированную конфигурацию пиринга ExpressRoute обратно в Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-109">The **Set-AzExpressRouteCircuitPeeringConfig** cmdlets saves a modified ExpressRoute peering configuration back to Azure.</span></span>

## <span data-ttu-id="1dd5f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1dd5f-110">EXAMPLES</span></span>

### <span data-ttu-id="1dd5f-111">Пример 1: изменение существующей конфигурации пиринга</span><span class="sxs-lookup"><span data-stu-id="1dd5f-111">Example 1: Change an existing peering configuration</span></span>
```
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

## <span data-ttu-id="1dd5f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1dd5f-112">PARAMETERS</span></span>

### <span data-ttu-id="1dd5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd5f-113">-DefaultProfile</span></span>
<span data-ttu-id="1dd5f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dd5f-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1dd5f-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1dd5f-116">Объект цепи ExpressRoute, содержащий конфигурацию пиринга, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-116">The ExpressRoute circuit object containing the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="1dd5f-117">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="1dd5f-117">-LegacyMode</span></span>
<span data-ttu-id="1dd5f-118">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="1dd5f-118">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="1dd5f-119">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="1dd5f-119">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="1dd5f-120">Для PeeringType MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявить для сеанса BGP.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-120">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="1dd5f-121">Принимаются только префиксы общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-121">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="1dd5f-122">Вы можете отправить список с разделителями-запятыми, если вы собираетесь отправить набор префиксов.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-122">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="1dd5f-123">Эти префиксы должны быть зарегистрированы в названии реестра маршрутизации (RIR/ВСД).</span><span class="sxs-lookup"><span data-stu-id="1dd5f-123">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="1dd5f-124">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="1dd5f-124">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="1dd5f-125">Если вы используете префиксы для рекламы, которые не зарегистрированы в качестве номера, вы можете указать номер, по которому они будут зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-125">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="1dd5f-126">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="1dd5f-126">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="1dd5f-127">Имя реестра маршрутизации (RIR/ВСД), для которого зарегистрированы номера и префиксы.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-127">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="1dd5f-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1dd5f-128">-Name</span></span>
<span data-ttu-id="1dd5f-129">Имя конфигурации пиринга, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-129">The name of the peering configuration to be modified.</span></span>

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

### <span data-ttu-id="1dd5f-130">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1dd5f-130">-PeerAddressType</span></span>
<span data-ttu-id="1dd5f-131">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="1dd5f-131">PeerAddressType</span></span>

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

### <span data-ttu-id="1dd5f-132">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="1dd5f-132">-PeerASN</span></span>
<span data-ttu-id="1dd5f-133">Число в канале ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-133">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="1dd5f-134">Это значение должно быть общедоступным ASN, когда PeeringType — AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-134">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="1dd5f-135">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="1dd5f-135">-PeeringType</span></span>
<span data-ttu-id="1dd5f-136">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="1dd5f-136">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="1dd5f-137">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1dd5f-137">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="1dd5f-138">Это диапазон IP-адресов для основного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-138">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="1dd5f-139">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-139">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1dd5f-140">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-140">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1dd5f-141">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-141">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="1dd5f-142">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dd5f-142">-RouteFilter</span></span>
<span data-ttu-id="1dd5f-143">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-143">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="1dd5f-144">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="1dd5f-144">-RouteFilterId</span></span>
<span data-ttu-id="1dd5f-145">Это идентификатор ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-145">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="1dd5f-146">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1dd5f-146">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="1dd5f-147">Это диапазон IP-адресов для дополнительного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-147">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="1dd5f-148">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-148">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="1dd5f-149">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-149">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="1dd5f-150">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-150">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="1dd5f-151">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="1dd5f-151">-SharedKey</span></span>
<span data-ttu-id="1dd5f-152">Это необязательный хэш MD5, используемый в качестве предварительно общего ключа для настройки пиринга.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-152">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="1dd5f-153">-VlanId</span><span class="sxs-lookup"><span data-stu-id="1dd5f-153">-VlanId</span></span>
<span data-ttu-id="1dd5f-154">Это идентификационный номер VLAN, назначенный для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-154">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="1dd5f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd5f-155">CommonParameters</span></span>
<span data-ttu-id="1dd5f-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1dd5f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd5f-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd5f-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd5f-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1dd5f-158">INPUTS</span></span>

### <span data-ttu-id="1dd5f-159">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1dd5f-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="1dd5f-160">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd5f-160">System.String</span></span>

### <span data-ttu-id="1dd5f-161">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1dd5f-161">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="1dd5f-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1dd5f-162">System.Boolean</span></span>

## <span data-ttu-id="1dd5f-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dd5f-163">OUTPUTS</span></span>

### <span data-ttu-id="1dd5f-164">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1dd5f-164">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1dd5f-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="1dd5f-165">NOTES</span></span>

## <span data-ttu-id="1dd5f-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dd5f-166">RELATED LINKS</span></span>

[<span data-ttu-id="1dd5f-167">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dd5f-167">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1dd5f-168">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1dd5f-168">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1dd5f-169">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dd5f-169">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1dd5f-170">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1dd5f-170">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)
