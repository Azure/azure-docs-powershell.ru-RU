---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 76adf0c831b79b219598a254a859b8603f8c3f27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003432"
---
# <span data-ttu-id="35038-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35038-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="35038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35038-102">SYNOPSIS</span></span>
<span data-ttu-id="35038-103">Настраивает исходящие правила для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="35038-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="35038-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35038-104">SYNTAX</span></span>

### <span data-ttu-id="35038-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35038-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35038-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="35038-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35038-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35038-107">DESCRIPTION</span></span>
<span data-ttu-id="35038-108">Cmdlet **Set-AzLoadBalancerOutboundRuleConfig** настраивает исходящие правила для балансиров нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="35038-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="35038-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35038-109">EXAMPLES</span></span>

### <span data-ttu-id="35038-110">Пример 1. Изменение конфигурации правил исходящие для балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="35038-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="35038-111">Первая команда получает балансировку нагрузки с именем MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="35038-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="35038-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb add-AzLoadBalancerOutboundRuleConfig, который добавляет в него конфигурацию исходящие правила.</span><span class="sxs-lookup"><span data-stu-id="35038-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="35038-113">Третья команда передает балансиру нагрузки в **Set-AzLoadBalancerOutboundRuleConfig,** который сохраняет и обновляет конфигурацию исходящие правила.</span><span class="sxs-lookup"><span data-stu-id="35038-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="35038-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35038-114">PARAMETERS</span></span>

### <span data-ttu-id="35038-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="35038-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="35038-116">Количество исходящие порты, используемые для NAT.</span><span class="sxs-lookup"><span data-stu-id="35038-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="35038-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35038-117">-BackendAddressPool</span></span>
<span data-ttu-id="35038-118">Ссылка на пул дипов.</span><span class="sxs-lookup"><span data-stu-id="35038-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="35038-119">Исходящие потоки случайным образом балансирует нагрузка по IP на backend IPS.</span><span class="sxs-lookup"><span data-stu-id="35038-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="35038-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="35038-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="35038-121">Ссылка на пул ДИПов.</span><span class="sxs-lookup"><span data-stu-id="35038-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="35038-122">Исходящие потоки случайным образом балансирует нагрузка по IP на backend IPS.</span><span class="sxs-lookup"><span data-stu-id="35038-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="35038-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35038-123">-DefaultProfile</span></span>
<span data-ttu-id="35038-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35038-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35038-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="35038-125">-EnableTcpReset</span></span>
<span data-ttu-id="35038-126">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="35038-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="35038-127">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="35038-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="35038-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="35038-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="35038-129">IP-адреса переднего ip-адреса балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="35038-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="35038-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="35038-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="35038-131">Время ожидания для неавтайного подключения TCP</span><span class="sxs-lookup"><span data-stu-id="35038-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="35038-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35038-132">-LoadBalancer</span></span>
<span data-ttu-id="35038-133">Ссылка на ресурс балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="35038-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="35038-134">-Name</span><span class="sxs-lookup"><span data-stu-id="35038-134">-Name</span></span>
<span data-ttu-id="35038-135">Имя правила исходящие.</span><span class="sxs-lookup"><span data-stu-id="35038-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="35038-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="35038-136">-Protocol</span></span>
<span data-ttu-id="35038-137">Протокол TCP, UDP или All</span><span class="sxs-lookup"><span data-stu-id="35038-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="35038-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35038-138">-Confirm</span></span>
<span data-ttu-id="35038-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35038-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35038-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35038-140">-WhatIf</span></span>
<span data-ttu-id="35038-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35038-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35038-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35038-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35038-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35038-143">CommonParameters</span></span>
<span data-ttu-id="35038-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35038-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35038-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35038-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35038-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35038-146">INPUTS</span></span>

### <span data-ttu-id="35038-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35038-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="35038-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="35038-148">System.Int32</span></span>

### <span data-ttu-id="35038-149">System.String</span><span class="sxs-lookup"><span data-stu-id="35038-149">System.String</span></span>

### <span data-ttu-id="35038-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="35038-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="35038-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35038-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="35038-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35038-152">OUTPUTS</span></span>

### <span data-ttu-id="35038-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35038-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="35038-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35038-154">NOTES</span></span>

## <span data-ttu-id="35038-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35038-155">RELATED LINKS</span></span>

[<span data-ttu-id="35038-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35038-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="35038-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35038-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="35038-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35038-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="35038-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35038-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
