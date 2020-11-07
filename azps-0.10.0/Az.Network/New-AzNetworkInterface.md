---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: a4a40f67eef901cd1e93ac004fa01a3224ab222e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909669"
---
# <span data-ttu-id="8080f-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8080f-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="8080f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8080f-102">SYNOPSIS</span></span>
<span data-ttu-id="8080f-103">Создание сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-103">Creates a network interface.</span></span>

## <span data-ttu-id="8080f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8080f-104">SYNTAX</span></span>

### <span data-ttu-id="8080f-105">SetByIpConfigurationResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8080f-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8080f-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="8080f-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8080f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8080f-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8080f-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8080f-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8080f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8080f-109">DESCRIPTION</span></span>
<span data-ttu-id="8080f-110">Командлет **New-AzNetworkInterface** создает сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="8080f-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="8080f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8080f-111">EXAMPLES</span></span>

### <span data-ttu-id="8080f-112">Пример 1: создание сетевого интерфейса Azure</span><span class="sxs-lookup"><span data-stu-id="8080f-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="8080f-113">Эта команда создает сетевой интерфейс с именем NetworkInterface001 и динамически назначенный частный IP-адрес из Subnet1 в виртуальной сети с именем VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="8080f-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="8080f-114">Команда также назначает двум DNS-серверам сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8080f-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="8080f-115">Дочерний ресурс IP, который будет создан автоматически с использованием имени IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="8080f-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="8080f-116">Пример 2: создание сетевого интерфейса Azure с помощью объекта конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="8080f-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="8080f-117">В этом примере создается новый сетевой интерфейс с помощью объекта конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="8080f-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="8080f-118">Объект Configuration IP задает статический частный IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="8080f-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="8080f-119">Первая команда создает IP-конфигурацию сетевого интерфейса с именем IPConfig1 и сохраняет конфигурацию в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="8080f-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="8080f-120">Вторая команда создает сетевой интерфейс с именем NetworkInterface1, который использует IP-конфигурацию сетевого интерфейса, хранящуюся в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="8080f-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="8080f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8080f-121">PARAMETERS</span></span>

### <span data-ttu-id="8080f-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8080f-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="8080f-123">Указывает объект **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8080f-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8080f-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8080f-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="8080f-125">Указывает идентификатор объекта **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8080f-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8080f-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8080f-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="8080f-127">Указывает коллекцию ссылок на группы безопасности приложения, к которой должна входить IP-адрес сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="8080f-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8080f-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="8080f-129">Указывает коллекцию ссылок на группы безопасности приложения, к которой должна входить IP-адрес сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="8080f-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8080f-130">-AsJob</span></span>
<span data-ttu-id="8080f-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8080f-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8080f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8080f-132">-DefaultProfile</span></span>
<span data-ttu-id="8080f-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8080f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8080f-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="8080f-134">-DnsServer</span></span>
<span data-ttu-id="8080f-135">Указывает DNS-сервер для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-135">Specifies the DNS server for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="8080f-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="8080f-137">Включает ускорение работы сети.</span><span class="sxs-lookup"><span data-stu-id="8080f-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="8080f-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="8080f-138">-EnableIPForwarding</span></span>
<span data-ttu-id="8080f-139">Указывает на то, что этот командлет включает IP-переадресацию для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="8080f-140">IP-переадресация позволяет виртуальным машинам принимать трафик, адресованный другим получателям.</span><span class="sxs-lookup"><span data-stu-id="8080f-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="8080f-141">-Force</span><span class="sxs-lookup"><span data-stu-id="8080f-141">-Force</span></span>
<span data-ttu-id="8080f-142">Вызывает принудительное создание сетевого интерфейса, даже если сетевой интерфейс с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="8080f-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="8080f-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="8080f-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="8080f-144">Задает метку внутренней DNS-имени для нового сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-145">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="8080f-145">-IpConfiguration</span></span>
<span data-ttu-id="8080f-146">Задает IP-конфигурацию, которую этот командлет использует для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8080f-147">-IpConfigurationName</span></span>
<span data-ttu-id="8080f-148">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="8080f-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8080f-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="8080f-150">Указывает объект **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8080f-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8080f-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8080f-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="8080f-152">Указывает идентификатор объекта **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="8080f-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="8080f-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="8080f-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="8080f-154">Указывает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="8080f-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="8080f-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="8080f-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="8080f-156">Указывает идентификатор конфигурации правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="8080f-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="8080f-157">-Location</span><span class="sxs-lookup"><span data-stu-id="8080f-157">-Location</span></span>
<span data-ttu-id="8080f-158">Указывает регион для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8080f-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8080f-159">-Name</span></span>
<span data-ttu-id="8080f-160">Указывает имя сетевого интерфейса для создания.</span><span class="sxs-lookup"><span data-stu-id="8080f-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8080f-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8080f-162">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="8080f-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8080f-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="8080f-164">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="8080f-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8080f-165">-PrivateIpAddress</span></span>
<span data-ttu-id="8080f-166">Задает статический IP-адрес IPv4 для назначения этому сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8080f-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8080f-167">-PublicIpAddress</span></span>
<span data-ttu-id="8080f-168">Указывает объект **PublicIPAddress** , который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8080f-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8080f-169">-PublicIpAddressId</span></span>
<span data-ttu-id="8080f-170">Указывает идентификатор объекта **PublicIPAddress** , который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="8080f-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8080f-171">-ResourceGroupName</span></span>
<span data-ttu-id="8080f-172">Указывает имя группы ресурсов, к которой относится сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8080f-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-173">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="8080f-173">-Subnet</span></span>
<span data-ttu-id="8080f-174">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="8080f-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="8080f-175">Этот командлет создает сетевой интерфейс для подсети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8080f-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8080f-176">-SubnetId</span></span>
<span data-ttu-id="8080f-177">Указывает идентификатор подсети, для которой требуется создать сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8080f-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-178">-Тег</span><span class="sxs-lookup"><span data-stu-id="8080f-178">-Tag</span></span>
<span data-ttu-id="8080f-179">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8080f-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8080f-180">Например:</span><span class="sxs-lookup"><span data-stu-id="8080f-180">For example:</span></span>

<span data-ttu-id="8080f-181">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8080f-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8080f-182">-Confirm</span></span>
<span data-ttu-id="8080f-183">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8080f-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8080f-184">-WhatIf</span></span>
<span data-ttu-id="8080f-185">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8080f-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8080f-186">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8080f-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8080f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8080f-187">CommonParameters</span></span>
<span data-ttu-id="8080f-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8080f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8080f-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8080f-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8080f-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8080f-190">INPUTS</span></span>

## <span data-ttu-id="8080f-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8080f-191">OUTPUTS</span></span>

### <span data-ttu-id="8080f-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8080f-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8080f-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="8080f-193">NOTES</span></span>

## <span data-ttu-id="8080f-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8080f-194">RELATED LINKS</span></span>

[<span data-ttu-id="8080f-195">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8080f-195">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="8080f-196">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8080f-196">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="8080f-197">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8080f-197">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
