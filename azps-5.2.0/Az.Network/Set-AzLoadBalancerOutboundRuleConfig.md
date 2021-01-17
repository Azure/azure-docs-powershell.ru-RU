---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402876"
---
# <span data-ttu-id="9f55e-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f55e-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="9f55e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f55e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f55e-103">Настраивает исходящие правила для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f55e-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="9f55e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f55e-104">SYNTAX</span></span>

### <span data-ttu-id="9f55e-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f55e-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f55e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9f55e-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f55e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f55e-107">DESCRIPTION</span></span>
<span data-ttu-id="9f55e-108">Cmdlet **Set-AzLoadBalancerOutboundRuleConfig** настраивает исходящие правила для балансиров нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9f55e-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9f55e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f55e-109">EXAMPLES</span></span>

### <span data-ttu-id="9f55e-110">Пример 1. Изменение конфигурации правил исходящие для балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="9f55e-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="9f55e-111">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="9f55e-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="9f55e-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb Add-AzLoadBalancerOutboundRuleConfig, который добавляет в него конфигурацию исходящие правила.</span><span class="sxs-lookup"><span data-stu-id="9f55e-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="9f55e-113">Третья команда передает балансиру нагрузки в **Set-AzLoadBalancerOutboundRuleConfig,** который сохраняет и обновляет конфигурацию исходящие правила.</span><span class="sxs-lookup"><span data-stu-id="9f55e-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="9f55e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f55e-114">PARAMETERS</span></span>

### <span data-ttu-id="9f55e-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="9f55e-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="9f55e-116">Количество исходящие порты, используемые для NAT.</span><span class="sxs-lookup"><span data-stu-id="9f55e-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="9f55e-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f55e-117">-BackendAddressPool</span></span>
<span data-ttu-id="9f55e-118">Ссылка на пул ДИПов.</span><span class="sxs-lookup"><span data-stu-id="9f55e-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="9f55e-119">Исходящие потоки случайным образом балансирует нагрузка по IPS на backend IPS.</span><span class="sxs-lookup"><span data-stu-id="9f55e-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="9f55e-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9f55e-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="9f55e-121">Ссылка на пул ДИПов.</span><span class="sxs-lookup"><span data-stu-id="9f55e-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="9f55e-122">Исходящие потоки случайным образом балансирует нагрузка по IPS на backend IPS.</span><span class="sxs-lookup"><span data-stu-id="9f55e-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="9f55e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f55e-123">-DefaultProfile</span></span>
<span data-ttu-id="9f55e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f55e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f55e-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9f55e-125">-EnableTcpReset</span></span>
<span data-ttu-id="9f55e-126">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="9f55e-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="9f55e-127">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="9f55e-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9f55e-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f55e-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9f55e-129">IP-адреса переднего ip-адреса балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f55e-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="9f55e-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9f55e-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9f55e-131">Время ожидания для неавтайного подключения TCP</span><span class="sxs-lookup"><span data-stu-id="9f55e-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="9f55e-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9f55e-132">-LoadBalancer</span></span>
<span data-ttu-id="9f55e-133">Ссылка на ресурс балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9f55e-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="9f55e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="9f55e-134">-Name</span></span>
<span data-ttu-id="9f55e-135">Имя правила исходящие.</span><span class="sxs-lookup"><span data-stu-id="9f55e-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="9f55e-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9f55e-136">-Protocol</span></span>
<span data-ttu-id="9f55e-137">Протокол TCP, UDP или All</span><span class="sxs-lookup"><span data-stu-id="9f55e-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="9f55e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f55e-138">-Confirm</span></span>
<span data-ttu-id="9f55e-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f55e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f55e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f55e-140">-WhatIf</span></span>
<span data-ttu-id="9f55e-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f55e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f55e-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f55e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f55e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f55e-143">CommonParameters</span></span>
<span data-ttu-id="9f55e-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f55e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f55e-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f55e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f55e-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f55e-146">INPUTS</span></span>

### <span data-ttu-id="9f55e-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9f55e-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9f55e-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9f55e-148">System.Int32</span></span>

### <span data-ttu-id="9f55e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9f55e-149">System.String</span></span>

### <span data-ttu-id="9f55e-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="9f55e-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="9f55e-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9f55e-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9f55e-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f55e-152">OUTPUTS</span></span>

### <span data-ttu-id="9f55e-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9f55e-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9f55e-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f55e-154">NOTES</span></span>

## <span data-ttu-id="9f55e-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f55e-155">RELATED LINKS</span></span>

[<span data-ttu-id="9f55e-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f55e-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9f55e-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f55e-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9f55e-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f55e-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9f55e-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9f55e-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
