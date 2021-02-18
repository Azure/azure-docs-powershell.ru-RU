---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 68bcbcf0aa99ee4ee1a40c038e3eb5255deb690a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228041"
---
# <span data-ttu-id="3e68c-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3e68c-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="3e68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e68c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e68c-103">Добавляет конфигурацию переднего IP-адреса в балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3e68c-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="3e68c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e68c-104">SYNTAX</span></span>

### <span data-ttu-id="3e68c-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e68c-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e68c-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="3e68c-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e68c-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3e68c-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e68c-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3e68c-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e68c-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3e68c-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefixId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e68c-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3e68c-110">SetByResourcePublicIpAddressPrefix</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressPrefix <PSPublicIpPrefix> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e68c-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e68c-111">DESCRIPTION</span></span>
<span data-ttu-id="3e68c-112">Для балансиента нагрузки Azure добавляется конфигурация переднего IP-адреса **Add-AzLoadBalancerFrontendIpConfig.**</span><span class="sxs-lookup"><span data-stu-id="3e68c-112">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="3e68c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e68c-113">EXAMPLES</span></span>

### <span data-ttu-id="3e68c-114">Пример 1. Добавление конфигурации переднего IP-адреса с динамическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="3e68c-114">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="3e68c-115">Первая команда получает виртуальную сеть Azure MyVnet и передает результат с помощью конвейера **командлету Get-AzVirtualNetworkSubnetConfig** для получения подсети с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-115">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="3e68c-116">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-116">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="3e68c-117">Вторая команда получает баланс нагрузки MyLB и передает результат **командлету Add-AzLoadBalancerFrontendIpConfig,** который добавляет в балансор загрузки конфигурацию переднего IP-адреса с динамическим частным IP-адресом из подсети, храняной в переменной с именем $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-117">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="3e68c-118">Пример 2. Добавление передней конфигурации IP-адреса со статическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="3e68c-118">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\> $Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="3e68c-119">Первая команда получает виртуальную сеть Azure MyVnet и передает результат с помощью конвейера **командлету Get-AzVirtualNetworkSubnetConfig** для получения подсети с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-119">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="3e68c-120">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-120">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="3e68c-121">Вторая команда получает балансовый баланс нагрузки MyLB и передает результат **командлету Add-AzLoadBalancerFrontendIpConfig,** который добавляет в балансор загрузки конфигурацию переднего IP-адреса со статическим частным IP-адресом из подсети, которая хранится в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-121">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="3e68c-122">Пример 3. Добавление конфигурации переднего IP-адреса с общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="3e68c-122">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\> $PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="3e68c-123">Первая команда получает общедоступный IP-адрес Azure MyPub и сохраняет результат в переменной с $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3e68c-123">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="3e68c-124">Вторая команда получает баланс нагрузки MyLB и передает результат **командлету Add-AzLoadBalancerFrontendIpConfig,** который добавляет в баланслет переднего IP-адреса с общедоступным IP-адресом, который хранится в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="3e68c-124">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

### <span data-ttu-id="3e68c-125">Пример 4. Добавление передней конфигурации IP-адреса с общедоступным IP-префиксом</span><span class="sxs-lookup"><span data-stu-id="3e68c-125">Example 4 Add a front-end IP configuration with a public IP prefix</span></span>
```
PS C:\> $PublicIpPrefix = Get-AzPublicIpPrefix -ResourceGroupName "myRG" -Name "MyPubPrefix"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddressPrefix $PublicIpPrefix | Set-AzLoadBalancer
```

<span data-ttu-id="3e68c-126">Первая команда получает общедоступный IP-префикс Azure MyPubPrefix и сохраняет результат в переменной с $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3e68c-126">The first command gets the Azure public IP prefix named MyPubPrefix and stores the result in the variable named $PublicIpPrefix.</span></span>
<span data-ttu-id="3e68c-127">Вторая команда получает балансовый баланс нагрузки MyLB и передает результат **командлету Add-AzLoadBalancerFrontendIpConfig,** который добавляет переднюю конфигурацию IP-адреса к балансе нагрузки с общедоступным IP-префиксом, который хранится в переменной с именем $PublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="3e68c-127">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP prefix stored in the variable named $PublicIpPrefix.</span></span>

