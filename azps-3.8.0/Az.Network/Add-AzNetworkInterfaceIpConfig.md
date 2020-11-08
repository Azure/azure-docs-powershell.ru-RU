---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073592"
---
# <span data-ttu-id="2195e-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2195e-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="2195e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2195e-102">SYNOPSIS</span></span>
<span data-ttu-id="2195e-103">Добавление IP-конфигурации сетевого интерфейса к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="2195e-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="2195e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2195e-104">SYNTAX</span></span>

### <span data-ttu-id="2195e-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2195e-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2195e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2195e-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2195e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2195e-107">DESCRIPTION</span></span>
<span data-ttu-id="2195e-108">Командлет **Add-AzNetworkInterfaceIpConfig** добавляет IP-конфигурацию сетевого интерфейса к сетевому интерфейсу Azure.</span><span class="sxs-lookup"><span data-stu-id="2195e-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="2195e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2195e-109">EXAMPLES</span></span>

### <span data-ttu-id="2195e-110">Пример 1: Добавление новой конфигурации IP с помощью группы безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="2195e-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="2195e-111">В этом примере мы создаем новый сетевой интерфейс MyNetworkInterface, который принадлежит к подсети в новой виртуальной сети MyVNET.</span><span class="sxs-lookup"><span data-stu-id="2195e-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="2195e-112">Кроме того, мы создам пустую группу безопасности приложений MyASG для связи с конфигурациями IP в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="2195e-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="2195e-113">После того как оба объекта созданы, свяжите конфигурацию IP по умолчанию с объектом MyASG.</span><span class="sxs-lookup"><span data-stu-id="2195e-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="2195e-114">Наконец, мы создам новую конфигурацию IP в сетевом интерфейсе, также связанной с объектом группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="2195e-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="2195e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2195e-115">PARAMETERS</span></span>

### <span data-ttu-id="2195e-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2195e-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="2195e-117">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2195e-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="2195e-119">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2195e-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="2195e-121">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2195e-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="2195e-123">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2195e-124">-DefaultProfile</span></span>
<span data-ttu-id="2195e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2195e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2195e-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2195e-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="2195e-127">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2195e-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="2195e-129">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2195e-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="2195e-131">Указывает коллекцию ссылок на правила преобразования сетевых адресов (NAT) для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="2195e-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="2195e-133">Задает коллекцию ссылок на правила NAT для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2195e-134">-Name</span></span>
<span data-ttu-id="2195e-135">Задает имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="2195e-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2195e-136">-NetworkInterface</span></span>
<span data-ttu-id="2195e-137">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="2195e-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="2195e-138">Этот командлет добавляет IP-конфигурацию сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="2195e-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="2195e-139">-Primary</span></span>
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

### <span data-ttu-id="2195e-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2195e-140">-PrivateIpAddress</span></span>
<span data-ttu-id="2195e-141">Задает статический IP-адрес IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="2195e-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2195e-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="2195e-143">Определяет версию IP-адреса конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="2195e-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2195e-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2195e-145">IPv6</span><span class="sxs-lookup"><span data-stu-id="2195e-145">IPv4</span></span>
- <span data-ttu-id="2195e-146">IPv</span><span class="sxs-lookup"><span data-stu-id="2195e-146">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2195e-147">-PublicIpAddress</span></span>
<span data-ttu-id="2195e-148">Указывает объект **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="2195e-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="2195e-149">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2195e-150">-PublicIpAddressId</span></span>
<span data-ttu-id="2195e-151">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-152">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="2195e-152">-Subnet</span></span>
<span data-ttu-id="2195e-153">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="2195e-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="2195e-154">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2195e-155">-SubnetId</span></span>
<span data-ttu-id="2195e-156">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2195e-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2195e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2195e-157">CommonParameters</span></span>
<span data-ttu-id="2195e-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2195e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2195e-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2195e-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2195e-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2195e-160">INPUTS</span></span>

### <span data-ttu-id="2195e-161">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2195e-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="2195e-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="2195e-162">System.String[]</span></span>

### <span data-ttu-id="2195e-163">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="2195e-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="2195e-164">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="2195e-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="2195e-165">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="2195e-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="2195e-166">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="2195e-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="2195e-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2195e-167">OUTPUTS</span></span>

### <span data-ttu-id="2195e-168">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2195e-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2195e-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="2195e-169">NOTES</span></span>
* <span data-ttu-id="2195e-170">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="2195e-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2195e-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2195e-171">RELATED LINKS</span></span>

[<span data-ttu-id="2195e-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2195e-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2195e-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2195e-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2195e-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2195e-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2195e-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2195e-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
