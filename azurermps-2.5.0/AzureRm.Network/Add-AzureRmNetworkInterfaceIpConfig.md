---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: 8f0678f3b8c14e6d0c98c5cf29857fc3b2cad794
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913645"
---
# <span data-ttu-id="d01f9-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d01f9-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d01f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d01f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d01f9-103">Добавление IP-конфигурации сетевого интерфейса к сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="d01f9-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d01f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d01f9-104">SYNTAX</span></span>

### <span data-ttu-id="d01f9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d01f9-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d01f9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d01f9-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d01f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d01f9-107">DESCRIPTION</span></span>
<span data-ttu-id="d01f9-108">Командлет **Add-AzureRmNetworkInterfaceIpConfig** добавляет IP-конфигурацию сетевого интерфейса к сетевому интерфейсу Azure.</span><span class="sxs-lookup"><span data-stu-id="d01f9-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="d01f9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d01f9-109">EXAMPLES</span></span>

### <span data-ttu-id="d01f9-110">Пример 1: Добавление новой конфигурации IP с помощью группы безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="d01f9-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="d01f9-111">В этом примере мы создаем новый сетевой интерфейс MyNetworkInterface, который принадлежит к подсети в новой виртуальной сети MyVNET.</span><span class="sxs-lookup"><span data-stu-id="d01f9-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="d01f9-112">Кроме того, мы создам пустую группу безопасности приложений MyASG для связи с конфигурациями IP в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d01f9-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="d01f9-113">После того как оба объекта созданы, свяжите конфигурацию IP по умолчанию с объектом MyASG.</span><span class="sxs-lookup"><span data-stu-id="d01f9-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="d01f9-114">Наконец, мы создам новую конфигурацию IP в сетевом интерфейсе, также связанной с объектом группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="d01f9-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="d01f9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d01f9-115">PARAMETERS</span></span>

### <span data-ttu-id="d01f9-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d01f9-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="d01f9-117">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d01f9-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="d01f9-119">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d01f9-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="d01f9-121">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d01f9-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="d01f9-123">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01f9-124">-DefaultProfile</span></span>
<span data-ttu-id="d01f9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d01f9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d01f9-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="d01f9-127">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d01f9-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="d01f9-129">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="d01f9-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="d01f9-131">Указывает коллекцию ссылок на правила преобразования сетевых адресов (NAT) для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="d01f9-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="d01f9-133">Задает коллекцию ссылок на правила NAT для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d01f9-134">-Name</span></span>
<span data-ttu-id="d01f9-135">Задает имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-135">Specifies the name of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d01f9-136">-NetworkInterface</span></span>
<span data-ttu-id="d01f9-137">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="d01f9-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="d01f9-138">Этот командлет добавляет IP-конфигурацию сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d01f9-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="d01f9-139">-Primary</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d01f9-140">-PrivateIpAddress</span></span>
<span data-ttu-id="d01f9-141">Задает статический IP-адрес IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-141">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d01f9-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d01f9-143">Определяет версию IP-адреса конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="d01f9-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d01f9-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d01f9-145">IPv6</span><span class="sxs-lookup"><span data-stu-id="d01f9-145">IPv4</span></span>
- <span data-ttu-id="d01f9-146">IPv</span><span class="sxs-lookup"><span data-stu-id="d01f9-146">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d01f9-147">-PublicIpAddress</span></span>
<span data-ttu-id="d01f9-148">Указывает объект **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="d01f9-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="d01f9-149">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d01f9-150">-PublicIpAddressId</span></span>
<span data-ttu-id="d01f9-151">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-152">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="d01f9-152">-Subnet</span></span>
<span data-ttu-id="d01f9-153">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="d01f9-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="d01f9-154">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d01f9-155">-SubnetId</span></span>
<span data-ttu-id="d01f9-156">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d01f9-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01f9-157">CommonParameters</span></span>
<span data-ttu-id="d01f9-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d01f9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01f9-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d01f9-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01f9-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d01f9-160">INPUTS</span></span>

### <span data-ttu-id="d01f9-161">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d01f9-161">PSNetworkInterface</span></span>
<span data-ttu-id="d01f9-162">Параметр "NetworkInterface" принимает значение типа "PSNetworkInterface" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d01f9-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="d01f9-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d01f9-163">OUTPUTS</span></span>

### <span data-ttu-id="d01f9-164">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d01f9-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d01f9-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="d01f9-165">NOTES</span></span>
* <span data-ttu-id="d01f9-166">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="d01f9-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d01f9-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d01f9-167">RELATED LINKS</span></span>

[<span data-ttu-id="d01f9-168">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d01f9-168">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d01f9-169">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d01f9-169">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d01f9-170">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d01f9-170">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d01f9-171">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d01f9-171">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


