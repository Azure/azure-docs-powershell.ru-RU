---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244896"
---
# <span data-ttu-id="eb8e2-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb8e2-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="eb8e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8e2-103">Добавление интерфейсной конфигурации IP в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="eb8e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb8e2-104">SYNTAX</span></span>

### <span data-ttu-id="eb8e2-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb8e2-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8e2-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="eb8e2-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8e2-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb8e2-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb8e2-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb8e2-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb8e2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb8e2-109">DESCRIPTION</span></span>
<span data-ttu-id="eb8e2-110">Командлет **Add-AzLoadBalancerFrontendIpConfig** добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="eb8e2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb8e2-111">EXAMPLES</span></span>

### <span data-ttu-id="eb8e2-112">Пример 1. Добавление интерфейсной конфигурации IP с динамическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="eb8e2-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="eb8e2-113">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="eb8e2-114">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="eb8e2-115">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с динамическим частным IP-адресом из подсети, хранящейся в переменной с именем $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="eb8e2-116">Пример 2. Добавление интерфейсной конфигурации IP со статическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="eb8e2-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="eb8e2-117">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="eb8e2-118">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="eb8e2-119">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки со статическим частным IP-адресом из подсети, хранящейся в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="eb8e2-120">Пример 3. Добавление интерфейсной конфигурации IP с помощью общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="eb8e2-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="eb8e2-121">Первая команда получает общедоступный IP-адрес Azure с именем MyPub и сохраняет результат в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="eb8e2-122">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с общедоступным IP-адресом, хранящимся в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="eb8e2-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb8e2-123">PARAMETERS</span></span>

### <span data-ttu-id="eb8e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8e2-124">-DefaultProfile</span></span>
<span data-ttu-id="eb8e2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb8e2-126">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="eb8e2-126">-LoadBalancer</span></span>
<span data-ttu-id="eb8e2-127">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="eb8e2-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="eb8e2-128">Этот командлет добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb8e2-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb8e2-129">-Name</span></span>
<span data-ttu-id="eb8e2-130">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="eb8e2-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb8e2-131">-PrivateIpAddress</span></span>
<span data-ttu-id="eb8e2-132">Задает частный IP-адрес, который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="eb8e2-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="eb8e2-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="eb8e2-134">Версия частного IP-адреса конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-134">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="eb8e2-135">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb8e2-135">-PublicIpAddress</span></span>
<span data-ttu-id="eb8e2-136">Указывает общедоступный IP-адрес для связи с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="eb8e2-137">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="eb8e2-137">-PublicIpAddressId</span></span>
<span data-ttu-id="eb8e2-138">Указывает идентификатор общедоступного IP-адреса, в который нужно добавить IP-конфигурацию переднего плана.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="eb8e2-139">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="eb8e2-139">-Subnet</span></span>
<span data-ttu-id="eb8e2-140">Указывает объект подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="eb8e2-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="eb8e2-141">-SubnetId</span></span>
<span data-ttu-id="eb8e2-142">Указывает идентификатор подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="eb8e2-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="eb8e2-143">-Zone</span></span>
<span data-ttu-id="eb8e2-144">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="eb8e2-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb8e2-145">-Confirm</span></span>
<span data-ttu-id="eb8e2-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb8e2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8e2-147">-WhatIf</span></span>
<span data-ttu-id="eb8e2-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb8e2-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb8e2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8e2-150">CommonParameters</span></span>
<span data-ttu-id="eb8e2-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb8e2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8e2-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb8e2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8e2-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb8e2-153">INPUTS</span></span>

### <span data-ttu-id="eb8e2-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb8e2-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="eb8e2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="eb8e2-155">System.String</span></span>

### <span data-ttu-id="eb8e2-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="eb8e2-156">System.String[]</span></span>

### <span data-ttu-id="eb8e2-157">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="eb8e2-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="eb8e2-158">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eb8e2-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="eb8e2-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb8e2-159">OUTPUTS</span></span>

### <span data-ttu-id="eb8e2-160">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eb8e2-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="eb8e2-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb8e2-161">NOTES</span></span>

## <span data-ttu-id="eb8e2-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb8e2-162">RELATED LINKS</span></span>

[<span data-ttu-id="eb8e2-163">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb8e2-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eb8e2-164">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb8e2-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="eb8e2-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eb8e2-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="eb8e2-166">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb8e2-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eb8e2-167">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb8e2-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eb8e2-168">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eb8e2-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


