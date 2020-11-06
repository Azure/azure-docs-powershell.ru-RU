---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: d071e6f20d91dacfd99ca9566c64c4734ae93e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562436"
---
# <span data-ttu-id="9cd53-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9cd53-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="9cd53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cd53-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd53-103">Задает состояние цели для интерфейсной конфигурации IP в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9cd53-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cd53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cd53-104">SYNTAX</span></span>

### <span data-ttu-id="9cd53-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="9cd53-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd53-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="9cd53-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd53-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9cd53-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd53-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9cd53-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cd53-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cd53-109">DESCRIPTION</span></span>
<span data-ttu-id="9cd53-110">Командлет **Set-AzureRmLoadBalancerFrontendIpConfig** задает состояние цели для интерфейсной конфигурации IP в средстве балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd53-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="9cd53-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cd53-111">EXAMPLES</span></span>

### <span data-ttu-id="9cd53-112">Пример 1: изменение интерфейса IP-конфигурации для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="9cd53-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="9cd53-113">Первая команда возвращает виртуальную подсеть с именем Subnet и затем сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="9cd53-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="9cd53-114">Вторая команда получает связанную подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="9cd53-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="9cd53-115">Третья команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerFrontendIpConfig, который создает интерфейсную конфигурацию IP с именем NewFrontend для $slb.</span><span class="sxs-lookup"><span data-stu-id="9cd53-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="9cd53-116">Четвертая команда передает подсистему балансировки нагрузки в $slb в **Set-AzureRmLoadBalancerFrontendIpConfig** , которая сохраняет и обновляет интерфейсную конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="9cd53-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="9cd53-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cd53-117">PARAMETERS</span></span>

### <span data-ttu-id="9cd53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd53-118">-DefaultProfile</span></span>
<span data-ttu-id="9cd53-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd53-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd53-120">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="9cd53-120">-LoadBalancer</span></span>
<span data-ttu-id="9cd53-121">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9cd53-121">Specifies a load balancer.</span></span>
<span data-ttu-id="9cd53-122">Этот командлет задает состояние цели для серверной конфигурации для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9cd53-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd53-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cd53-123">-Name</span></span>
<span data-ttu-id="9cd53-124">Задает имя устанавливаемой интерфейсной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9cd53-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="9cd53-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9cd53-125">-PrivateIpAddress</span></span>
<span data-ttu-id="9cd53-126">Задает частный IP-адрес для подсистемы балансировки нагрузки, связанного с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9cd53-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="9cd53-127">Указывайте этот параметр только в том случае, если вы также указали параметр *подсети* .</span><span class="sxs-lookup"><span data-stu-id="9cd53-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd53-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9cd53-128">-PublicIpAddress</span></span>
<span data-ttu-id="9cd53-129">Указывает объект **PublicIpAddress** , связанный с интерфейсной КОНФИГУРАЦИей IP-интерфейса, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="9cd53-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd53-130">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9cd53-130">-PublicIpAddressId</span></span>
<span data-ttu-id="9cd53-131">Указывает идентификатор объекта **PublicIpAddress** , связанного с интерфейсной КОНФИГУРАЦИЕЙ IP-интерфейса, которую этот командлет задает.</span><span class="sxs-lookup"><span data-stu-id="9cd53-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd53-132">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="9cd53-132">-Subnet</span></span>
<span data-ttu-id="9cd53-133">Указывает объект **подсети** , содержащий интерфейсную конфигурацию IP, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cd53-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd53-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9cd53-134">-SubnetId</span></span>
<span data-ttu-id="9cd53-135">Указывает идентификатор подсети, содержащей интерфейсную конфигурацию IP-адресов, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9cd53-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd53-136">-Zone</span><span class="sxs-lookup"><span data-stu-id="9cd53-136">-Zone</span></span>
<span data-ttu-id="9cd53-137">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="9cd53-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="9cd53-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd53-138">CommonParameters</span></span>
<span data-ttu-id="9cd53-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cd53-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd53-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd53-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd53-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cd53-141">INPUTS</span></span>

### <span data-ttu-id="9cd53-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cd53-142">PSLoadBalancer</span></span>
<span data-ttu-id="9cd53-143">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9cd53-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9cd53-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cd53-144">OUTPUTS</span></span>

### <span data-ttu-id="9cd53-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cd53-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9cd53-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cd53-146">NOTES</span></span>

## <span data-ttu-id="9cd53-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cd53-147">RELATED LINKS</span></span>

[<span data-ttu-id="9cd53-148">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9cd53-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9cd53-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9cd53-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9cd53-150">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9cd53-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9cd53-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9cd53-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="9cd53-152">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9cd53-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9cd53-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9cd53-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


