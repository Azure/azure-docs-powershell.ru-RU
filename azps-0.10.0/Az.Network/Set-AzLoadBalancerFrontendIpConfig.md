---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 9692f44ce5d0a819d0176e0b295571ca260a2a71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911046"
---
# <span data-ttu-id="498a6-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="498a6-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="498a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="498a6-102">SYNOPSIS</span></span>
<span data-ttu-id="498a6-103">Задает состояние цели для интерфейсной конфигурации IP в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="498a6-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="498a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="498a6-104">SYNTAX</span></span>

### <span data-ttu-id="498a6-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="498a6-105">SetByResourceSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="498a6-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="498a6-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="498a6-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="498a6-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="498a6-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="498a6-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="498a6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="498a6-109">DESCRIPTION</span></span>
<span data-ttu-id="498a6-110">Командлет **Set-AzLoadBalancerFrontendIpConfig** задает состояние цели для интерфейсной конфигурации IP в средстве балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="498a6-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="498a6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="498a6-111">EXAMPLES</span></span>

### <span data-ttu-id="498a6-112">Пример 1: изменение интерфейса IP-конфигурации для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="498a6-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="498a6-113">Первая команда возвращает виртуальную подсеть с именем Subnet и затем сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="498a6-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="498a6-114">Вторая команда получает связанную подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="498a6-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="498a6-115">Третья команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerFrontendIpConfig, который создает интерфейсную конфигурацию IP с именем NewFrontend для $slb.</span><span class="sxs-lookup"><span data-stu-id="498a6-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="498a6-116">Четвертая команда передает подсистему балансировки нагрузки в $slb в **Set-AzLoadBalancerFrontendIpConfig** , которая сохраняет и обновляет интерфейсную конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="498a6-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="498a6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="498a6-117">PARAMETERS</span></span>

### <span data-ttu-id="498a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498a6-118">-DefaultProfile</span></span>
<span data-ttu-id="498a6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="498a6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="498a6-120">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="498a6-120">-LoadBalancer</span></span>
<span data-ttu-id="498a6-121">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="498a6-121">Specifies a load balancer.</span></span>
<span data-ttu-id="498a6-122">Этот командлет задает состояние цели для серверной конфигурации для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="498a6-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="498a6-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="498a6-123">-Name</span></span>
<span data-ttu-id="498a6-124">Задает имя устанавливаемой интерфейсной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="498a6-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="498a6-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="498a6-125">-PrivateIpAddress</span></span>
<span data-ttu-id="498a6-126">Задает частный IP-адрес для подсистемы балансировки нагрузки, связанного с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="498a6-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="498a6-127">Указывайте этот параметр только в том случае, если вы также указали параметр *подсети* .</span><span class="sxs-lookup"><span data-stu-id="498a6-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="498a6-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="498a6-128">-PublicIpAddress</span></span>
<span data-ttu-id="498a6-129">Указывает объект **PublicIpAddress** , связанный с интерфейсной КОНФИГУРАЦИей IP-интерфейса, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="498a6-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="498a6-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="498a6-130">-PublicIpAddressId</span></span>
<span data-ttu-id="498a6-131">Указывает идентификатор объекта **PublicIpAddress** , связанного с интерфейсной КОНФИГУРАЦИЕЙ IP-интерфейса, которую этот командлет задает.</span><span class="sxs-lookup"><span data-stu-id="498a6-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="498a6-132">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="498a6-132">-Subnet</span></span>
<span data-ttu-id="498a6-133">Указывает объект **подсети** , содержащий интерфейсную конфигурацию IP, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="498a6-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="498a6-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="498a6-134">-SubnetId</span></span>
<span data-ttu-id="498a6-135">Указывает идентификатор подсети, содержащей интерфейсную конфигурацию IP-адресов, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="498a6-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="498a6-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="498a6-136">-Zone</span></span>
<span data-ttu-id="498a6-137">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="498a6-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="498a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498a6-138">CommonParameters</span></span>
<span data-ttu-id="498a6-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="498a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498a6-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="498a6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498a6-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="498a6-141">INPUTS</span></span>

### <span data-ttu-id="498a6-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="498a6-142">PSLoadBalancer</span></span>
<span data-ttu-id="498a6-143">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="498a6-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="498a6-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="498a6-144">OUTPUTS</span></span>

### <span data-ttu-id="498a6-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="498a6-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="498a6-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="498a6-146">NOTES</span></span>

## <span data-ttu-id="498a6-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="498a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="498a6-148">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="498a6-148">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="498a6-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="498a6-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="498a6-150">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="498a6-150">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="498a6-151">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="498a6-151">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="498a6-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="498a6-152">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="498a6-153">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="498a6-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


