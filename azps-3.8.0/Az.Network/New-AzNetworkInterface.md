---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066606"
---
# <span data-ttu-id="8a89c-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a89c-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="8a89c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a89c-102">SYNOPSIS</span></span>
<span data-ttu-id="8a89c-103">Создание сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-103">Creates a network interface.</span></span>

## <span data-ttu-id="8a89c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a89c-104">SYNTAX</span></span>

### <span data-ttu-id="8a89c-105">SetByIpConfigurationResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a89c-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a89c-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="8a89c-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a89c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a89c-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a89c-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8a89c-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a89c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a89c-109">DESCRIPTION</span></span>
<span data-ttu-id="8a89c-110">Командлет **New-AzNetworkInterface** создает сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="8a89c-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="8a89c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a89c-111">EXAMPLES</span></span>

### <span data-ttu-id="8a89c-112">Пример 1: создание сетевого интерфейса Azure</span><span class="sxs-lookup"><span data-stu-id="8a89c-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="8a89c-113">Эта команда создает сетевой интерфейс с именем NetworkInterface001 и динамически назначенный частный IP-адрес из Subnet1 в виртуальной сети с именем VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="8a89c-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="8a89c-114">Команда также назначает двум DNS-серверам сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8a89c-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="8a89c-115">Дочерний ресурс IP, который будет создан автоматически с использованием имени IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="8a89c-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="8a89c-116">Пример 2: создание сетевого интерфейса Azure с помощью объекта конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="8a89c-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="8a89c-117">В этом примере создается новый сетевой интерфейс с помощью объекта конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="8a89c-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="8a89c-118">Объект Configuration IP задает статический частный IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="8a89c-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="8a89c-119">Первая команда извлекает текущую указанную виртуальную сеть, используемую для назначения подсети во второй команде.</span><span class="sxs-lookup"><span data-stu-id="8a89c-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="8a89c-120">Вторая команда создает IP-конфигурацию сетевого интерфейса с именем IPConfig1 и сохраняет конфигурацию в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="8a89c-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="8a89c-121">Третья команда создает сетевой интерфейс с именем NetworkInterface1, который использует IP-конфигурацию сетевого интерфейса, хранящуюся в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="8a89c-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="8a89c-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a89c-122">PARAMETERS</span></span>

