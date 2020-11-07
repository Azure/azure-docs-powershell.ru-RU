---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2dba7d00ea308225736de6714c90c74b0ce30837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730711"
---
# <span data-ttu-id="6d13c-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d13c-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="6d13c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d13c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d13c-103">Добавление интерфейсной конфигурации IP в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6d13c-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="6d13c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d13c-104">SYNTAX</span></span>

### <span data-ttu-id="6d13c-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d13c-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d13c-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="6d13c-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d13c-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d13c-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d13c-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d13c-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d13c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d13c-109">DESCRIPTION</span></span>
<span data-ttu-id="6d13c-110">Командлет **Add-AzLoadBalancerFrontendIpConifg** добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="6d13c-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="6d13c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d13c-111">EXAMPLES</span></span>

### <span data-ttu-id="6d13c-112">Пример 1. Добавление интерфейсной конфигурации IP с динамическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="6d13c-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="6d13c-113">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="6d13c-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="6d13c-114">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="6d13c-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="6d13c-115">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с динамическим частным IP-адресом из подсети, хранящейся в переменной с именем $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="6d13c-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="6d13c-116">Пример 2. Добавление интерфейсной конфигурации IP со статическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="6d13c-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="6d13c-117">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="6d13c-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="6d13c-118">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="6d13c-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="6d13c-119">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки со статическим частным IP-адресом из подсети, хранящейся в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="6d13c-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="6d13c-120">Пример 3. Добавление интерфейсной конфигурации IP с помощью общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="6d13c-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="6d13c-121">Первая команда получает общедоступный IP-адрес Azure с именем MyPub и сохраняет результат в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="6d13c-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="6d13c-122">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с общедоступным IP-адресом, хранящимся в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="6d13c-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="6d13c-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d13c-123">PARAMETERS</span></span>

### <span data-ttu-id="6d13c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d13c-124">-DefaultProfile</span></span>
<span data-ttu-id="6d13c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d13c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d13c-126">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="6d13c-126">-LoadBalancer</span></span>
<span data-ttu-id="6d13c-127">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="6d13c-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="6d13c-128">Этот командлет добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="6d13c-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d13c-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d13c-129">-Name</span></span>
<span data-ttu-id="6d13c-130">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6d13c-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="6d13c-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d13c-131">-PrivateIpAddress</span></span>
<span data-ttu-id="6d13c-132">Задает частный IP-адрес, который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="6d13c-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6d13c-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d13c-133">-PublicIpAddress</span></span>
<span data-ttu-id="6d13c-134">Указывает общедоступный IP-адрес для связи с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6d13c-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6d13c-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="6d13c-135">-PublicIpAddressId</span></span>
<span data-ttu-id="6d13c-136">Specifes. идентификатор общедоступного IP-адреса, в который добавляется интерфейсная конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6d13c-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6d13c-137">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="6d13c-137">-Subnet</span></span>
<span data-ttu-id="6d13c-138">Указывает объект подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6d13c-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6d13c-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6d13c-139">-SubnetId</span></span>
<span data-ttu-id="6d13c-140">Указывает идентификатор подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="6d13c-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="6d13c-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="6d13c-141">-Zone</span></span>
<span data-ttu-id="6d13c-142">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="6d13c-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="6d13c-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d13c-143">-Confirm</span></span>
<span data-ttu-id="6d13c-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d13c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d13c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d13c-145">-WhatIf</span></span>
<span data-ttu-id="6d13c-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d13c-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d13c-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d13c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d13c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d13c-148">CommonParameters</span></span>
<span data-ttu-id="6d13c-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d13c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d13c-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d13c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d13c-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d13c-151">INPUTS</span></span>

### <span data-ttu-id="6d13c-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d13c-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="6d13c-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6d13c-153">System.String</span></span>

### <span data-ttu-id="6d13c-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="6d13c-154">System.String[]</span></span>

### <span data-ttu-id="6d13c-155">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6d13c-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="6d13c-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d13c-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="6d13c-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d13c-157">OUTPUTS</span></span>

### <span data-ttu-id="6d13c-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d13c-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6d13c-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d13c-159">NOTES</span></span>

## <span data-ttu-id="6d13c-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d13c-160">RELATED LINKS</span></span>

[<span data-ttu-id="6d13c-161">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d13c-161">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6d13c-162">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6d13c-162">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="6d13c-163">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6d13c-163">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="6d13c-164">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d13c-164">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6d13c-165">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d13c-165">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="6d13c-166">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6d13c-166">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


