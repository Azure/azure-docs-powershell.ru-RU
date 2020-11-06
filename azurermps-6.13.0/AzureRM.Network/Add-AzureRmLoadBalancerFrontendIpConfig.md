---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560115"
---
# <span data-ttu-id="20086-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20086-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="20086-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20086-102">SYNOPSIS</span></span>
<span data-ttu-id="20086-103">Добавление интерфейсной конфигурации IP в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="20086-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20086-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20086-104">SYNTAX</span></span>

### <span data-ttu-id="20086-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20086-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20086-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="20086-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20086-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20086-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20086-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20086-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20086-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20086-109">DESCRIPTION</span></span>
<span data-ttu-id="20086-110">Командлет **Add-AzureRmLoadBalancerFrontendIpConifg** добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="20086-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="20086-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20086-111">EXAMPLES</span></span>

### <span data-ttu-id="20086-112">Пример 1. Добавление интерфейсной конфигурации IP с динамическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="20086-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="20086-113">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzureRmVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="20086-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="20086-114">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="20086-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="20086-115">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzureRmLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с динамическим частным IP-адресом из подсети, хранящейся в переменной с именем $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="20086-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="20086-116">Пример 2. Добавление интерфейсной конфигурации IP со статическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="20086-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="20086-117">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzureRmVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="20086-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="20086-118">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="20086-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="20086-119">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzureRmLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки со статическим частным IP-адресом из подсети, хранящейся в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="20086-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="20086-120">Пример 3. Добавление интерфейсной конфигурации IP с помощью общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="20086-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="20086-121">Первая команда получает общедоступный IP-адрес Azure с именем MyPub и сохраняет результат в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="20086-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="20086-122">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzureRmLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с общедоступным IP-адресом, хранящимся в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="20086-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="20086-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20086-123">PARAMETERS</span></span>

### <span data-ttu-id="20086-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20086-124">-DefaultProfile</span></span>
<span data-ttu-id="20086-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20086-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20086-126">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="20086-126">-LoadBalancer</span></span>
<span data-ttu-id="20086-127">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="20086-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="20086-128">Этот командлет добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="20086-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="20086-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20086-129">-Name</span></span>
<span data-ttu-id="20086-130">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="20086-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="20086-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="20086-131">-PrivateIpAddress</span></span>
<span data-ttu-id="20086-132">Задает частный IP-адрес, который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="20086-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="20086-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20086-133">-PublicIpAddress</span></span>
<span data-ttu-id="20086-134">Указывает общедоступный IP-адрес для связи с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="20086-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="20086-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="20086-135">-PublicIpAddressId</span></span>
<span data-ttu-id="20086-136">Specifes. идентификатор общедоступного IP-адреса, в который добавляется интерфейсная конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="20086-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="20086-137">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="20086-137">-Subnet</span></span>
<span data-ttu-id="20086-138">Указывает объект подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="20086-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="20086-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="20086-139">-SubnetId</span></span>
<span data-ttu-id="20086-140">Указывает идентификатор подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="20086-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="20086-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="20086-141">-Zone</span></span>
<span data-ttu-id="20086-142">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="20086-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="20086-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20086-143">-Confirm</span></span>
<span data-ttu-id="20086-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20086-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20086-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20086-145">-WhatIf</span></span>
<span data-ttu-id="20086-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20086-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20086-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20086-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20086-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20086-148">CommonParameters</span></span>
<span data-ttu-id="20086-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20086-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20086-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20086-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20086-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20086-151">INPUTS</span></span>

### <span data-ttu-id="20086-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20086-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="20086-153">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20086-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="20086-154">System. Collections. Generic. List \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="20086-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="20086-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20086-155">OUTPUTS</span></span>

### <span data-ttu-id="20086-156">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="20086-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="20086-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="20086-157">NOTES</span></span>

## <span data-ttu-id="20086-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20086-158">RELATED LINKS</span></span>

[<span data-ttu-id="20086-159">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20086-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="20086-160">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="20086-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="20086-161">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="20086-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="20086-162">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20086-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="20086-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20086-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="20086-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="20086-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


