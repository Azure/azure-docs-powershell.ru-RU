---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223537"
---
# <span data-ttu-id="2a976-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a976-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="2a976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a976-102">SYNOPSIS</span></span>
<span data-ttu-id="2a976-103">Обновляет конфигурацию IP-адреса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="2a976-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a976-104">SYNTAX</span></span>

### <span data-ttu-id="2a976-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a976-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a976-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a976-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a976-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a976-107">DESCRIPTION</span></span>
<span data-ttu-id="2a976-108">Командлет **Set-AzNetworkInterfaceIpConfig** обновляет конфигурацию IP-адреса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="2a976-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a976-109">EXAMPLES</span></span>

### <span data-ttu-id="2a976-110">1. Изменение IP-адреса конфигурации IP-адреса</span><span class="sxs-lookup"><span data-stu-id="2a976-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2a976-111">Первые две команды получают виртуальную сеть подсети под названием myvnet и подсеть подсети mysubnet и хранят ее в переменных, $vnet и $subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="2a976-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="2a976-112">Третья команда получает сетевой интерфейс nic1, связанный с конфигурацией IP,которая должна быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="2a976-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="2a976-113">Третья команда задает частный IP-адрес для основного IP-адреса конфигурации IPconfig1 в качестве 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="2a976-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="2a976-114">Наконец, последняя команда обновляет сетевой интерфейс, обеспечивая успешное внесение изменений.</span><span class="sxs-lookup"><span data-stu-id="2a976-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="2a976-115">2. Связывание конфигурации IP-адреса с группой безопасности приложения</span><span class="sxs-lookup"><span data-stu-id="2a976-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="2a976-116">В этом примере переменная $asg содержит ссылку на группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="2a976-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="2a976-117">Четвертая команда получает сетевой интерфейс nic1, связанный с конфигурацией IP,которая должна быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="2a976-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="2a976-118">При Set-AzNetworkInterfaceIpConfig ipconfig1 основного IP-адреса конфигурации ipconfig1 устанавливается 10.0.0.11 и создается связь с извлеченной группой безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="2a976-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="2a976-119">Наконец, последняя команда обновляет сетевой интерфейс, обеспечивая успешное внесение изменений.</span><span class="sxs-lookup"><span data-stu-id="2a976-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="2a976-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a976-120">PARAMETERS</span></span>

### <span data-ttu-id="2a976-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a976-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="2a976-122">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a976-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="2a976-124">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a976-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="2a976-126">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2a976-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="2a976-128">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a976-129">-DefaultProfile</span></span>
<span data-ttu-id="2a976-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a976-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a976-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a976-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="2a976-132">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a976-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="2a976-134">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="2a976-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="2a976-136">Набор ссылок на правила перевода сетевых адресов (NAT), к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="2a976-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="2a976-138">Набор ссылок на входящие правила NAT для балансиров нагрузки, к которым относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="2a976-139">-Name</span><span class="sxs-lookup"><span data-stu-id="2a976-139">-Name</span></span>
<span data-ttu-id="2a976-140">Задает имя конфигурации IP-адреса сети, для которой этот cmdlet sets.</span><span class="sxs-lookup"><span data-stu-id="2a976-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="2a976-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a976-141">-NetworkInterface</span></span>
<span data-ttu-id="2a976-142">Определяет объект **NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="2a976-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="2a976-143">Этот cmdlet добавляет конфигурацию IP-адреса сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="2a976-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a976-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="2a976-144">-Primary</span></span>
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

### <span data-ttu-id="2a976-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a976-145">-PrivateIpAddress</span></span>
<span data-ttu-id="2a976-146">Определяет статический IP-адрес конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="2a976-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2a976-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="2a976-148">Указывает версию IP-адреса конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="2a976-149">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="2a976-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a976-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="2a976-150">IPv4</span></span>
- <span data-ttu-id="2a976-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="2a976-151">IPv6</span></span>

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

### <span data-ttu-id="2a976-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a976-152">-PublicIpAddress</span></span>
<span data-ttu-id="2a976-153">Указывает объект **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="2a976-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="2a976-154">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="2a976-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2a976-155">-PublicIpAddressId</span></span>
<span data-ttu-id="2a976-156">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="2a976-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="2a976-157">-Subnet</span></span>
<span data-ttu-id="2a976-158">Указывает объект **подсети.**</span><span class="sxs-lookup"><span data-stu-id="2a976-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="2a976-159">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="2a976-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2a976-160">-SubnetId</span></span>
<span data-ttu-id="2a976-161">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2a976-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="2a976-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a976-162">CommonParameters</span></span>
<span data-ttu-id="2a976-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a976-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a976-164">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a976-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a976-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a976-165">INPUTS</span></span>

### <span data-ttu-id="2a976-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a976-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="2a976-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2a976-167">System.String[]</span></span>

### <span data-ttu-id="2a976-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="2a976-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="2a976-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="2a976-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="2a976-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="2a976-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="2a976-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="2a976-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="2a976-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a976-172">OUTPUTS</span></span>

### <span data-ttu-id="2a976-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a976-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2a976-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a976-174">NOTES</span></span>
* <span data-ttu-id="2a976-175">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="2a976-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2a976-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a976-176">RELATED LINKS</span></span>

[<span data-ttu-id="2a976-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a976-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2a976-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a976-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2a976-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a976-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="2a976-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2a976-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
