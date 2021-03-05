---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 994c0e85745e08d4a01e7b5a20b90a25513a983f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984427"
---
# <span data-ttu-id="85a72-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="85a72-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="85a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a72-102">SYNOPSIS</span></span>
<span data-ttu-id="85a72-103">Создается сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="85a72-103">Creates a network interface.</span></span>

## <span data-ttu-id="85a72-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85a72-104">SYNTAX</span></span>

### <span data-ttu-id="85a72-105">SetByIpConfigurationResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85a72-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a72-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="85a72-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a72-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85a72-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a72-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85a72-108">SetByResource</span></span>
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

## <span data-ttu-id="85a72-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a72-109">DESCRIPTION</span></span>
<span data-ttu-id="85a72-110">Командлет **New-AzNetworkInterface** создает сетевой интерфейс Azure.</span><span class="sxs-lookup"><span data-stu-id="85a72-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="85a72-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85a72-111">EXAMPLES</span></span>

### <span data-ttu-id="85a72-112">Пример 1. Создание сетевого интерфейса Azure</span><span class="sxs-lookup"><span data-stu-id="85a72-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="85a72-113">Эта команда создает сетевой интерфейс NetworkInterface001 с динамически присвоенным личным IP-адресом из подсети1 в виртуальной сети VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="85a72-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="85a72-114">Команда также назначает два DNS-сервера для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="85a72-115">Ребенок IPConfiguration будет создан автоматически с использованием имени IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="85a72-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="85a72-116">Пример 2. Создание сетевого интерфейса Azure с использованием объекта конфигурации IP-адреса</span><span class="sxs-lookup"><span data-stu-id="85a72-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="85a72-117">В этом примере создается новый сетевой интерфейс с использованием объекта конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="85a72-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="85a72-118">Объект конфигурации IP указывает статический частный IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="85a72-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="85a72-119">Первая команда извлекает существующую указанную виртуальную сеть, используемую для назначения подсети во второй команде.</span><span class="sxs-lookup"><span data-stu-id="85a72-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="85a72-120">Вторая команда создает конфигурацию IP-интерфейса с именем IPConfig1 и сохраняет конфигурацию в переменной с именем $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="85a72-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="85a72-121">Третья команда создает сетевой интерфейс NetworkInterface1 и использует конфигурацию IP-интерфейса сетевого интерфейса, храняную в переменной $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="85a72-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="85a72-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="85a72-122">Example 3</span></span>

<span data-ttu-id="85a72-123">Создается сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="85a72-123">Creates a network interface.</span></span> <span data-ttu-id="85a72-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="85a72-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="85a72-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85a72-125">PARAMETERS</span></span>

