---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8804fd7fd9e2ea1d784d2b1607f72e7e0aa1bb6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556591"
---
# <span data-ttu-id="74c9f-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="74c9f-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="74c9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="74c9f-103">Задает состояние цели для IP-конфигурации сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="74c9f-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74c9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74c9f-104">SYNTAX</span></span>

### <span data-ttu-id="74c9f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74c9f-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74c9f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74c9f-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74c9f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74c9f-107">DESCRIPTION</span></span>
<span data-ttu-id="74c9f-108">Командлет **Set-AzureRmNetworkInterfaceIpConfig** задает состояние цели для IP-конфигурации сетевого интерфейса Azure.</span><span class="sxs-lookup"><span data-stu-id="74c9f-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="74c9f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74c9f-109">EXAMPLES</span></span>

### <span data-ttu-id="74c9f-110">1: изменение IP-адреса конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="74c9f-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="74c9f-111">Первые две команды получают виртуальную сеть под названием myvnet и подсеть под названием mysubnet и хранят их в переменных $vnet и $subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="74c9f-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="74c9f-112">Третья команда получает сетевой интерфейс NIC1, связанный с IP-конфигурацией, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="74c9f-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="74c9f-113">Третья команда задает для частного IP-адреса основного IP-конфигурации ipconfig1 значение 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="74c9f-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="74c9f-114">Наконец, последняя команда обновляет сетевой интерфейс, гарантируя, что изменения были выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="74c9f-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="74c9f-115">2. Сопоставление конфигурации IP с группой безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="74c9f-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="74c9f-116">В этом примере переменная $asg включает ссылку на группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="74c9f-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="74c9f-117">Четвертая команда получает сетевой интерфейс NIC1, связанный с IP-конфигурацией, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="74c9f-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="74c9f-118">Set-AzureRmNetworkInterfaceIpConfig задает для частного IP-адреса основного IP-конфигурации ipconfig1 10.0.0.11 и создает связь с полученной Группой безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="74c9f-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="74c9f-119">Наконец, последняя команда обновляет сетевой интерфейс, гарантируя, что изменения были выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="74c9f-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="74c9f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74c9f-120">PARAMETERS</span></span>

### <span data-ttu-id="74c9f-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="74c9f-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="74c9f-122">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="74c9f-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="74c9f-124">Указывает коллекцию ссылок на пул серверных адресов для шлюза приложений, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="74c9f-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="74c9f-126">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="74c9f-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="74c9f-128">Указывает коллекцию ссылок на группы безопасности приложения, к которой относится эта конфигурация IP сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c9f-129">-DefaultProfile</span></span>
<span data-ttu-id="74c9f-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74c9f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c9f-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="74c9f-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="74c9f-132">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="74c9f-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="74c9f-134">Указывает коллекцию ссылок на пул серверной адресной системы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="74c9f-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="74c9f-136">Указывает коллекцию ссылок на правила преобразования сетевых адресов (NAT) для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="74c9f-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="74c9f-138">Задает коллекцию ссылок на правила NAT для подсистемы балансировки нагрузки, к которой относится эта IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="74c9f-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74c9f-139">-Name</span></span>
<span data-ttu-id="74c9f-140">Указывает имя конфигурации IP-сети, которую этот командлет задает.</span><span class="sxs-lookup"><span data-stu-id="74c9f-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="74c9f-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="74c9f-141">-NetworkInterface</span></span>
<span data-ttu-id="74c9f-142">Указывает объект **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="74c9f-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="74c9f-143">Этот командлет добавляет IP-конфигурацию сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="74c9f-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="74c9f-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="74c9f-144">-Primary</span></span>
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

### <span data-ttu-id="74c9f-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="74c9f-145">-PrivateIpAddress</span></span>
<span data-ttu-id="74c9f-146">Задает статический IP-адрес IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="74c9f-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="74c9f-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="74c9f-148">Определяет версию IP-адреса конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="74c9f-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="74c9f-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="74c9f-150">IPv6</span><span class="sxs-lookup"><span data-stu-id="74c9f-150">IPv4</span></span>
- <span data-ttu-id="74c9f-151">IPv</span><span class="sxs-lookup"><span data-stu-id="74c9f-151">IPv6</span></span>

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

### <span data-ttu-id="74c9f-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="74c9f-152">-PublicIpAddress</span></span>
<span data-ttu-id="74c9f-153">Указывает объект **PublicIPAddress** .</span><span class="sxs-lookup"><span data-stu-id="74c9f-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="74c9f-154">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="74c9f-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="74c9f-155">-PublicIpAddressId</span></span>
<span data-ttu-id="74c9f-156">Этот командлет создает ссылку на общедоступный IP-адрес, который нужно связать с этой IP-конфигурацией сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="74c9f-157">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="74c9f-157">-Subnet</span></span>
<span data-ttu-id="74c9f-158">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="74c9f-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="74c9f-159">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="74c9f-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="74c9f-160">-SubnetId</span></span>
<span data-ttu-id="74c9f-161">Этот командлет создает ссылку на подсеть, в которой создана IP-конфигурация сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="74c9f-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="74c9f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c9f-162">CommonParameters</span></span>
<span data-ttu-id="74c9f-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74c9f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c9f-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74c9f-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c9f-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74c9f-165">INPUTS</span></span>

### <span data-ttu-id="74c9f-166">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="74c9f-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="74c9f-167">Параметры: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74c9f-167">Parameters: NetworkInterface (ByValue)</span></span>

### <span data-ttu-id="74c9f-168">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="74c9f-168">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="74c9f-169">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="74c9f-169">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="74c9f-170">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSInboundNatRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="74c9f-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="74c9f-171">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="74c9f-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="74c9f-172">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="74c9f-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="74c9f-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74c9f-173">OUTPUTS</span></span>

### <span data-ttu-id="74c9f-174">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="74c9f-174">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="74c9f-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="74c9f-175">NOTES</span></span>
* <span data-ttu-id="74c9f-176">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="74c9f-176">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="74c9f-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74c9f-177">RELATED LINKS</span></span>

[<span data-ttu-id="74c9f-178">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="74c9f-178">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="74c9f-179">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="74c9f-179">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="74c9f-180">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="74c9f-180">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="74c9f-181">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="74c9f-181">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


