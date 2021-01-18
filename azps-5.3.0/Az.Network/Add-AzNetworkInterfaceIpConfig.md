---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9fef4a3cfe57b75ad992d4f4068bb0d51bbdcd90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506149"
---
# <span data-ttu-id="875ae-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="875ae-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="875ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="875ae-102">SYNOPSIS</span></span>
<span data-ttu-id="875ae-103">Добавляет конфигурацию IP-интерфейса в сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="875ae-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="875ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="875ae-104">SYNTAX</span></span>

### <span data-ttu-id="875ae-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="875ae-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="875ae-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="875ae-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="875ae-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="875ae-107">DESCRIPTION</span></span>
<span data-ttu-id="875ae-108">Командлет **Add-AzNetworkInterfaceIpConfig** добавляет конфигурацию IP-интерфейса сетевого интерфейса в сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="875ae-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="875ae-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="875ae-109">EXAMPLES</span></span>

### <span data-ttu-id="875ae-110">Пример 1. Добавление новой конфигурации IP-адреса с группой безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="875ae-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="875ae-111">В этом примере мы создали новый сетевой интерфейс MyNetworkInterface, который принадлежит подсети в новой виртуальной сети MyVNET.</span><span class="sxs-lookup"><span data-stu-id="875ae-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="875ae-112">Мы также создадим пустую группу безопасности приложений MyASG, которая будет связываться с конфигурациями IP-адресов в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="875ae-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="875ae-113">После создания обоих объектов мы связываем стандартную конфигурацию IP-адреса с объектом MyASG.</span><span class="sxs-lookup"><span data-stu-id="875ae-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="875ae-114">Наконец, мы создадим новую конфигурацию IP-адреса в сетевом интерфейсе, связанную с объектом группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="875ae-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="875ae-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="875ae-115">PARAMETERS</span></span>

### <span data-ttu-id="875ae-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="875ae-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="875ae-117">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-118">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="875ae-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="875ae-119">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="875ae-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="875ae-121">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-122">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="875ae-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="875ae-123">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875ae-124">-DefaultProfile</span></span>
<span data-ttu-id="875ae-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="875ae-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="875ae-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="875ae-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="875ae-127">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-128">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="875ae-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="875ae-129">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-130">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="875ae-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="875ae-131">Набор ссылок на правила перевода сетевых адресов (NAT), к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-132">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="875ae-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="875ae-133">Набор ссылок на входящие правила NAT для балансиров нагрузки, к которым относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="875ae-134">-Name</span><span class="sxs-lookup"><span data-stu-id="875ae-134">-Name</span></span>
<span data-ttu-id="875ae-135">Указывает имя конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="875ae-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="875ae-136">-NetworkInterface</span></span>
<span data-ttu-id="875ae-137">Определяет объект **NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="875ae-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="875ae-138">Этот cmdlet добавляет конфигурацию IP-адреса сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="875ae-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="875ae-139">-Primary</span><span class="sxs-lookup"><span data-stu-id="875ae-139">-Primary</span></span>
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

### <span data-ttu-id="875ae-140">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="875ae-140">-PrivateIpAddress</span></span>
<span data-ttu-id="875ae-141">Определяет статический IP-адрес конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="875ae-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="875ae-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="875ae-143">Указывает версию IP-адреса конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="875ae-144">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="875ae-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="875ae-145">IPv4</span><span class="sxs-lookup"><span data-stu-id="875ae-145">IPv4</span></span>
- <span data-ttu-id="875ae-146">IPv6</span><span class="sxs-lookup"><span data-stu-id="875ae-146">IPv6</span></span>

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

### <span data-ttu-id="875ae-147">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="875ae-147">-PublicIpAddress</span></span>
<span data-ttu-id="875ae-148">Указывает объект **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="875ae-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="875ae-149">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="875ae-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="875ae-150">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="875ae-150">-PublicIpAddressId</span></span>
<span data-ttu-id="875ae-151">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="875ae-152">-Subnet</span><span class="sxs-lookup"><span data-stu-id="875ae-152">-Subnet</span></span>
<span data-ttu-id="875ae-153">Указывает объект **подсети.**</span><span class="sxs-lookup"><span data-stu-id="875ae-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="875ae-154">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="875ae-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="875ae-155">-SubnetId</span></span>
<span data-ttu-id="875ae-156">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="875ae-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="875ae-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875ae-157">CommonParameters</span></span>
<span data-ttu-id="875ae-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="875ae-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875ae-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="875ae-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875ae-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="875ae-160">INPUTS</span></span>

### <span data-ttu-id="875ae-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="875ae-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="875ae-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="875ae-162">System.String[]</span></span>

### <span data-ttu-id="875ae-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="875ae-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="875ae-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="875ae-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="875ae-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="875ae-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="875ae-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="875ae-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="875ae-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="875ae-167">OUTPUTS</span></span>

### <span data-ttu-id="875ae-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="875ae-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="875ae-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="875ae-169">NOTES</span></span>
* <span data-ttu-id="875ae-170">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="875ae-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="875ae-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="875ae-171">RELATED LINKS</span></span>

[<span data-ttu-id="875ae-172">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="875ae-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="875ae-173">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="875ae-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="875ae-174">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="875ae-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="875ae-175">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="875ae-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
