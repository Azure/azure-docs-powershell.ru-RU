---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078824"
---
# <span data-ttu-id="97e04-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97e04-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="97e04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97e04-102">SYNOPSIS</span></span>
<span data-ttu-id="97e04-103">Обновляет конфигурацию IP-сети для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="97e04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97e04-104">SYNTAX</span></span>

### <span data-ttu-id="97e04-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97e04-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97e04-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="97e04-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97e04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97e04-107">DESCRIPTION</span></span>
<span data-ttu-id="97e04-108">Командлет **Set-AzNetworkInterfaceIpConfig** ОБНОВЛЯЕТ конфигурацию IP для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="97e04-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97e04-109">EXAMPLES</span></span>

### <span data-ttu-id="97e04-110">1: изменение IP-адреса конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="97e04-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="97e04-111">Первые две команды получают виртуальную сеть под названием myvnet и подсеть под названием mysubnet и хранят их в переменных $vnet и $subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="97e04-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="97e04-112">Третья команда получает сетевой интерфейс NIC1, связанный с IP-конфигурацией, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="97e04-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="97e04-113">Третья команда задает для частного IP-адреса основного IP-конфигурации ipconfig1 значение 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="97e04-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="97e04-114">Наконец, последняя команда обновляет сетевой интерфейс, гарантируя, что изменения были выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="97e04-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="97e04-115">2. Сопоставление конфигурации IP с группой безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="97e04-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="97e04-116">В этом примере переменная $asg включает ссылку на группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="97e04-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="97e04-117">Четвертая команда получает сетевой интерфейс NIC1, связанный с IP-конфигурацией, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="97e04-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="97e04-118">Set-AzNetworkInterfaceIpConfig задает для частного IP-адреса основного IP-конфигурации ipconfig1 10.0.0.11 и создает связь с полученной Группой безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="97e04-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="97e04-119">Наконец, последняя команда обновляет сетевой интерфейс, гарантируя, что изменения были выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="97e04-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="97e04-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97e04-120">PARAMETERS</span></span>

### <span data-ttu-id="97e04-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97e04-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="97e04-122">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97e04-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="97e04-124">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="97e04-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="97e04-126">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="97e04-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="97e04-128">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e04-129">-DefaultProfile</span></span>
<span data-ttu-id="97e04-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97e04-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97e04-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="97e04-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="97e04-132">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="97e04-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="97e04-134">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="97e04-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="97e04-136">Указывает коллекцию ссылок на правила преобразования сетевых адресов (NAT) для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="97e04-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="97e04-138">Задает коллекцию ссылок на правила NAT для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="97e04-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97e04-139">-Name</span></span>
<span data-ttu-id="97e04-140">Указывает имя конфигурации IP-сети, которую этот командлет задает.</span><span class="sxs-lookup"><span data-stu-id="97e04-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="97e04-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="97e04-141">-NetworkInterface</span></span>
<span data-ttu-id="97e04-142">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="97e04-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="97e04-143">Этот командлет добавляет IP-конфигурацию сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="97e04-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="97e04-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="97e04-144">-Primary</span></span>
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

### <span data-ttu-id="97e04-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="97e04-145">-PrivateIpAddress</span></span>
<span data-ttu-id="97e04-146">Задает статический IP-адрес IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="97e04-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="97e04-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="97e04-148">Определяет версию IP-адреса конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="97e04-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="97e04-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97e04-150">IPv6</span><span class="sxs-lookup"><span data-stu-id="97e04-150">IPv4</span></span>
- <span data-ttu-id="97e04-151">IPv</span><span class="sxs-lookup"><span data-stu-id="97e04-151">IPv6</span></span>

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

### <span data-ttu-id="97e04-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="97e04-152">-PublicIpAddress</span></span>
<span data-ttu-id="97e04-153">Указывает объект **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="97e04-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="97e04-154">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="97e04-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="97e04-155">-PublicIpAddressId</span></span>
<span data-ttu-id="97e04-156">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="97e04-157">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="97e04-157">-Subnet</span></span>
<span data-ttu-id="97e04-158">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="97e04-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="97e04-159">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="97e04-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="97e04-160">-SubnetId</span></span>
<span data-ttu-id="97e04-161">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97e04-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="97e04-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e04-162">CommonParameters</span></span>
<span data-ttu-id="97e04-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97e04-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e04-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97e04-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e04-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97e04-165">INPUTS</span></span>

### <span data-ttu-id="97e04-166">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="97e04-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="97e04-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="97e04-167">System.String[]</span></span>

### <span data-ttu-id="97e04-168">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="97e04-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="97e04-169">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="97e04-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="97e04-170">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="97e04-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="97e04-171">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="97e04-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="97e04-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97e04-172">OUTPUTS</span></span>

### <span data-ttu-id="97e04-173">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="97e04-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="97e04-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="97e04-174">NOTES</span></span>
* <span data-ttu-id="97e04-175">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="97e04-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="97e04-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97e04-176">RELATED LINKS</span></span>

[<span data-ttu-id="97e04-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97e04-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="97e04-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97e04-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="97e04-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97e04-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="97e04-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="97e04-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)