### <span data-ttu-id="85a72-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85a72-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="85a72-127">Указывает объект **ApplicationGatewayBackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="85a72-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="85a72-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="85a72-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="85a72-129">Определяет ИД объекта **ApplicationGatewayBackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="85a72-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="85a72-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="85a72-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="85a72-131">Набор ссылок на группы безопасности приложений, к которым относится конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="85a72-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="85a72-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="85a72-133">Набор ссылок на группы безопасности приложений, к которым относится конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="85a72-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85a72-134">-AsJob</span></span>
<span data-ttu-id="85a72-135">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="85a72-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85a72-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a72-136">-DefaultProfile</span></span>
<span data-ttu-id="85a72-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85a72-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85a72-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="85a72-138">-DnsServer</span></span>
<span data-ttu-id="85a72-139">Определяет DNS-сервер для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="85a72-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="85a72-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="85a72-141">Включает ускорение сетевого связи.</span><span class="sxs-lookup"><span data-stu-id="85a72-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="85a72-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="85a72-142">-EnableIPForwarding</span></span>
<span data-ttu-id="85a72-143">Указывает на то, что этот cmdlet включает переадваровку IP-адресов для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="85a72-144">Переадправление IP-адресов позволяет виртуальной машине получать трафик, адресованный другим назначениям.</span><span class="sxs-lookup"><span data-stu-id="85a72-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="85a72-145">-Force</span><span class="sxs-lookup"><span data-stu-id="85a72-145">-Force</span></span>
<span data-ttu-id="85a72-146">Будет создаваться сетевой интерфейс, даже если уже существует сетевой интерфейс с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="85a72-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="85a72-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="85a72-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="85a72-148">Указывает внутреннюю метку имени DNS для нового интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="85a72-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="85a72-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="85a72-149">-IpConfiguration</span></span>
<span data-ttu-id="85a72-150">Определяет конфигурацию IP-адреса, которая используется этим cmdlet для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="85a72-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="85a72-151">-IpConfigurationName</span></span>
<span data-ttu-id="85a72-152">Указывает имя конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="85a72-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="85a72-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="85a72-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="85a72-154">Объект **BackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="85a72-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="85a72-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="85a72-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="85a72-156">Определяет ИД объекта **BackendAddressPool.**</span><span class="sxs-lookup"><span data-stu-id="85a72-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="85a72-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="85a72-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="85a72-158">Определяет конфигурацию правила NAT для входящие остаток на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="85a72-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="85a72-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="85a72-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="85a72-160">Определяет ID конфигурации входящие правила NAT для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="85a72-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="85a72-161">-Location</span><span class="sxs-lookup"><span data-stu-id="85a72-161">-Location</span></span>
<span data-ttu-id="85a72-162">Определяет регион для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="85a72-163">-Name</span><span class="sxs-lookup"><span data-stu-id="85a72-163">-Name</span></span>
<span data-ttu-id="85a72-164">Имя создаемого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="85a72-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="85a72-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="85a72-166">Объект **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="85a72-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="85a72-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="85a72-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="85a72-168">Определяет ИД группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="85a72-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="85a72-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="85a72-169">-PrivateIpAddress</span></span>
<span data-ttu-id="85a72-170">Задает статический IP-адрес IPv4, который нужно назначить для этого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85a72-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="85a72-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="85a72-171">-PublicIpAddress</span></span>
<span data-ttu-id="85a72-172">Задает объект **PublicIPAddress,** который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="85a72-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="85a72-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="85a72-173">-PublicIpAddressId</span></span>
<span data-ttu-id="85a72-174">Задает ИД объекта **PublicIPAddress,** который нужно назначить сетевому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="85a72-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="85a72-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a72-175">-ResourceGroupName</span></span>
<span data-ttu-id="85a72-176">Имя группы ресурсов, к которой принадлежит сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="85a72-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="85a72-177">-Subnet</span><span class="sxs-lookup"><span data-stu-id="85a72-177">-Subnet</span></span>
<span data-ttu-id="85a72-178">Указывает объект **подсети.**</span><span class="sxs-lookup"><span data-stu-id="85a72-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="85a72-179">Этот cmdlet создает сетевой интерфейс для подсети, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="85a72-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="85a72-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="85a72-180">-SubnetId</span></span>
<span data-ttu-id="85a72-181">Определяет ИД подсети, для которой требуется создать сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="85a72-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="85a72-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="85a72-182">-Tag</span></span>
<span data-ttu-id="85a72-183">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="85a72-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85a72-184">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="85a72-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85a72-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85a72-185">-Confirm</span></span>
<span data-ttu-id="85a72-186">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a72-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a72-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a72-187">-WhatIf</span></span>
<span data-ttu-id="85a72-188">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85a72-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a72-189">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="85a72-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a72-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a72-190">CommonParameters</span></span>
<span data-ttu-id="85a72-191">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85a72-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a72-192">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a72-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a72-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85a72-193">INPUTS</span></span>

### <span data-ttu-id="85a72-194">System.String</span><span class="sxs-lookup"><span data-stu-id="85a72-194">System.String</span></span>

### <span data-ttu-id="85a72-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="85a72-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="85a72-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="85a72-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="85a72-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="85a72-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="85a72-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="85a72-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="85a72-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="85a72-199">System.String[]</span></span>

### <span data-ttu-id="85a72-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="85a72-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="85a72-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="85a72-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="85a72-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="85a72-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="85a72-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span><span class="sxs-lookup"><span data-stu-id="85a72-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="85a72-204">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="85a72-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="85a72-205">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85a72-205">OUTPUTS</span></span>

### <span data-ttu-id="85a72-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="85a72-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="85a72-207">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85a72-207">NOTES</span></span>

## <span data-ttu-id="85a72-208">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85a72-208">RELATED LINKS</span></span>

[<span data-ttu-id="85a72-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="85a72-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="85a72-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="85a72-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="85a72-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="85a72-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
