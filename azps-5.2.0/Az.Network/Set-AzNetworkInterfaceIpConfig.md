---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322745"
---
# <span data-ttu-id="54983-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54983-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="54983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54983-102">SYNOPSIS</span></span>
<span data-ttu-id="54983-103">Обновляет конфигурацию IP-адреса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="54983-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54983-104">SYNTAX</span></span>

### <span data-ttu-id="54983-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54983-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54983-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="54983-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54983-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54983-107">DESCRIPTION</span></span>
<span data-ttu-id="54983-108">Командлет **Set-AzNetworkInterfaceIpConfig** обновляет конфигурацию IP-адреса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="54983-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54983-109">EXAMPLES</span></span>

### <span data-ttu-id="54983-110">1. Изменение IP-адреса конфигурации IP-адреса</span><span class="sxs-lookup"><span data-stu-id="54983-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="54983-111">Первые две команды получают виртуальную сеть подсети под названием myvnet и подсеть подсети mysubnet и хранят ее в переменных, $vnet и $subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="54983-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="54983-112">Третья команда получает сетевой интерфейс nic1, связанный с конфигурацией IP,которая должна быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="54983-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="54983-113">Третья команда задает частный IP-адрес для основного IP-адреса конфигурации IPconfig1 в качестве 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="54983-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="54983-114">Наконец, последняя команда обновляет интерфейс сети, обеспечивая успешное внесение изменений.</span><span class="sxs-lookup"><span data-stu-id="54983-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="54983-115">2. Связывание конфигурации IP-адреса с группой безопасности приложения</span><span class="sxs-lookup"><span data-stu-id="54983-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="54983-116">В этом примере переменная $asg содержит ссылку на группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="54983-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="54983-117">Четвертая команда получает сетевой интерфейс nic1, связанный с конфигурацией IP-адреса, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="54983-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="54983-118">Этот Set-AzNetworkInterfaceIpConfig задает частный IP-адрес основного IP-адреса конфигурации ipconfig1 10.0.0.11 и создает связь с извлеченной группой безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="54983-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="54983-119">Наконец, последняя команда обновляет интерфейс сети, обеспечивая успешное внесение изменений.</span><span class="sxs-lookup"><span data-stu-id="54983-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="54983-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54983-120">PARAMETERS</span></span>

### <span data-ttu-id="54983-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="54983-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="54983-122">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="54983-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="54983-124">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="54983-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="54983-126">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="54983-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="54983-128">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54983-129">-DefaultProfile</span></span>
<span data-ttu-id="54983-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54983-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54983-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="54983-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="54983-132">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="54983-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="54983-134">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="54983-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="54983-136">Набор ссылок на правила перевода сетевых адресов (NAT), к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="54983-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="54983-138">Набор ссылок на входящие правила NAT балансиров нагрузки, к которым относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="54983-139">-Name</span><span class="sxs-lookup"><span data-stu-id="54983-139">-Name</span></span>
<span data-ttu-id="54983-140">Задает имя конфигурации IP-адреса сети, для которой задан этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54983-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="54983-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54983-141">-NetworkInterface</span></span>
<span data-ttu-id="54983-142">Определяет объект **NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="54983-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="54983-143">Этот cmdlet добавляет конфигурацию IP-адреса сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="54983-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="54983-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="54983-144">-Primary</span></span>
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

### <span data-ttu-id="54983-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="54983-145">-PrivateIpAddress</span></span>
<span data-ttu-id="54983-146">Определяет статический IP-адрес конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="54983-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="54983-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="54983-148">Указывает версию IP-адреса конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="54983-149">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="54983-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54983-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="54983-150">IPv4</span></span>
- <span data-ttu-id="54983-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="54983-151">IPv6</span></span>

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

### <span data-ttu-id="54983-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54983-152">-PublicIpAddress</span></span>
<span data-ttu-id="54983-153">Указывает объект **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="54983-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="54983-154">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="54983-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="54983-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="54983-155">-PublicIpAddressId</span></span>
<span data-ttu-id="54983-156">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="54983-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="54983-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="54983-157">-Subnet</span></span>
<span data-ttu-id="54983-158">Указывает объект **подсети.**</span><span class="sxs-lookup"><span data-stu-id="54983-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="54983-159">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="54983-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="54983-160">-SubnetId</span></span>
<span data-ttu-id="54983-161">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54983-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="54983-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54983-162">CommonParameters</span></span>
<span data-ttu-id="54983-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54983-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54983-164">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54983-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54983-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54983-165">INPUTS</span></span>

### <span data-ttu-id="54983-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54983-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="54983-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="54983-167">System.String[]</span></span>

### <span data-ttu-id="54983-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="54983-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="54983-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="54983-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="54983-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="54983-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="54983-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="54983-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="54983-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54983-172">OUTPUTS</span></span>

### <span data-ttu-id="54983-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="54983-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="54983-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54983-174">NOTES</span></span>
* <span data-ttu-id="54983-175">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="54983-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="54983-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54983-176">RELATED LINKS</span></span>

[<span data-ttu-id="54983-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54983-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54983-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54983-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54983-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54983-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="54983-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="54983-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
