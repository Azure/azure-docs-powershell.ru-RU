---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 4d329b0521e5b0f4974c25382be53ff32267e51c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911850"
---
# <span data-ttu-id="d33e5-101">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d33e5-101">Add-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="d33e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d33e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d33e5-103">Добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d33e5-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

## <span data-ttu-id="d33e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d33e5-104">SYNTAX</span></span>

### <span data-ttu-id="d33e5-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d33e5-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d33e5-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="d33e5-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d33e5-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="d33e5-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String>
 -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilter <PSRouteFilter> [-PeerAddressType <String>]
 [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d33e5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d33e5-108">DESCRIPTION</span></span>
<span data-ttu-id="d33e5-109">Командлет **Add-AzExpressRouteCircuitPeeringConfig** добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d33e5-109">The **Add-AzExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="d33e5-110">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="d33e5-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="d33e5-111">Обратите внимание, что после выполнения **Add-AzExpressRouteCircuitPeeringConfig** необходимо вызвать командлет Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d33e5-111">Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="d33e5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d33e5-112">EXAMPLES</span></span>

### <span data-ttu-id="d33e5-113">Пример 1: Добавление однорангового элемента в существующую цепь ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d33e5-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
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

## <span data-ttu-id="d33e5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d33e5-114">PARAMETERS</span></span>

### <span data-ttu-id="d33e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33e5-115">-DefaultProfile</span></span>
<span data-ttu-id="d33e5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d33e5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d33e5-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d33e5-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d33e5-118">Изменяемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d33e5-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="d33e5-119">Это объект Azure, возвращенный командлетом **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="d33e5-119">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="d33e5-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="d33e5-120">-LegacyMode</span></span>
<span data-ttu-id="d33e5-121">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="d33e5-121">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="d33e5-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="d33e5-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="d33e5-123">Для PeeringType MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявить для сеанса BGP.</span><span class="sxs-lookup"><span data-stu-id="d33e5-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="d33e5-124">Принимаются только префиксы общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d33e5-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="d33e5-125">Вы можете отправить список с разделителями-запятыми, если вы собираетесь отправить набор префиксов.</span><span class="sxs-lookup"><span data-stu-id="d33e5-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="d33e5-126">Эти префиксы должны быть зарегистрированы в названии реестра маршрутизации (RIR/ВСД).</span><span class="sxs-lookup"><span data-stu-id="d33e5-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="d33e5-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="d33e5-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="d33e5-128">Если вы используете префиксы для рекламы, которые не зарегистрированы в качестве номера, вы можете указать номер, по которому они будут зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="d33e5-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="d33e5-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="d33e5-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="d33e5-130">Имя реестра маршрутизации (RIR/ВСД), для которого зарегистрированы номера и префиксы.</span><span class="sxs-lookup"><span data-stu-id="d33e5-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="d33e5-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d33e5-131">-Name</span></span>
<span data-ttu-id="d33e5-132">Имя добавляемого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="d33e5-132">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="d33e5-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d33e5-133">-PeerAddressType</span></span>
<span data-ttu-id="d33e5-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="d33e5-134">PeerAddressType</span></span>

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

### <span data-ttu-id="d33e5-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="d33e5-135">-PeerASN</span></span>
<span data-ttu-id="d33e5-136">Число в канале ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d33e5-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="d33e5-137">Это значение должно быть общедоступным ASN, когда PeeringType — AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="d33e5-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="d33e5-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="d33e5-138">-PeeringType</span></span>
<span data-ttu-id="d33e5-139">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="d33e5-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="d33e5-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d33e5-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="d33e5-141">Это диапазон IP-адресов для основного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="d33e5-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="d33e5-142">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="d33e5-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="d33e5-143">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d33e5-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="d33e5-144">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="d33e5-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="d33e5-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d33e5-145">-RouteFilter</span></span>
<span data-ttu-id="d33e5-146">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="d33e5-146">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="d33e5-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="d33e5-147">-RouteFilterId</span></span>
<span data-ttu-id="d33e5-148">Это идентификатор ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="d33e5-148">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="d33e5-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d33e5-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="d33e5-150">Это диапазон IP-адресов для дополнительного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="d33e5-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="d33e5-151">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="d33e5-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="d33e5-152">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="d33e5-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="d33e5-153">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="d33e5-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="d33e5-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="d33e5-154">-SharedKey</span></span>
<span data-ttu-id="d33e5-155">Это необязательный хэш MD5, используемый в качестве предварительно общего ключа для настройки пиринга.</span><span class="sxs-lookup"><span data-stu-id="d33e5-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="d33e5-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="d33e5-156">-VlanId</span></span>
<span data-ttu-id="d33e5-157">Это идентификационный номер VLAN, назначенный для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="d33e5-157">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="d33e5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33e5-158">CommonParameters</span></span>
<span data-ttu-id="d33e5-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d33e5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33e5-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d33e5-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33e5-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d33e5-161">INPUTS</span></span>

### <span data-ttu-id="d33e5-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d33e5-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="d33e5-163">System. String</span><span class="sxs-lookup"><span data-stu-id="d33e5-163">System.String</span></span>

### <span data-ttu-id="d33e5-164">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d33e5-164">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

### <span data-ttu-id="d33e5-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d33e5-165">System.Boolean</span></span>

## <span data-ttu-id="d33e5-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d33e5-166">OUTPUTS</span></span>

### <span data-ttu-id="d33e5-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d33e5-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d33e5-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="d33e5-168">NOTES</span></span>

## <span data-ttu-id="d33e5-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d33e5-169">RELATED LINKS</span></span>

[<span data-ttu-id="d33e5-170">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d33e5-170">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d33e5-171">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d33e5-171">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="d33e5-172">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="d33e5-172">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="d33e5-173">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d33e5-173">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
