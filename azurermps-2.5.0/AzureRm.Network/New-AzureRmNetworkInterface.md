---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 1a87b7bfa4c497ad7d09a9e84d972d548e2031b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914074"
---
# <span data-ttu-id="7b95e-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b95e-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="7b95e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b95e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b95e-103">Создание сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b95e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b95e-104">SYNTAX</span></span>

### <span data-ttu-id="7b95e-105">SetByIpConfigurationResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b95e-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b95e-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="7b95e-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b95e-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b95e-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b95e-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7b95e-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
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

## <span data-ttu-id="7b95e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b95e-109">DESCRIPTION</span></span>
<span data-ttu-id="7b95e-110">Командлет **New-AzureRmNetworkInterface** создает сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="7b95e-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="7b95e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b95e-111">EXAMPLES</span></span>

### <span data-ttu-id="7b95e-112">Пример 1: создание сетевого интерфейса Azure</span><span class="sxs-lookup"><span data-stu-id="7b95e-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="7b95e-113">Эта команда создает сетевой интерфейс с именем NetworkInterface001 и динамически назначенный частный IP-адрес из Subnet1 в виртуальной сети с именем VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="7b95e-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="7b95e-114">Команда также назначает двум DNS-серверам сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="7b95e-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="7b95e-115">Дочерний ресурс IP, который будет создан автоматически с использованием имени IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="7b95e-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="7b95e-116">Пример 2: создание сетевого интерфейса Azure с помощью объекта конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="7b95e-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="7b95e-117">В этом примере создается новый сетевой интерфейс с помощью объекта конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="7b95e-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="7b95e-118">Объект Configuration IP задает статический частный IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="7b95e-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="7b95e-119">Первая команда создает IP-конфигурацию сетевого интерфейса с именем IPConfig1 и сохраняет конфигурацию в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="7b95e-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="7b95e-120">Вторая команда создает сетевой интерфейс с именем NetworkInterface1, который использует IP-конфигурацию сетевого интерфейса, хранящуюся в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="7b95e-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="7b95e-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b95e-121">PARAMETERS</span></span>

### <span data-ttu-id="7b95e-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b95e-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="7b95e-123">Указывает объект **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="7b95e-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7b95e-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7b95e-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="7b95e-125">Указывает идентификатор объекта **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="7b95e-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7b95e-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7b95e-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="7b95e-127">Указывает коллекцию ссылок на группы безопасности приложения, к которой должна входить IP-адрес сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="7b95e-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7b95e-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="7b95e-129">Указывает коллекцию ссылок на группы безопасности приложения, к которой должна входить IP-адрес сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="7b95e-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b95e-130">-AsJob</span></span>
<span data-ttu-id="7b95e-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7b95e-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b95e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b95e-132">-DefaultProfile</span></span>
<span data-ttu-id="7b95e-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b95e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b95e-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="7b95e-134">-DnsServer</span></span>
<span data-ttu-id="7b95e-135">Указывает DNS-сервер для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="7b95e-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="7b95e-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="7b95e-137">Включает ускорение работы сети.</span><span class="sxs-lookup"><span data-stu-id="7b95e-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="7b95e-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="7b95e-138">-EnableIPForwarding</span></span>
<span data-ttu-id="7b95e-139">Указывает на то, что этот командлет включает IP-переадресацию для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="7b95e-140">IP-переадресация позволяет виртуальным машинам принимать трафик, адресованный другим получателям.</span><span class="sxs-lookup"><span data-stu-id="7b95e-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="7b95e-141">-Force</span><span class="sxs-lookup"><span data-stu-id="7b95e-141">-Force</span></span>
<span data-ttu-id="7b95e-142">Вызывает принудительное создание сетевого интерфейса, даже если сетевой интерфейс с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="7b95e-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="7b95e-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="7b95e-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="7b95e-144">Задает метку внутренней DNS-имени для нового сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="7b95e-145">-Конфигурацию</span><span class="sxs-lookup"><span data-stu-id="7b95e-145">-IpConfiguration</span></span>
<span data-ttu-id="7b95e-146">Задает IP-конфигурацию, которую этот командлет использует для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="7b95e-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7b95e-147">-IpConfigurationName</span></span>
<span data-ttu-id="7b95e-148">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="7b95e-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="7b95e-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7b95e-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="7b95e-150">Указывает объект **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="7b95e-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7b95e-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7b95e-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="7b95e-152">Указывает идентификатор объекта **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="7b95e-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="7b95e-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="7b95e-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="7b95e-154">Указывает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7b95e-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="7b95e-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="7b95e-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="7b95e-156">Указывает идентификатор конфигурации правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7b95e-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="7b95e-157">-Location</span><span class="sxs-lookup"><span data-stu-id="7b95e-157">-Location</span></span>
<span data-ttu-id="7b95e-158">Указывает регион для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b95e-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="7b95e-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b95e-159">-Name</span></span>
<span data-ttu-id="7b95e-160">Указывает имя сетевого интерфейса для создания.</span><span class="sxs-lookup"><span data-stu-id="7b95e-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="7b95e-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7b95e-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7b95e-162">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="7b95e-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="7b95e-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7b95e-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7b95e-164">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="7b95e-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="7b95e-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b95e-165">-PrivateIpAddress</span></span>
<span data-ttu-id="7b95e-166">Задает статический IP-адрес IPv4 для назначения этому сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="7b95e-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="7b95e-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b95e-167">-PublicIpAddress</span></span>
<span data-ttu-id="7b95e-168">Указывает объект **PublicIPAddress** , который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="7b95e-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="7b95e-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="7b95e-169">-PublicIpAddressId</span></span>
<span data-ttu-id="7b95e-170">Указывает идентификатор объекта **PublicIPAddress** , который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="7b95e-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="7b95e-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b95e-171">-ResourceGroupName</span></span>
<span data-ttu-id="7b95e-172">Указывает имя группы ресурсов, к которой относится сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7b95e-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="7b95e-173">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="7b95e-173">-Subnet</span></span>
<span data-ttu-id="7b95e-174">Указывает объект **подсети** .</span><span class="sxs-lookup"><span data-stu-id="7b95e-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="7b95e-175">Этот командлет создает сетевой интерфейс для подсети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7b95e-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b95e-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7b95e-176">-SubnetId</span></span>
<span data-ttu-id="7b95e-177">Указывает идентификатор подсети, для которой требуется создать сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7b95e-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="7b95e-178">-Тег</span><span class="sxs-lookup"><span data-stu-id="7b95e-178">-Tag</span></span>
<span data-ttu-id="7b95e-179">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="7b95e-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7b95e-180">Например:</span><span class="sxs-lookup"><span data-stu-id="7b95e-180">For example:</span></span>

<span data-ttu-id="7b95e-181">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="7b95e-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7b95e-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b95e-182">-Confirm</span></span>
<span data-ttu-id="7b95e-183">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b95e-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b95e-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b95e-184">-WhatIf</span></span>
<span data-ttu-id="7b95e-185">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b95e-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b95e-186">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b95e-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b95e-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b95e-187">CommonParameters</span></span>
<span data-ttu-id="7b95e-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b95e-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b95e-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b95e-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b95e-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b95e-190">INPUTS</span></span>

## <span data-ttu-id="7b95e-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b95e-191">OUTPUTS</span></span>

### <span data-ttu-id="7b95e-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b95e-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7b95e-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b95e-193">NOTES</span></span>

## <span data-ttu-id="7b95e-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b95e-194">RELATED LINKS</span></span>

[<span data-ttu-id="7b95e-195">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b95e-195">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="7b95e-196">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b95e-196">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="7b95e-197">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b95e-197">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
