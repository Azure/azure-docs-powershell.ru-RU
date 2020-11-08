---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 62a479dd0c9c622100f5880c1aaf46836e179c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065141"
---
# <span data-ttu-id="36944-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36944-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="36944-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36944-102">SYNOPSIS</span></span>
<span data-ttu-id="36944-103">Обновляет интерфейсную конфигурацию IP для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="36944-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="36944-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36944-104">SYNTAX</span></span>

### <span data-ttu-id="36944-105">SetByResourceSubnet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36944-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36944-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="36944-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36944-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36944-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36944-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36944-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36944-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36944-109">DESCRIPTION</span></span>
<span data-ttu-id="36944-110">Командлет **Set-AzLoadBalancerFrontendIpConfig** обновляет интерфейсную конфигурацию IP-конфигурации для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="36944-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="36944-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36944-111">EXAMPLES</span></span>

### <span data-ttu-id="36944-112">Пример 1: изменение интерфейса IP-конфигурации для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="36944-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="36944-113">Первая команда возвращает виртуальную подсеть с именем Subnet и затем сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="36944-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="36944-114">Вторая команда получает связанную подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="36944-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="36944-115">Третья команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerFrontendIpConfig, который создает интерфейсную конфигурацию IP с именем NewFrontend для $slb.</span><span class="sxs-lookup"><span data-stu-id="36944-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="36944-116">Четвертая команда передает подсистему балансировки нагрузки в $slb в **Set-AzLoadBalancerFrontendIpConfig** , которая сохраняет и обновляет интерфейсную конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="36944-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="36944-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36944-117">PARAMETERS</span></span>

### <span data-ttu-id="36944-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36944-118">-DefaultProfile</span></span>
<span data-ttu-id="36944-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36944-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36944-120">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="36944-120">-LoadBalancer</span></span>
<span data-ttu-id="36944-121">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="36944-121">Specifies a load balancer.</span></span>
<span data-ttu-id="36944-122">Этот командлет обновляет конфигурацию интерфейсной части для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="36944-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="36944-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36944-123">-Name</span></span>
<span data-ttu-id="36944-124">Задает имя устанавливаемой интерфейсной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="36944-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="36944-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="36944-125">-PrivateIpAddress</span></span>
<span data-ttu-id="36944-126">Задает частный IP-адрес для подсистемы балансировки нагрузки, связанного с интерфейсной конфигурацией IP-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="36944-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="36944-127">Указывайте этот параметр только в том случае, если вы также указали параметр *подсети* .</span><span class="sxs-lookup"><span data-stu-id="36944-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="36944-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="36944-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="36944-129">Версия частного IP-адреса конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="36944-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="36944-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36944-130">-PublicIpAddress</span></span>
<span data-ttu-id="36944-131">Указывает объект **PublicIpAddress** , связанный с интерфейсной КОНФИГУРАЦИей IP-интерфейса, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="36944-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="36944-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="36944-132">-PublicIpAddressId</span></span>
<span data-ttu-id="36944-133">Указывает идентификатор объекта **PublicIpAddress** , связанного с интерфейсной КОНФИГУРАЦИЕЙ IP-интерфейса, которую этот командлет задает.</span><span class="sxs-lookup"><span data-stu-id="36944-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="36944-134">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="36944-134">-Subnet</span></span>
<span data-ttu-id="36944-135">Указывает объект **подсети** , содержащий интерфейсную конфигурацию IP, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36944-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="36944-136">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="36944-136">-SubnetId</span></span>
<span data-ttu-id="36944-137">Указывает идентификатор подсети, содержащей интерфейсную конфигурацию IP-адресов, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36944-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="36944-138">-Zone</span><span class="sxs-lookup"><span data-stu-id="36944-138">-Zone</span></span>
<span data-ttu-id="36944-139">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="36944-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="36944-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36944-140">-Confirm</span></span>
<span data-ttu-id="36944-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36944-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36944-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36944-142">-WhatIf</span></span>
<span data-ttu-id="36944-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36944-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36944-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36944-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36944-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36944-145">CommonParameters</span></span>
<span data-ttu-id="36944-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36944-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36944-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36944-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36944-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36944-148">INPUTS</span></span>

### <span data-ttu-id="36944-149">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36944-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="36944-150">System. String</span><span class="sxs-lookup"><span data-stu-id="36944-150">System.String</span></span>

### <span data-ttu-id="36944-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="36944-151">System.String[]</span></span>

### <span data-ttu-id="36944-152">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="36944-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="36944-153">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="36944-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="36944-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36944-154">OUTPUTS</span></span>

### <span data-ttu-id="36944-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36944-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="36944-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="36944-156">NOTES</span></span>

## <span data-ttu-id="36944-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36944-157">RELATED LINKS</span></span>

[<span data-ttu-id="36944-158">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36944-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="36944-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="36944-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="36944-160">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36944-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="36944-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36944-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="36944-162">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36944-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="36944-163">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="36944-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


