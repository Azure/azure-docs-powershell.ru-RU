---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9427a79c607d56fcc9ce7a39fa24bfa3e301cfc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003384"
---
# <span data-ttu-id="592af-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="592af-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="592af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="592af-102">SYNOPSIS</span></span>
<span data-ttu-id="592af-103">Обновляет конфигурацию IP-адреса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="592af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="592af-104">SYNTAX</span></span>

### <span data-ttu-id="592af-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="592af-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="592af-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="592af-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592af-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="592af-107">DESCRIPTION</span></span>
<span data-ttu-id="592af-108">Командлет **Set-AzNetworkInterfaceIpConfig** обновляет конфигурацию IP-адреса для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="592af-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="592af-109">EXAMPLES</span></span>

### <span data-ttu-id="592af-110">1. Изменение IP-адреса конфигурации IP-адреса</span><span class="sxs-lookup"><span data-stu-id="592af-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="592af-111">Первые две команды получают виртуальную сеть подсети под названием myvnet и подсеть подсети mysubnet и хранят ее в переменных, $vnet и $subnet соответственно.</span><span class="sxs-lookup"><span data-stu-id="592af-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="592af-112">Третья команда получает сетевой интерфейс nic1, связанный с конфигурацией IP,которая должна быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="592af-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="592af-113">Третья команда задает личный IP-адрес основного IP-конфигурации ipconfig1 с 10.0.0.11.</span><span class="sxs-lookup"><span data-stu-id="592af-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="592af-114">Наконец, последняя команда обновляет сетевой интерфейс, обеспечивая успешное внесение изменений.</span><span class="sxs-lookup"><span data-stu-id="592af-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="592af-115">2. Связывание конфигурации IP-адреса с группой безопасности приложения</span><span class="sxs-lookup"><span data-stu-id="592af-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="592af-116">В этом примере переменная $asg содержит ссылку на группу безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="592af-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="592af-117">Четвертая команда получает сетевой интерфейс nic1, связанный с конфигурацией IP-адреса, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="592af-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="592af-118">Этот Set-AzNetworkInterfaceIpConfig задает частный IP-адрес основного IP-адреса конфигурации ipconfig1 10.0.0.11 и создает связь с извлеченной группой безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="592af-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="592af-119">Наконец, последняя команда обновляет сетевой интерфейс, обеспечивая успешное внесение изменений.</span><span class="sxs-lookup"><span data-stu-id="592af-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="592af-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="592af-120">PARAMETERS</span></span>

### <span data-ttu-id="592af-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="592af-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="592af-122">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-123">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="592af-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="592af-124">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="592af-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="592af-126">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-127">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="592af-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="592af-128">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592af-129">-DefaultProfile</span></span>
<span data-ttu-id="592af-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="592af-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="592af-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="592af-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="592af-132">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-133">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="592af-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="592af-134">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-135">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="592af-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="592af-136">Набор ссылок на правила перевода сетевых адресов (NAT) для балансиров нагрузки, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-137">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="592af-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="592af-138">Набор ссылок на входящие правила NAT для балансиров нагрузки, к которым относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="592af-139">-Name</span><span class="sxs-lookup"><span data-stu-id="592af-139">-Name</span></span>
<span data-ttu-id="592af-140">Задает имя конфигурации IP-адреса сети, для которой задан этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592af-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="592af-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="592af-141">-NetworkInterface</span></span>
<span data-ttu-id="592af-142">Определяет объект **NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="592af-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="592af-143">Этот cmdlet добавляет конфигурацию IP-адреса сетевого интерфейса к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="592af-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="592af-144">-Primary</span><span class="sxs-lookup"><span data-stu-id="592af-144">-Primary</span></span>
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

### <span data-ttu-id="592af-145">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="592af-145">-PrivateIpAddress</span></span>
<span data-ttu-id="592af-146">Определяет статический IP-адрес конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="592af-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="592af-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="592af-148">Указывает версию IP-адреса конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="592af-149">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="592af-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="592af-150">IPv4</span><span class="sxs-lookup"><span data-stu-id="592af-150">IPv4</span></span>
- <span data-ttu-id="592af-151">IPv6</span><span class="sxs-lookup"><span data-stu-id="592af-151">IPv6</span></span>

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

### <span data-ttu-id="592af-152">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="592af-152">-PublicIpAddress</span></span>
<span data-ttu-id="592af-153">Указывает объект **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="592af-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="592af-154">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="592af-155">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="592af-155">-PublicIpAddressId</span></span>
<span data-ttu-id="592af-156">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="592af-157">-Subnet</span><span class="sxs-lookup"><span data-stu-id="592af-157">-Subnet</span></span>
<span data-ttu-id="592af-158">Указывает объект **подсети.**</span><span class="sxs-lookup"><span data-stu-id="592af-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="592af-159">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="592af-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="592af-160">-SubnetId</span></span>
<span data-ttu-id="592af-161">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="592af-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="592af-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592af-162">CommonParameters</span></span>
<span data-ttu-id="592af-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592af-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592af-164">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="592af-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592af-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="592af-165">INPUTS</span></span>

### <span data-ttu-id="592af-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="592af-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="592af-167">System.String[]</span><span class="sxs-lookup"><span data-stu-id="592af-167">System.String[]</span></span>

### <span data-ttu-id="592af-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="592af-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="592af-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="592af-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="592af-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="592af-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="592af-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="592af-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="592af-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="592af-172">OUTPUTS</span></span>

### <span data-ttu-id="592af-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="592af-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="592af-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="592af-174">NOTES</span></span>
* <span data-ttu-id="592af-175">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="592af-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="592af-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="592af-176">RELATED LINKS</span></span>

[<span data-ttu-id="592af-177">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="592af-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="592af-178">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="592af-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="592af-179">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="592af-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="592af-180">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="592af-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
