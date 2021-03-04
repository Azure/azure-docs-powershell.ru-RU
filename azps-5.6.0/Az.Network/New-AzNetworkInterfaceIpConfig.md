---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 72d2439e66245e8469e440cb5e501cd9e9379fa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953939"
---
# <span data-ttu-id="7611f-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7611f-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="7611f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7611f-102">SYNOPSIS</span></span>
<span data-ttu-id="7611f-103">Создает конфигурацию IP-интерфейса сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="7611f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7611f-104">SYNTAX</span></span>

### <span data-ttu-id="7611f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7611f-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7611f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7611f-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7611f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7611f-107">DESCRIPTION</span></span>
<span data-ttu-id="7611f-108">Командлет **New-AzNetworkInterfaceIpConfig** создает конфигурацию IP-интерфейса сетевого интерфейса Azure для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="7611f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7611f-109">EXAMPLES</span></span>

### <span data-ttu-id="7611f-110">1. Создание конфигурации IP-адреса с общедоступным IP-адресом для интерфейса сети</span><span class="sxs-lookup"><span data-stu-id="7611f-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="7611f-111">Первые две команды получают виртуальную сеть под названием myvnet и подсеть подсети под названием mysubnet соответственно, которая была создана ранее.</span><span class="sxs-lookup"><span data-stu-id="7611f-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="7611f-112">Они хранятся в $vnet и $Subnet данных.</span><span class="sxs-lookup"><span data-stu-id="7611f-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="7611f-113">Третья команда получает ранее созданный общедоступный IP-адрес под названием PIP1.</span><span class="sxs-lookup"><span data-stu-id="7611f-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="7611f-114">Данная команда создает новую конфигурацию IP-адреса под названием "IPConfig-1" в качестве основной конфигурации IP-адреса с общедоступным IP-адресом, связанным с ней.</span><span class="sxs-lookup"><span data-stu-id="7611f-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="7611f-115">Затем с помощью этой конфигурации IP-адреса создается сетевой интерфейс mynic1.</span><span class="sxs-lookup"><span data-stu-id="7611f-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="7611f-116">2. Создание конфигурации IP-адреса с закрытым IP-адресом</span><span class="sxs-lookup"><span data-stu-id="7611f-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="7611f-117">Первые две команды получают виртуальную сеть под названием myvnet и подсеть подсети под названием mysubnet соответственно, которая была создана ранее.</span><span class="sxs-lookup"><span data-stu-id="7611f-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="7611f-118">Они хранятся в $vnet и $Subnet данных.</span><span class="sxs-lookup"><span data-stu-id="7611f-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="7611f-119">Третья команда создает новую конфигурацию IP-адреса под названием "IPConfig-2" с закрытым IP-адресом 10.0.0.5, связанным с ним.</span><span class="sxs-lookup"><span data-stu-id="7611f-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="7611f-120">Затем с помощью этой конфигурации IP-адреса создается сетевой интерфейс mynic1.</span><span class="sxs-lookup"><span data-stu-id="7611f-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="7611f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7611f-121">PARAMETERS</span></span>

### <span data-ttu-id="7611f-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7611f-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7611f-123">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7611f-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7611f-125">Набор ссылок на пул адресов backend шлюза приложений, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7611f-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7611f-127">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7611f-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7611f-129">Набор ссылок на группы безопасности приложений, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7611f-130">-DefaultProfile</span></span>
<span data-ttu-id="7611f-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7611f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7611f-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7611f-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7611f-133">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-134">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7611f-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7611f-135">Набор ссылок на пул адресов для балансиров нагрузки, к которому относится эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-136">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7611f-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7611f-137">Набор ссылок на входящие правила NAT для балансиента нагрузки, к которым принадлежит это сетевое правило IPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7611f-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="7611f-138">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7611f-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7611f-139">Набор ссылок на правила перевода сетевых адресов (NAT) для балансиров нагрузки, к которым принадлежит эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="7611f-140">-Name</span><span class="sxs-lookup"><span data-stu-id="7611f-140">-Name</span></span>
<span data-ttu-id="7611f-141">Указывает имя конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-141">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="7611f-142">-Primary</span><span class="sxs-lookup"><span data-stu-id="7611f-142">-Primary</span></span>
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

### <span data-ttu-id="7611f-143">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7611f-143">-PrivateIpAddress</span></span>
<span data-ttu-id="7611f-144">Определяет статический IP-адрес конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="7611f-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7611f-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7611f-146">Указывает версию IP-адреса конфигурации IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="7611f-147">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="7611f-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7611f-148">IPv4</span><span class="sxs-lookup"><span data-stu-id="7611f-148">IPv4</span></span>
- <span data-ttu-id="7611f-149">IPv6</span><span class="sxs-lookup"><span data-stu-id="7611f-149">IPv6</span></span>

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

### <span data-ttu-id="7611f-150">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7611f-150">-PublicIpAddress</span></span>
<span data-ttu-id="7611f-151">Указывает объект **PublicIPAddress.**</span><span class="sxs-lookup"><span data-stu-id="7611f-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="7611f-152">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7611f-153">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7611f-153">-PublicIpAddressId</span></span>
<span data-ttu-id="7611f-154">Этот cmdlet создает ссылку на общедоступный IP-адрес, который связывается с этой конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="7611f-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7611f-155">-Subnet</span></span>
<span data-ttu-id="7611f-156">Указывает объект **подсети.**</span><span class="sxs-lookup"><span data-stu-id="7611f-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7611f-157">Этот cmdlet создает ссылку на подсеть, в которой создается конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7611f-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7611f-158">-SubnetId</span></span>
<span data-ttu-id="7611f-159">Указывает ссылку на подсеть, в которой создается эта конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7611f-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="7611f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7611f-160">CommonParameters</span></span>
<span data-ttu-id="7611f-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7611f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7611f-162">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7611f-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7611f-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7611f-163">INPUTS</span></span>

### <span data-ttu-id="7611f-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7611f-164">System.String[]</span></span>

### <span data-ttu-id="7611f-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="7611f-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="7611f-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="7611f-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="7611f-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="7611f-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="7611f-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="7611f-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="7611f-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7611f-169">OUTPUTS</span></span>

### <span data-ttu-id="7611f-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7611f-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="7611f-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7611f-171">NOTES</span></span>
* <span data-ttu-id="7611f-172">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="7611f-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7611f-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7611f-173">RELATED LINKS</span></span>

[<span data-ttu-id="7611f-174">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7611f-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7611f-175">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7611f-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7611f-176">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7611f-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="7611f-177">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7611f-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
