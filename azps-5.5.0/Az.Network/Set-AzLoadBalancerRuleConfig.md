---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240568"
---
# <span data-ttu-id="ac0e0-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ac0e0-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="ac0e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0e0-103">Обновляет конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ac0e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac0e0-104">SYNTAX</span></span>

### <span data-ttu-id="ac0e0-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac0e0-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac0e0-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0e0-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac0e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac0e0-107">DESCRIPTION</span></span>
<span data-ttu-id="ac0e0-108">**Cmdlet Set-AzLoadBalancerRuleConfig** обновляет конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="ac0e0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac0e0-109">EXAMPLES</span></span>

### <span data-ttu-id="ac0e0-110">Пример 1. Изменение конфигурации правила балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="ac0e0-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="ac0e0-111">Первая команда получает балансировку нагрузки с именем MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="ac0e0-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb add-AzLoadBalancerRuleConfig, который добавляет в него правило NewRule.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="ac0e0-113">Третья команда передает балансиру нагрузки в **set-AzLoadBalancerRuleConfig,** который задает новую конфигурацию правила.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="ac0e0-114">Обратите внимание, что конфигурация не включает плавающий IP-адрес, который был включен предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="ac0e0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac0e0-115">PARAMETERS</span></span>

### <span data-ttu-id="ac0e0-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ac0e0-116">-BackendAddressPool</span></span>
<span data-ttu-id="ac0e0-117">Объект **BackendAddressPool,** который нужно связать с правилом балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="ac0e0-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ac0e0-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="ac0e0-119">Определяет ID объекта **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ac0e0-120">-BackendPort</span></span>
<span data-ttu-id="ac0e0-121">Определяет порт для трафика, на который совме задана конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0e0-122">-DefaultProfile</span></span>
<span data-ttu-id="ac0e0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac0e0-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="ac0e0-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="ac0e0-125">Настраивает SNAT для VMs в пуле backend, чтобы использовать общедоступный IP-адрес, указанный на переднем панели правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="ac0e0-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ac0e0-126">-EnableFloatingIP</span></span>
<span data-ttu-id="ac0e0-127">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ac0e0-128">-EnableTcpReset</span></span>
<span data-ttu-id="ac0e0-129">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ac0e0-130">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ac0e0-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac0e0-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ac0e0-132">Список IP-адресов, которые нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ac0e0-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ac0e0-134">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ac0e0-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac0e0-135">-FrontendPort</span></span>
<span data-ttu-id="ac0e0-136">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ac0e0-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ac0e0-138">Определяет продолжительность бесед (в минутах), в течение которых состояние бесед сохраняется на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ac0e0-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac0e0-139">-LoadBalancer</span></span>
<span data-ttu-id="ac0e0-140">Определяет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-140">Specifies a load balancer.</span></span>
<span data-ttu-id="ac0e0-141">Этот cmdlet обновляет конфигурацию правила для балансироса нагрузки, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac0e0-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="ac0e0-142">-LoadDistribution</span></span>
<span data-ttu-id="ac0e0-143">Определяет распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-143">Specifies a load distribution.</span></span>
<span data-ttu-id="ac0e0-144">Допустимыми значениями для этого параметра являются SourceIP и SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="ac0e0-145">-Name</span><span class="sxs-lookup"><span data-stu-id="ac0e0-145">-Name</span></span>
<span data-ttu-id="ac0e0-146">Указывает имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="ac0e0-147">-Размассив</span><span class="sxs-lookup"><span data-stu-id="ac0e0-147">-Probe</span></span>
<span data-ttu-id="ac0e0-148">Указывает, к каковую измеримую конфигурацию правил балансиров нагрузки можно связать.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-149">-Вадим-ИД</span><span class="sxs-lookup"><span data-stu-id="ac0e0-149">-ProbeId</span></span>
<span data-ttu-id="ac0e0-150">Определяет, как будет связываться этот документ с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="ac0e0-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ac0e0-151">-Protocol</span></span>
<span data-ttu-id="ac0e0-152">Протокол, который соответствует правилу балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="ac0e0-153">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ac0e0-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac0e0-154">-Confirm</span></span>
<span data-ttu-id="ac0e0-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac0e0-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac0e0-156">-WhatIf</span></span>
<span data-ttu-id="ac0e0-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac0e0-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac0e0-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0e0-159">CommonParameters</span></span>
<span data-ttu-id="ac0e0-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac0e0-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0e0-161">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac0e0-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0e0-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac0e0-162">INPUTS</span></span>

### <span data-ttu-id="ac0e0-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac0e0-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ac0e0-164">System.String</span><span class="sxs-lookup"><span data-stu-id="ac0e0-164">System.String</span></span>

### <span data-ttu-id="ac0e0-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ac0e0-165">System.Int32</span></span>

### <span data-ttu-id="ac0e0-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac0e0-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="ac0e0-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ac0e0-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="ac0e0-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="ac0e0-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="ac0e0-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac0e0-169">OUTPUTS</span></span>

### <span data-ttu-id="ac0e0-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ac0e0-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ac0e0-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac0e0-171">NOTES</span></span>

## <span data-ttu-id="ac0e0-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac0e0-172">RELATED LINKS</span></span>

[<span data-ttu-id="ac0e0-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ac0e0-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ac0e0-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ac0e0-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ac0e0-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ac0e0-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ac0e0-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ac0e0-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="ac0e0-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ac0e0-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


