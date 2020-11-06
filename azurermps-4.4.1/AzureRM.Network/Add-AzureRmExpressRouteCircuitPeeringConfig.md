---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5655fafa866fbc3702a1c6bf017caddd21df6fab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569336"
---
# <span data-ttu-id="bfeb1-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bfeb1-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="bfeb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfeb1-102">SYNOPSIS</span></span>
<span data-ttu-id="bfeb1-103">Добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfeb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfeb1-104">SYNTAX</span></span>

### <span data-ttu-id="bfeb1-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfeb1-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfeb1-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="bfeb1-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfeb1-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="bfeb1-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <Int32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfeb1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfeb1-108">DESCRIPTION</span></span>
<span data-ttu-id="bfeb1-109">Командлет **Add-AzureRmExpressRouteCircuitPeeringConfig** добавляет конфигурацию пиринга в канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="bfeb1-110">Каналы ExpressRoute соединяют локальную сеть с облаком Microsoft, используя поставщик услуг по подключению к сети, а не общедоступный Интернет.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="bfeb1-111">Обратите внимание, что после выполнения **Add-AzureRmExpressRouteCircuitPeeringConfig** необходимо вызвать командлет Set-AzureRmExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="bfeb1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfeb1-112">EXAMPLES</span></span>

### <span data-ttu-id="bfeb1-113">Пример 1: Добавление однорангового элемента в существующую цепь ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="bfeb1-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="bfeb1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfeb1-114">PARAMETERS</span></span>

### <span data-ttu-id="bfeb1-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bfeb1-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bfeb1-116">Изменяемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-116">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="bfeb1-117">Это объект Azure, возвращенный командлетом **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="bfeb1-117">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="bfeb1-118">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="bfeb1-118">-LegacyMode</span></span>
<span data-ttu-id="bfeb1-119">Устаревший режим пиринга</span><span class="sxs-lookup"><span data-stu-id="bfeb1-119">The legacy mode of the Peering</span></span>

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

### <span data-ttu-id="bfeb1-120">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="bfeb1-120">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="bfeb1-121">Для PeeringType MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявить для сеанса BGP.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-121">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="bfeb1-122">Принимаются только префиксы общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-122">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="bfeb1-123">Вы можете отправить список с разделителями-запятыми, если вы собираетесь отправить набор префиксов.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-123">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="bfeb1-124">Эти префиксы должны быть зарегистрированы в названии реестра маршрутизации (RIR/ВСД).</span><span class="sxs-lookup"><span data-stu-id="bfeb1-124">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="bfeb1-125">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="bfeb1-125">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="bfeb1-126">Если вы используете префиксы для рекламы, которые не зарегистрированы в качестве номера, вы можете указать номер, по которому они будут зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-126">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="bfeb1-127">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="bfeb1-127">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="bfeb1-128">Имя реестра маршрутизации (RIR/ВСД), для которого зарегистрированы номера и префиксы.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-128">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="bfeb1-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfeb1-129">-Name</span></span>
<span data-ttu-id="bfeb1-130">Имя добавляемого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-130">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="bfeb1-131">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="bfeb1-131">-PeerAddressType</span></span>
<span data-ttu-id="bfeb1-132">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="bfeb1-132">PeerAddressType</span></span>

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

### <span data-ttu-id="bfeb1-133">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="bfeb1-133">-PeerASN</span></span>
<span data-ttu-id="bfeb1-134">Число в канале ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-134">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="bfeb1-135">Это значение должно быть общедоступным ASN, когда PeeringType — AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-135">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="bfeb1-136">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="bfeb1-136">-PeeringType</span></span>
<span data-ttu-id="bfeb1-137">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="bfeb1-137">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="bfeb1-138">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bfeb1-138">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="bfeb1-139">Это диапазон IP-адресов для основного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-139">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="bfeb1-140">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-140">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="bfeb1-141">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-141">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="bfeb1-142">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-142">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="bfeb1-143">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bfeb1-143">-RouteFilter</span></span>
<span data-ttu-id="bfeb1-144">Это существующий объект RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-144">This is an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="bfeb1-145">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="bfeb1-145">-RouteFilterId</span></span>
<span data-ttu-id="bfeb1-146">Это идентификатор ресурса существующего объекта RouteFilter.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-146">This is the resource Id of an existing RouteFilter object.</span></span>

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

### <span data-ttu-id="bfeb1-147">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bfeb1-147">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="bfeb1-148">Это диапазон IP-адресов для дополнительного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-148">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="bfeb1-149">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-149">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="bfeb1-150">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-150">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="bfeb1-151">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-151">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="bfeb1-152">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="bfeb1-152">-SharedKey</span></span>
<span data-ttu-id="bfeb1-153">Это необязательный хэш MD5, используемый в качестве предварительно общего ключа для настройки пиринга.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-153">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="bfeb1-154">-VlanId</span><span class="sxs-lookup"><span data-stu-id="bfeb1-154">-VlanId</span></span>
<span data-ttu-id="bfeb1-155">Это идентификационный номер VLAN, назначенный для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-155">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="bfeb1-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfeb1-156">-DefaultProfile</span></span>
<span data-ttu-id="bfeb1-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfeb1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfeb1-158">CommonParameters</span></span>
<span data-ttu-id="bfeb1-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfeb1-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfeb1-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfeb1-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfeb1-161">INPUTS</span></span>

### <span data-ttu-id="bfeb1-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bfeb1-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="bfeb1-163">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bfeb1-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="bfeb1-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfeb1-164">OUTPUTS</span></span>

### <span data-ttu-id="bfeb1-165">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bfeb1-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bfeb1-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfeb1-166">NOTES</span></span>

## <span data-ttu-id="bfeb1-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfeb1-167">RELATED LINKS</span></span>

[<span data-ttu-id="bfeb1-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bfeb1-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="bfeb1-169">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bfeb1-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="bfeb1-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bfeb1-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="bfeb1-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bfeb1-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
