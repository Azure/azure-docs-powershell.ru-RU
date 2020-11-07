---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 80324e1d6fa87959edb0da8e7aa72f3b2a42a3b6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910142"
---
# <span data-ttu-id="ea4bf-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea4bf-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="ea4bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4bf-103">Добавление интерфейсной конфигурации IP в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="ea4bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea4bf-104">SYNTAX</span></span>

### <span data-ttu-id="ea4bf-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="ea4bf-105">SetByResourceSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4bf-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="ea4bf-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4bf-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4bf-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea4bf-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4bf-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea4bf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea4bf-109">DESCRIPTION</span></span>
<span data-ttu-id="ea4bf-110">Командлет **Add-AzLoadBalancerFrontendIpConifg** добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="ea4bf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea4bf-111">EXAMPLES</span></span>

### <span data-ttu-id="ea4bf-112">Пример 1. Добавление интерфейсной конфигурации IP с динамическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="ea4bf-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="ea4bf-113">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="ea4bf-114">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="ea4bf-115">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с динамическим частным IP-адресом из подсети, хранящейся в переменной с именем $MySubnet.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="ea4bf-116">Пример 2. Добавление интерфейсной конфигурации IP со статическим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="ea4bf-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="ea4bf-117">Первая команда получает виртуальную сеть Azure с именем MyVnet и передает результат с помощью конвейера в командлет **Get-AzVirtualNetworkSubnetConfig** , чтобы получить подсеть с именем MySubnet.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="ea4bf-118">Затем команда сохраняет результат в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="ea4bf-119">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки со статическим частным IP-адресом из подсети, хранящейся в переменной с именем $Subnet.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="ea4bf-120">Пример 3. Добавление интерфейсной конфигурации IP с помощью общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="ea4bf-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="ea4bf-121">Первая команда получает общедоступный IP-адрес Azure с именем MyPub и сохраняет результат в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="ea4bf-122">Вторая команда получает подсистему балансировки нагрузки с именем MyLB и передает результат в командлет **Add-AzLoadBalancerFrontendIpConfig** , который добавляет интерфейсную конфигурацию IP в подсистему балансировки нагрузки с общедоступным IP-адресом, хранящимся в переменной с именем $PublicIp.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="ea4bf-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea4bf-123">PARAMETERS</span></span>

### <span data-ttu-id="ea4bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4bf-124">-DefaultProfile</span></span>
<span data-ttu-id="ea4bf-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea4bf-126">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="ea4bf-126">-LoadBalancer</span></span>
<span data-ttu-id="ea4bf-127">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="ea4bf-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="ea4bf-128">Этот командлет добавляет IP-конфигурацию переднего плана в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea4bf-129">-Name</span></span>
<span data-ttu-id="ea4bf-130">Указывает имя добавляемой интерфейсной конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-130">Specifies the name of the front-end IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4bf-131">-PrivateIpAddress</span></span>
<span data-ttu-id="ea4bf-132">Задает частный IP-адрес, который нужно связать с интерфейсной конфигурацией IP.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ea4bf-133">-PublicIpAddress</span></span>
<span data-ttu-id="ea4bf-134">Указывает общедоступный IP-адрес для связи с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="ea4bf-135">-PublicIpAddressId</span></span>
<span data-ttu-id="ea4bf-136">Specifes. идентификатор общедоступного IP-адреса, в который добавляется интерфейсная конфигурация IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-137">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="ea4bf-137">-Subnet</span></span>
<span data-ttu-id="ea4bf-138">Указывает объект подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ea4bf-139">-SubnetId</span></span>
<span data-ttu-id="ea4bf-140">Указывает идентификатор подсети, в который нужно добавить интерфейсную конфигурацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4bf-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="ea4bf-141">-Zone</span></span>
<span data-ttu-id="ea4bf-142">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="ea4bf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4bf-143">CommonParameters</span></span>
<span data-ttu-id="ea4bf-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4bf-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4bf-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4bf-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea4bf-146">INPUTS</span></span>

### <span data-ttu-id="ea4bf-147">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea4bf-147">PSLoadBalancer</span></span>
<span data-ttu-id="ea4bf-148">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ea4bf-148">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ea4bf-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea4bf-149">OUTPUTS</span></span>

### <span data-ttu-id="ea4bf-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea4bf-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ea4bf-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea4bf-151">NOTES</span></span>

## <span data-ttu-id="ea4bf-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea4bf-152">RELATED LINKS</span></span>

[<span data-ttu-id="ea4bf-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea4bf-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ea4bf-154">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ea4bf-154">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ea4bf-155">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ea4bf-155">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ea4bf-156">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea4bf-156">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ea4bf-157">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea4bf-157">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="ea4bf-158">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea4bf-158">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


