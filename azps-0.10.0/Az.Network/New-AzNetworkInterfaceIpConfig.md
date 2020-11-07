---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 7776bb57215ce3cb9b4291a0a71fdb01e028491e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909666"
---
# <span data-ttu-id="317bf-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="317bf-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="317bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="317bf-102">SYNOPSIS</span></span>
<span data-ttu-id="317bf-103">Создание IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="317bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="317bf-104">SYNTAX</span></span>

### <span data-ttu-id="317bf-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="317bf-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="317bf-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="317bf-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="317bf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="317bf-107">DESCRIPTION</span></span>
<span data-ttu-id="317bf-108">Командлет **New-AzNetworkInterfaceIpConfig** создает IP-конфигурацию сетевого интерфейса Azure для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="317bf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="317bf-109">EXAMPLES</span></span>

### <span data-ttu-id="317bf-110">1: создание IP-конфигурации с общедоступным IP-адресом для сетевого интерфейса</span><span class="sxs-lookup"><span data-stu-id="317bf-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="317bf-111">Первые две команды получают виртуальную сеть под названием myvnet и подсеть под названием mysubnet, которая была ранее создана.</span><span class="sxs-lookup"><span data-stu-id="317bf-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="317bf-112">Они хранятся в $vnet и $Subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="317bf-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="317bf-113">Третья команда получает ранее созданный общедоступный IP-адрес с именем PIP1.</span><span class="sxs-lookup"><span data-stu-id="317bf-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="317bf-114">С помощью команды "вперед" создается новая конфигурация IP, называемая "IPConfig-1", в качестве основной конфигурации IP-адреса, связанной с общедоступным IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="317bf-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="317bf-115">Последняя команда затем создает сетевой интерфейс с именем mynic1, используя эту конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="317bf-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="317bf-116">2. Создание конфигурации IP с частным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="317bf-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="317bf-117">Первые две команды получают виртуальную сеть под названием myvnet и подсеть под названием mysubnet, которая была ранее создана.</span><span class="sxs-lookup"><span data-stu-id="317bf-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="317bf-118">Они хранятся в $vnet и $Subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="317bf-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="317bf-119">Третья команда создает новую IP-конфигурацию с именем IPConfig-2 и связанным с ней частным IP-адресом 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="317bf-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="317bf-120">Последняя команда затем создает сетевой интерфейс с именем mynic1, используя эту конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="317bf-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="317bf-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="317bf-121">PARAMETERS</span></span>

### <span data-ttu-id="317bf-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="317bf-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="317bf-123">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="317bf-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="317bf-125">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="317bf-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="317bf-127">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="317bf-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="317bf-129">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317bf-130">-DefaultProfile</span></span>
<span data-ttu-id="317bf-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="317bf-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="317bf-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="317bf-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="317bf-133">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="317bf-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="317bf-135">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="317bf-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="317bf-137">Указывает коллекцию ссылок на правила NAT для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="317bf-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="317bf-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="317bf-139">Указывает коллекцию ссылок на правила преобразования сетевых адресов (NAT) для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="317bf-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="317bf-140">-Name</span></span>
<span data-ttu-id="317bf-141">Задает имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="317bf-142">-Primary</span><span class="sxs-lookup"><span data-stu-id="317bf-142">-Primary</span></span>
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

### <span data-ttu-id="317bf-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="317bf-143">-PrivateIpAddress</span></span>
<span data-ttu-id="317bf-144">Задает статический IP-адрес IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="317bf-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="317bf-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="317bf-146">Определяет версию IP-адреса конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="317bf-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="317bf-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="317bf-148">IPv6</span><span class="sxs-lookup"><span data-stu-id="317bf-148">IPv4</span></span>
- <span data-ttu-id="317bf-149">IPv</span><span class="sxs-lookup"><span data-stu-id="317bf-149">IPv6</span></span>

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

### <span data-ttu-id="317bf-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="317bf-150">-PublicIpAddress</span></span>
<span data-ttu-id="317bf-151">Указывает объект **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="317bf-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="317bf-152">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="317bf-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="317bf-153">-PublicIpAddressId</span></span>
<span data-ttu-id="317bf-154">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="317bf-155">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="317bf-155">-Subnet</span></span>
<span data-ttu-id="317bf-156">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="317bf-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="317bf-157">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="317bf-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="317bf-158">-SubnetId</span></span>
<span data-ttu-id="317bf-159">Указывает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="317bf-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="317bf-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317bf-160">CommonParameters</span></span>
<span data-ttu-id="317bf-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="317bf-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317bf-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317bf-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317bf-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="317bf-163">INPUTS</span></span>

## <span data-ttu-id="317bf-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="317bf-164">OUTPUTS</span></span>

### <span data-ttu-id="317bf-165">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="317bf-165">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="317bf-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="317bf-166">NOTES</span></span>
* <span data-ttu-id="317bf-167">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="317bf-167">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="317bf-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="317bf-168">RELATED LINKS</span></span>

[<span data-ttu-id="317bf-169">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="317bf-169">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="317bf-170">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="317bf-170">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="317bf-171">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="317bf-171">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="317bf-172">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="317bf-172">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


