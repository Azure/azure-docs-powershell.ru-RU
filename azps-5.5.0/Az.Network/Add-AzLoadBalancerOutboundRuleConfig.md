---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228017"
---
# <span data-ttu-id="b64ea-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b64ea-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="b64ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b64ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b64ea-103">Добавляет конфигурацию исходящие правила в балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b64ea-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="b64ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b64ea-104">SYNTAX</span></span>

### <span data-ttu-id="b64ea-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b64ea-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b64ea-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b64ea-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b64ea-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b64ea-107">DESCRIPTION</span></span>
<span data-ttu-id="b64ea-108">Cmdlet **Add-AzLoadBalancerOutboundRuleConfig** добавляет конфигурацию исходящие правила к балансиру нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="b64ea-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b64ea-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b64ea-109">EXAMPLES</span></span>

### <span data-ttu-id="b64ea-110">Пример 1. Добавление конфигурации исходящие правила для балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="b64ea-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="b64ea-111">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="b64ea-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="b64ea-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb **add-AzLoadBalancerOutboundRuleConfig,** который добавляет конфигурацию правил исходящие в балансиру нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b64ea-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="b64ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b64ea-113">PARAMETERS</span></span>

### <span data-ttu-id="b64ea-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="b64ea-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="b64ea-115">Количество исходящие порты, которые будут использоваться для NAT.</span><span class="sxs-lookup"><span data-stu-id="b64ea-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="b64ea-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b64ea-116">-BackendAddressPool</span></span>
<span data-ttu-id="b64ea-117">Ссылка на пул дипов.</span><span class="sxs-lookup"><span data-stu-id="b64ea-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="b64ea-118">Исходящие потоки случайным образом балансирует нагрузка по IPs в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="b64ea-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="b64ea-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b64ea-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="b64ea-120">Ссылка на пул дипов.</span><span class="sxs-lookup"><span data-stu-id="b64ea-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="b64ea-121">Исходящие потоки случайным образом балансирует нагрузка по IPs в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="b64ea-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="b64ea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64ea-122">-DefaultProfile</span></span>
<span data-ttu-id="b64ea-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b64ea-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64ea-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b64ea-124">-EnableTcpReset</span></span>
<span data-ttu-id="b64ea-125">Получите раздвивный TCP-сброс при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="b64ea-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="b64ea-126">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="b64ea-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b64ea-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b64ea-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b64ea-128">IP-адреса переднего ip-адреса балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b64ea-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="b64ea-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b64ea-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b64ea-130">Время ожидания для неавтайного подключения TCP</span><span class="sxs-lookup"><span data-stu-id="b64ea-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="b64ea-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b64ea-131">-LoadBalancer</span></span>
<span data-ttu-id="b64ea-132">Ссылка на ресурс балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b64ea-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="b64ea-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b64ea-133">-Name</span></span>
<span data-ttu-id="b64ea-134">Имя правила исходящие.</span><span class="sxs-lookup"><span data-stu-id="b64ea-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="b64ea-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b64ea-135">-Protocol</span></span>
<span data-ttu-id="b64ea-136">Протокол TCP, UDP или All</span><span class="sxs-lookup"><span data-stu-id="b64ea-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="b64ea-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b64ea-137">-Confirm</span></span>
<span data-ttu-id="b64ea-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b64ea-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64ea-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64ea-139">-WhatIf</span></span>
<span data-ttu-id="b64ea-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b64ea-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b64ea-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b64ea-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64ea-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64ea-142">CommonParameters</span></span>
<span data-ttu-id="b64ea-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b64ea-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64ea-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b64ea-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64ea-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b64ea-145">INPUTS</span></span>

### <span data-ttu-id="b64ea-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b64ea-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b64ea-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b64ea-147">System.Int32</span></span>

### <span data-ttu-id="b64ea-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b64ea-148">System.String</span></span>

### <span data-ttu-id="b64ea-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="b64ea-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="b64ea-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b64ea-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b64ea-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b64ea-151">OUTPUTS</span></span>

### <span data-ttu-id="b64ea-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b64ea-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b64ea-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b64ea-153">NOTES</span></span>

## <span data-ttu-id="b64ea-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b64ea-154">RELATED LINKS</span></span>

[<span data-ttu-id="b64ea-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b64ea-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b64ea-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b64ea-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b64ea-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b64ea-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="b64ea-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b64ea-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
