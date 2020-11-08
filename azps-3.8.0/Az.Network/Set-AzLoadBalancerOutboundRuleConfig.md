---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066975"
---
# <span data-ttu-id="293dc-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="293dc-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="293dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="293dc-102">SYNOPSIS</span></span>
<span data-ttu-id="293dc-103">Задает конфигурацию исходящего правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="293dc-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="293dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="293dc-104">SYNTAX</span></span>

### <span data-ttu-id="293dc-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="293dc-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="293dc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="293dc-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="293dc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="293dc-107">DESCRIPTION</span></span>
<span data-ttu-id="293dc-108">Командлет **Set-AzLoadBalancerOutboundRuleConfig** задает конфигурацию исходящего правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="293dc-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="293dc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="293dc-109">EXAMPLES</span></span>

### <span data-ttu-id="293dc-110">Пример 1: изменение конфигурации правила исходящего трафика для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="293dc-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="293dc-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="293dc-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="293dc-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerOutboundRuleConfig, который добавляет в него конфигурацию исходящего правила.</span><span class="sxs-lookup"><span data-stu-id="293dc-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="293dc-113">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancerOutboundRuleConfig** , которая сохраняет и обновляет конфигурацию исходящего правила.</span><span class="sxs-lookup"><span data-stu-id="293dc-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="293dc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="293dc-114">PARAMETERS</span></span>

### <span data-ttu-id="293dc-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="293dc-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="293dc-116">Количество исходящих портов, используемых для NAT.</span><span class="sxs-lookup"><span data-stu-id="293dc-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="293dc-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="293dc-117">-BackendAddressPool</span></span>
<span data-ttu-id="293dc-118">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="293dc-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="293dc-119">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="293dc-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="293dc-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="293dc-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="293dc-121">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="293dc-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="293dc-122">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="293dc-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="293dc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293dc-123">-DefaultProfile</span></span>
<span data-ttu-id="293dc-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="293dc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293dc-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="293dc-125">-EnableTcpReset</span></span>
<span data-ttu-id="293dc-126">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="293dc-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="293dc-127">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="293dc-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="293dc-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="293dc-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="293dc-129">IP-адреса переднего плана для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="293dc-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="293dc-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="293dc-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="293dc-131">Время ожидания для подключения по протоколу бездействия TCP</span><span class="sxs-lookup"><span data-stu-id="293dc-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="293dc-132">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="293dc-132">-LoadBalancer</span></span>
<span data-ttu-id="293dc-133">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="293dc-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="293dc-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="293dc-134">-Name</span></span>
<span data-ttu-id="293dc-135">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="293dc-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="293dc-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="293dc-136">-Protocol</span></span>
<span data-ttu-id="293dc-137">Протокол TCP, UDP или ALL</span><span class="sxs-lookup"><span data-stu-id="293dc-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="293dc-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="293dc-138">-Confirm</span></span>
<span data-ttu-id="293dc-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="293dc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="293dc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="293dc-140">-WhatIf</span></span>
<span data-ttu-id="293dc-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="293dc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="293dc-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="293dc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="293dc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293dc-143">CommonParameters</span></span>
<span data-ttu-id="293dc-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="293dc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293dc-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293dc-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293dc-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="293dc-146">INPUTS</span></span>

### <span data-ttu-id="293dc-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="293dc-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="293dc-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="293dc-148">System.Int32</span></span>

### <span data-ttu-id="293dc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="293dc-149">System.String</span></span>

### <span data-ttu-id="293dc-150">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="293dc-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="293dc-151">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="293dc-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="293dc-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="293dc-152">OUTPUTS</span></span>

### <span data-ttu-id="293dc-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="293dc-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="293dc-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="293dc-154">NOTES</span></span>

## <span data-ttu-id="293dc-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="293dc-155">RELATED LINKS</span></span>

[<span data-ttu-id="293dc-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="293dc-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="293dc-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="293dc-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="293dc-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="293dc-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="293dc-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="293dc-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
