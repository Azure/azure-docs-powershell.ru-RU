---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237089"
---
# <span data-ttu-id="70666-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="70666-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="70666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70666-102">SYNOPSIS</span></span>
<span data-ttu-id="70666-103">Добавляет конфигурацию пиринга к перекрестным подключениям ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="70666-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="70666-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70666-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70666-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70666-105">DESCRIPTION</span></span>
<span data-ttu-id="70666-106">Cmdlet **Add-AzExpressRouteCrossConnectionPeering** добавляет конфигурацию пиринга к перекрестным подключениям ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="70666-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="70666-107">Обратите внимание, что после запуска **Add-AzExpressRouteCrossConnectionPeering** необходимо вызвать Set-AzExpressRouteCrossConnection для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="70666-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="70666-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70666-108">EXAMPLES</span></span>

### <span data-ttu-id="70666-109">Пример 1. Добавление одноранговых подключений к существующему перекрестным подключением ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="70666-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="70666-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70666-110">PARAMETERS</span></span>

### <span data-ttu-id="70666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70666-111">-DefaultProfile</span></span>
<span data-ttu-id="70666-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70666-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70666-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="70666-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="70666-114">Перекрестное подключение ExpressRoute будет изменено.</span><span class="sxs-lookup"><span data-stu-id="70666-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="70666-115">Это объект Azure, возвращенный **cmdlet Get-AzExpressRouteCrossConnection.**</span><span class="sxs-lookup"><span data-stu-id="70666-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70666-116">-Force</span><span class="sxs-lookup"><span data-stu-id="70666-116">-Force</span></span>
<span data-ttu-id="70666-117">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="70666-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="70666-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="70666-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="70666-119">Для пиринга MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявлять в сеансе BGP.</span><span class="sxs-lookup"><span data-stu-id="70666-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="70666-120">Принимаются только префиксы общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="70666-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="70666-121">Если вы планируете отправить набор префиксов, вы можете отправить список с разделительными запятами.</span><span class="sxs-lookup"><span data-stu-id="70666-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="70666-122">Эти префиксы должны быть зарегистрированы в домене реестра routing (RIR/IRR).</span><span class="sxs-lookup"><span data-stu-id="70666-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="70666-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="70666-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="70666-124">Если вы рекламируете префиксы, которые не зарегистрированы для номера пиринга AS, вы можете указать номер AS, на который они зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="70666-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="70666-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="70666-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="70666-126">Имя реестра routing (RIR/IRR), на которое зарегистрировано число AS и префиксы.</span><span class="sxs-lookup"><span data-stu-id="70666-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="70666-127">-Name</span><span class="sxs-lookup"><span data-stu-id="70666-127">-Name</span></span>
<span data-ttu-id="70666-128">Имя добавляемого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="70666-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="70666-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="70666-129">-PeerAddressType</span></span>
<span data-ttu-id="70666-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="70666-130">PeerAddressType</span></span>

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

### <span data-ttu-id="70666-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="70666-131">-PeerASN</span></span>
<span data-ttu-id="70666-132">As number of your ExpressRoute cross connection.</span><span class="sxs-lookup"><span data-stu-id="70666-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="70666-133">Это должен быть общедоступный ASN, если пирингОм является AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="70666-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="70666-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="70666-134">-PeeringType</span></span>
<span data-ttu-id="70666-135">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="70666-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="70666-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="70666-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="70666-137">Это диапазон IP-адресов для основного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="70666-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="70666-138">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="70666-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="70666-139">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="70666-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="70666-140">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="70666-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="70666-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="70666-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="70666-142">Это диапазон IP-адресов для дополнительного пути маршрутинга для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="70666-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="70666-143">Это должна быть подсеть CIDR /30.</span><span class="sxs-lookup"><span data-stu-id="70666-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="70666-144">В интерфейсе маршрутизатора должен быть назначен первый нечетный адрес в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="70666-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="70666-145">Azure настроит следующий ровный адрес в интерфейсе маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="70666-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="70666-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="70666-146">-SharedKey</span></span>
<span data-ttu-id="70666-147">Это необязательный hash MD5, который используется в качестве предварительного общего ключа для конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="70666-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="70666-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="70666-148">-VlanId</span></span>
<span data-ttu-id="70666-149">Это ИД VLAN, назначенного для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="70666-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="70666-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70666-150">-Confirm</span></span>
<span data-ttu-id="70666-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70666-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70666-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70666-152">-WhatIf</span></span>
<span data-ttu-id="70666-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70666-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70666-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="70666-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70666-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70666-155">CommonParameters</span></span>
<span data-ttu-id="70666-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70666-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70666-157">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70666-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70666-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70666-158">INPUTS</span></span>

### <span data-ttu-id="70666-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="70666-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="70666-160">Параметр "ExpressRouteCrossConnection" принимает значение типа PSExpressRouteCrossConnection из конвейера.</span><span class="sxs-lookup"><span data-stu-id="70666-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="70666-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70666-161">OUTPUTS</span></span>

### <span data-ttu-id="70666-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="70666-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="70666-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70666-163">NOTES</span></span>

## <span data-ttu-id="70666-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70666-164">RELATED LINKS</span></span>

[<span data-ttu-id="70666-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="70666-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="70666-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="70666-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="70666-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="70666-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="70666-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="70666-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