### <span data-ttu-id="8a89c-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8a89c-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="8a89c-124">Указывает объект **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8a89c-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8a89c-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8a89c-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="8a89c-126">Указывает идентификатор объекта **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8a89c-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8a89c-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8a89c-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="8a89c-128">Указывает коллекцию ссылок на группы безопасности приложения, к которой должна входить IP-адрес сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="8a89c-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8a89c-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="8a89c-130">Указывает коллекцию ссылок на группы безопасности приложения, к которой должна входить IP-адрес сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="8a89c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a89c-131">-AsJob</span></span>
<span data-ttu-id="8a89c-132">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8a89c-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a89c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a89c-133">-DefaultProfile</span></span>
<span data-ttu-id="8a89c-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a89c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a89c-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="8a89c-135">-DnsServer</span></span>
<span data-ttu-id="8a89c-136">Указывает DNS-сервер для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-136">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="8a89c-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="8a89c-138">Включает ускорение работы сети.</span><span class="sxs-lookup"><span data-stu-id="8a89c-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="8a89c-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="8a89c-139">-EnableIPForwarding</span></span>
<span data-ttu-id="8a89c-140">Указывает на то, что этот командлет включает IP-переадресацию для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="8a89c-141">IP-переадресация позволяет виртуальным машинам принимать трафик, адресованный другим получателям.</span><span class="sxs-lookup"><span data-stu-id="8a89c-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="8a89c-142">-Force</span><span class="sxs-lookup"><span data-stu-id="8a89c-142">-Force</span></span>
<span data-ttu-id="8a89c-143">Вызывает принудительное создание сетевого интерфейса, даже если сетевой интерфейс с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="8a89c-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="8a89c-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="8a89c-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="8a89c-145">Задает метку внутренней DNS-имени для нового сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-145">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-146">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="8a89c-146">-IpConfiguration</span></span>
<span data-ttu-id="8a89c-147">Задает IP-конфигурацию, которую этот командлет использует для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8a89c-148">-IpConfigurationName</span></span>
<span data-ttu-id="8a89c-149">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="8a89c-149">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8a89c-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="8a89c-151">Указывает объект **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8a89c-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8a89c-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8a89c-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="8a89c-153">Указывает идентификатор объекта **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8a89c-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8a89c-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="8a89c-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="8a89c-155">Указывает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="8a89c-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="8a89c-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="8a89c-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="8a89c-157">Указывает идентификатор конфигурации правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="8a89c-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="8a89c-158">-Location</span><span class="sxs-lookup"><span data-stu-id="8a89c-158">-Location</span></span>
<span data-ttu-id="8a89c-159">Указывает регион для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a89c-159">Specifies the region for a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-160">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a89c-160">-Name</span></span>
<span data-ttu-id="8a89c-161">Указывает имя сетевого интерфейса для создания.</span><span class="sxs-lookup"><span data-stu-id="8a89c-161">Specifies the name of the network interface to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8a89c-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8a89c-163">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="8a89c-163">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8a89c-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="8a89c-165">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8a89c-165">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8a89c-166">-PrivateIpAddress</span></span>
<span data-ttu-id="8a89c-167">Задает статический IP-адрес IPv4 для назначения этому сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8a89c-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8a89c-168">-PublicIpAddress</span></span>
<span data-ttu-id="8a89c-169">Указывает объект **PublicIPAddress** , который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8a89c-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8a89c-170">-PublicIpAddressId</span></span>
<span data-ttu-id="8a89c-171">Указывает идентификатор объекта **PublicIPAddress** , который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8a89c-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a89c-172">-ResourceGroupName</span></span>
<span data-ttu-id="8a89c-173">Указывает имя группы ресурсов, к которой относится сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8a89c-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-174">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="8a89c-174">-Subnet</span></span>
<span data-ttu-id="8a89c-175">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="8a89c-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="8a89c-176">Этот командлет создает сетевой интерфейс для подсети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8a89c-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8a89c-177">-SubnetId</span></span>
<span data-ttu-id="8a89c-178">Указывает идентификатор подсети, для которой требуется создать сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8a89c-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-179">-Тег</span><span class="sxs-lookup"><span data-stu-id="8a89c-179">-Tag</span></span>
<span data-ttu-id="8a89c-180">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8a89c-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a89c-181">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8a89c-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a89c-182">-Confirm</span></span>
<span data-ttu-id="8a89c-183">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a89c-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a89c-184">-WhatIf</span></span>
<span data-ttu-id="8a89c-185">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a89c-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a89c-186">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a89c-186">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a89c-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a89c-187">CommonParameters</span></span>
<span data-ttu-id="8a89c-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a89c-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a89c-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a89c-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a89c-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a89c-190">INPUTS</span></span>

### <span data-ttu-id="8a89c-191">System. String</span><span class="sxs-lookup"><span data-stu-id="8a89c-191">System.String</span></span>

### <span data-ttu-id="8a89c-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="8a89c-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="8a89c-193">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8a89c-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="8a89c-194">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8a89c-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="8a89c-195">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8a89c-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="8a89c-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="8a89c-196">System.String[]</span></span>

### <span data-ttu-id="8a89c-197">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="8a89c-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="8a89c-198">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="8a89c-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="8a89c-199">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="8a89c-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="8a89c-200">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="8a89c-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="8a89c-201">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8a89c-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8a89c-202">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a89c-202">OUTPUTS</span></span>

### <span data-ttu-id="8a89c-203">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a89c-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8a89c-204">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a89c-204">NOTES</span></span>

## <span data-ttu-id="8a89c-205">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a89c-205">RELATED LINKS</span></span>

[<span data-ttu-id="8a89c-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a89c-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="8a89c-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a89c-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="8a89c-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8a89c-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
