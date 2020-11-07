---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: dac01839a5a646e8fe75f4b47cda2650ac5ad280
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903113"
---
# <span data-ttu-id="eff36-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eff36-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="eff36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eff36-102">SYNOPSIS</span></span>
<span data-ttu-id="eff36-103">Добавляет конфигурацию пиринга к перекрестному соединению ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eff36-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="eff36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eff36-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eff36-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eff36-105">DESCRIPTION</span></span>
<span data-ttu-id="eff36-106">Командлет **Add-AzExpressRouteCrossConnectionPeering** добавляет конфигурацию пиринга к перекрестному соединению ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eff36-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="eff36-107">Обратите внимание, что после выполнения **Add-AzExpressRouteCrossConnectionPeering** необходимо вызвать командлет Set-AzExpressRouteCrossConnection для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="eff36-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="eff36-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eff36-108">EXAMPLES</span></span>

### <span data-ttu-id="eff36-109">Пример 1: Добавление однорангового узла к существующему перекрестному соединению ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="eff36-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="eff36-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eff36-110">PARAMETERS</span></span>

### <span data-ttu-id="eff36-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff36-111">-DefaultProfile</span></span>
<span data-ttu-id="eff36-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eff36-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff36-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eff36-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="eff36-114">Изменено перекрестное соединение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eff36-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="eff36-115">Это объект Azure, возвращенный командлетом **Get-AzExpressRouteCrossConnection** .</span><span class="sxs-lookup"><span data-stu-id="eff36-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="eff36-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eff36-116">-Force</span></span>
<span data-ttu-id="eff36-117">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="eff36-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eff36-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="eff36-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="eff36-119">Для PeeringType MicrosoftPeering необходимо предоставить список всех префиксов, которые вы планируете объявить для сеанса BGP.</span><span class="sxs-lookup"><span data-stu-id="eff36-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="eff36-120">Принимаются только префиксы общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="eff36-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="eff36-121">Вы можете отправить список с разделителями-запятыми, если вы собираетесь отправить набор префиксов.</span><span class="sxs-lookup"><span data-stu-id="eff36-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="eff36-122">Эти префиксы должны быть зарегистрированы в названии реестра маршрутизации (RIR/ВСД).</span><span class="sxs-lookup"><span data-stu-id="eff36-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="eff36-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="eff36-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="eff36-124">Если вы используете префиксы для рекламы, которые не зарегистрированы в качестве номера, вы можете указать номер, по которому они будут зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="eff36-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="eff36-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="eff36-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="eff36-126">Имя реестра маршрутизации (RIR/ВСД), для которого зарегистрированы номера и префиксы.</span><span class="sxs-lookup"><span data-stu-id="eff36-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="eff36-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eff36-127">-Name</span></span>
<span data-ttu-id="eff36-128">Имя добавляемого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="eff36-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="eff36-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="eff36-129">-PeerAddressType</span></span>
<span data-ttu-id="eff36-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="eff36-130">PeerAddressType</span></span>

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

### <span data-ttu-id="eff36-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="eff36-131">-PeerASN</span></span>
<span data-ttu-id="eff36-132">Число перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="eff36-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="eff36-133">Это значение должно быть общедоступным ASN, когда PeeringType — AzurePublicPeering.</span><span class="sxs-lookup"><span data-stu-id="eff36-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="eff36-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="eff36-134">-PeeringType</span></span>
<span data-ttu-id="eff36-135">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="eff36-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="eff36-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="eff36-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="eff36-137">Это диапазон IP-адресов для основного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="eff36-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="eff36-138">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="eff36-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="eff36-139">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="eff36-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="eff36-140">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="eff36-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="eff36-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="eff36-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="eff36-142">Это диапазон IP-адресов для дополнительного пути маршрутизации для этого отношения пиринга.</span><span class="sxs-lookup"><span data-stu-id="eff36-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="eff36-143">Это может быть и более 30 подсеть CIDR.</span><span class="sxs-lookup"><span data-stu-id="eff36-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="eff36-144">Первый нечетнымй адрес в этой подсети должен быть назначен интерфейсу маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="eff36-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="eff36-145">Azure настроит следующий четный нумерованный адрес для интерфейса маршрутизатора Azure.</span><span class="sxs-lookup"><span data-stu-id="eff36-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="eff36-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="eff36-146">-SharedKey</span></span>
<span data-ttu-id="eff36-147">Это необязательный хэш MD5, используемый в качестве предварительно общего ключа для настройки пиринга.</span><span class="sxs-lookup"><span data-stu-id="eff36-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="eff36-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="eff36-148">-VlanId</span></span>
<span data-ttu-id="eff36-149">Это идентификационный номер VLAN, назначенный для этого пиринга.</span><span class="sxs-lookup"><span data-stu-id="eff36-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="eff36-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eff36-150">-Confirm</span></span>
<span data-ttu-id="eff36-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eff36-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eff36-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff36-152">-WhatIf</span></span>
<span data-ttu-id="eff36-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eff36-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eff36-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eff36-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eff36-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff36-155">CommonParameters</span></span>
<span data-ttu-id="eff36-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eff36-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff36-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff36-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff36-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eff36-158">INPUTS</span></span>

### <span data-ttu-id="eff36-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eff36-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="eff36-160">Параметр "ExpressRouteCrossConnection" принимает значение типа "PSExpressRouteCrossConnection" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eff36-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="eff36-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eff36-161">OUTPUTS</span></span>

### <span data-ttu-id="eff36-162">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eff36-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eff36-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="eff36-163">NOTES</span></span>

## <span data-ttu-id="eff36-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eff36-164">RELATED LINKS</span></span>

[<span data-ttu-id="eff36-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eff36-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="eff36-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="eff36-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="eff36-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eff36-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="eff36-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eff36-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