## <span data-ttu-id="3e68c-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e68c-128">PARAMETERS</span></span>

### <span data-ttu-id="3e68c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e68c-129">-DefaultProfile</span></span>
<span data-ttu-id="3e68c-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e68c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e68c-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e68c-131">-LoadBalancer</span></span>
<span data-ttu-id="3e68c-132">Указывает объект **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="3e68c-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="3e68c-133">Этот cmdlet добавляет конфигурацию переднего IP-адреса в балансировку нагрузки, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="3e68c-133">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3e68c-134">-Name</span></span>
<span data-ttu-id="3e68c-135">Указывает имя добавляемой передней конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-135">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="3e68c-136">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3e68c-136">-PrivateIpAddress</span></span>
<span data-ttu-id="3e68c-137">Указывает частный IP-адрес, который нужно связать с конфигурацией переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-137">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-138">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3e68c-138">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="3e68c-139">Версия конфигурации IP-адреса личного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-139">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-140">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3e68c-140">-PublicIpAddress</span></span>
<span data-ttu-id="3e68c-141">Указывает общедоступный IP-адрес, который нужно связать с конфигурацией переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-141">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-142">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3e68c-142">-PublicIpAddressId</span></span>
<span data-ttu-id="3e68c-143">Определяет ИД общего IP-адреса, для которого нужно добавить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-143">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-144">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3e68c-144">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="3e68c-145">Указывает объект префикса общего IP-адреса, который нужно связать с конфигурацией IP-адреса переднего.</span><span class="sxs-lookup"><span data-stu-id="3e68c-145">Specifies the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-146">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="3e68c-146">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="3e68c-147">Определяет ID объекта префикса общего IP-адреса, который нужно связать с конфигурацией переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-147">Specifies the ID of the public ip address prefix object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-148">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3e68c-148">-Subnet</span></span>
<span data-ttu-id="3e68c-149">Определяет объект подсети, в который нужно добавить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-149">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3e68c-150">-SubnetId</span></span>
<span data-ttu-id="3e68c-151">Определяет ИД подсети, в которую нужно добавить конфигурацию переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-151">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="3e68c-152">-Zone</span></span>
<span data-ttu-id="3e68c-153">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e68c-153">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="3e68c-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e68c-154">-Confirm</span></span>
<span data-ttu-id="3e68c-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e68c-156">-WhatIf</span></span>
<span data-ttu-id="3e68c-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e68c-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e68c-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3e68c-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e68c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e68c-159">CommonParameters</span></span>
<span data-ttu-id="3e68c-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e68c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e68c-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e68c-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e68c-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e68c-162">INPUTS</span></span>

### <span data-ttu-id="3e68c-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e68c-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3e68c-164">System.String</span><span class="sxs-lookup"><span data-stu-id="3e68c-164">System.String</span></span>

### <span data-ttu-id="3e68c-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3e68c-165">System.String[]</span></span>

### <span data-ttu-id="3e68c-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="3e68c-166">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="3e68c-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3e68c-167">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="3e68c-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e68c-168">OUTPUTS</span></span>

### <span data-ttu-id="3e68c-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3e68c-169">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3e68c-170">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e68c-170">NOTES</span></span>

## <span data-ttu-id="3e68c-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e68c-171">RELATED LINKS</span></span>

[<span data-ttu-id="3e68c-172">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3e68c-172">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3e68c-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3e68c-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="3e68c-174">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e68c-174">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3e68c-175">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3e68c-175">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3e68c-176">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3e68c-176">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3e68c-177">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3e68c-177">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


