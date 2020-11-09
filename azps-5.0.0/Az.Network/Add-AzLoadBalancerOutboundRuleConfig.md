---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319262"
---
# <span data-ttu-id="80514-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80514-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="80514-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80514-102">SYNOPSIS</span></span>
<span data-ttu-id="80514-103">Добавляет конфигурацию исходящего правила в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="80514-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="80514-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80514-104">SYNTAX</span></span>

### <span data-ttu-id="80514-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80514-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80514-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="80514-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80514-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80514-107">DESCRIPTION</span></span>
<span data-ttu-id="80514-108">Командлет **Add-AzLoadBalancerOutboundRuleConfig** добавляет конфигурацию исходящего правила в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="80514-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="80514-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80514-109">EXAMPLES</span></span>

### <span data-ttu-id="80514-110">Пример 1: Добавление конфигурации исходящего правила в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="80514-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="80514-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="80514-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="80514-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzLoadBalancerOutboundRuleConfig** , который добавляет конфигурацию исходящего правила в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="80514-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="80514-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80514-113">PARAMETERS</span></span>

### <span data-ttu-id="80514-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="80514-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="80514-115">Количество исходящих портов, используемых для NAT.</span><span class="sxs-lookup"><span data-stu-id="80514-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80514-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="80514-116">-BackendAddressPool</span></span>
<span data-ttu-id="80514-117">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="80514-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="80514-118">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="80514-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80514-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="80514-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="80514-120">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="80514-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="80514-121">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="80514-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="80514-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80514-122">-DefaultProfile</span></span>
<span data-ttu-id="80514-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80514-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80514-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="80514-124">-EnableTcpReset</span></span>
<span data-ttu-id="80514-125">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="80514-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="80514-126">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="80514-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="80514-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="80514-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="80514-128">IP-адреса переднего плана для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="80514-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80514-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="80514-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="80514-130">Время ожидания для подключения по протоколу бездействия TCP</span><span class="sxs-lookup"><span data-stu-id="80514-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80514-131">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="80514-131">-LoadBalancer</span></span>
<span data-ttu-id="80514-132">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="80514-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="80514-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80514-133">-Name</span></span>
<span data-ttu-id="80514-134">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="80514-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="80514-135">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="80514-135">-Protocol</span></span>
<span data-ttu-id="80514-136">Протокол TCP, UDP или ALL</span><span class="sxs-lookup"><span data-stu-id="80514-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="80514-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80514-137">-Confirm</span></span>
<span data-ttu-id="80514-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80514-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80514-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80514-139">-WhatIf</span></span>
<span data-ttu-id="80514-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80514-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80514-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80514-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80514-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80514-142">CommonParameters</span></span>
<span data-ttu-id="80514-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80514-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80514-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80514-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80514-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80514-145">INPUTS</span></span>

### <span data-ttu-id="80514-146">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80514-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="80514-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="80514-147">System.Int32</span></span>

### <span data-ttu-id="80514-148">System. String</span><span class="sxs-lookup"><span data-stu-id="80514-148">System.String</span></span>

### <span data-ttu-id="80514-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="80514-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="80514-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="80514-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="80514-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80514-151">OUTPUTS</span></span>

### <span data-ttu-id="80514-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80514-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="80514-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="80514-153">NOTES</span></span>

## <span data-ttu-id="80514-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80514-154">RELATED LINKS</span></span>

[<span data-ttu-id="80514-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80514-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="80514-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80514-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="80514-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80514-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="80514-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="80514-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)