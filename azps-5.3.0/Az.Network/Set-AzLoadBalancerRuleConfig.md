---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517962"
---
# <span data-ttu-id="4ae58-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ae58-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4ae58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae58-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae58-103">Обновляет конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4ae58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ae58-104">SYNTAX</span></span>

### <span data-ttu-id="4ae58-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ae58-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ae58-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae58-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ae58-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ae58-107">DESCRIPTION</span></span>
<span data-ttu-id="4ae58-108">**Cmdlet Set-AzLoadBalancerRuleConfig** обновляет конфигурацию правил для балансиента нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4ae58-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ae58-109">EXAMPLES</span></span>

### <span data-ttu-id="4ae58-110">Пример 1. Изменение конфигурации правила балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="4ae58-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="4ae58-111">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="4ae58-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4ae58-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb add-AzLoadBalancerRuleConfig, который добавляет в него правило NewRule.</span><span class="sxs-lookup"><span data-stu-id="4ae58-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="4ae58-113">Третья команда передает балансиру нагрузки в **set-AzLoadBalancerRuleConfig,** который задает новую конфигурацию правила.</span><span class="sxs-lookup"><span data-stu-id="4ae58-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="4ae58-114">Обратите внимание, что конфигурация не включает плавающий IP-адрес, который был включен предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="4ae58-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="4ae58-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ae58-115">PARAMETERS</span></span>

### <span data-ttu-id="4ae58-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ae58-116">-BackendAddressPool</span></span>
<span data-ttu-id="4ae58-117">Объект **BackendAddressPool,** который нужно связать с правилом балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4ae58-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="4ae58-119">Определяет ID объекта **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4ae58-120">-BackendPort</span></span>
<span data-ttu-id="4ae58-121">Определяет порт для трафика, на который совме задана конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="4ae58-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="4ae58-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae58-122">-DefaultProfile</span></span>
<span data-ttu-id="4ae58-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ae58-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae58-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="4ae58-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="4ae58-125">Настраивает SNAT для VMs в пуле backend, чтобы использовать общедоступный IP-адрес, указанный на переднем панели правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="4ae58-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4ae58-126">-EnableFloatingIP</span></span>
<span data-ttu-id="4ae58-127">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="4ae58-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4ae58-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4ae58-128">-EnableTcpReset</span></span>
<span data-ttu-id="4ae58-129">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="4ae58-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4ae58-130">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="4ae58-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4ae58-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ae58-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4ae58-132">Список IP-адресов, которые нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4ae58-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4ae58-134">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="4ae58-134">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4ae58-135">-FrontendPort</span></span>
<span data-ttu-id="4ae58-136">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4ae58-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4ae58-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4ae58-138">Определяет продолжительность бесед (в минутах), в течение которых состояние бесед сохраняется на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="4ae58-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae58-139">-LoadBalancer</span></span>
<span data-ttu-id="4ae58-140">Определяет балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="4ae58-140">Specifies a load balancer.</span></span>
<span data-ttu-id="4ae58-141">Этот cmdlet обновляет конфигурацию правила для балансироса нагрузки, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4ae58-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ae58-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="4ae58-142">-LoadDistribution</span></span>
<span data-ttu-id="4ae58-143">Определяет распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-143">Specifies a load distribution.</span></span>
<span data-ttu-id="4ae58-144">Допустимыми значениями для этого параметра являются SourceIP и SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="4ae58-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-145">-Name</span><span class="sxs-lookup"><span data-stu-id="4ae58-145">-Name</span></span>
<span data-ttu-id="4ae58-146">Указывает имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="4ae58-147">-Разротные</span><span class="sxs-lookup"><span data-stu-id="4ae58-147">-Probe</span></span>
<span data-ttu-id="4ae58-148">Указывает, к каковую измеримую конфигурацию правил балансиров нагрузки можно связать.</span><span class="sxs-lookup"><span data-stu-id="4ae58-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-149">-Тем нее</span><span class="sxs-lookup"><span data-stu-id="4ae58-149">-ProbeId</span></span>
<span data-ttu-id="4ae58-150">Определяет, как будет связываться этот документ с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4ae58-151">-Protocol</span></span>
<span data-ttu-id="4ae58-152">Протокол, который соответствует правилу балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ae58-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="4ae58-153">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="4ae58-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae58-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ae58-154">-Confirm</span></span>
<span data-ttu-id="4ae58-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ae58-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ae58-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ae58-156">-WhatIf</span></span>
<span data-ttu-id="4ae58-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ae58-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ae58-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ae58-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ae58-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae58-159">CommonParameters</span></span>
<span data-ttu-id="4ae58-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae58-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae58-161">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae58-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae58-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ae58-162">INPUTS</span></span>

### <span data-ttu-id="4ae58-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae58-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4ae58-164">System.String</span><span class="sxs-lookup"><span data-stu-id="4ae58-164">System.String</span></span>

### <span data-ttu-id="4ae58-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4ae58-165">System.Int32</span></span>

### <span data-ttu-id="4ae58-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ae58-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="4ae58-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ae58-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="4ae58-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="4ae58-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="4ae58-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ae58-169">OUTPUTS</span></span>

### <span data-ttu-id="4ae58-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae58-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4ae58-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ae58-171">NOTES</span></span>

## <span data-ttu-id="4ae58-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ae58-172">RELATED LINKS</span></span>

[<span data-ttu-id="4ae58-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ae58-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4ae58-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ae58-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4ae58-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ae58-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4ae58-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ae58-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4ae58-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ae58-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


