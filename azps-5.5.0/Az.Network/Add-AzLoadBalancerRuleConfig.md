---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221329"
---
# <span data-ttu-id="17fcb-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17fcb-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="17fcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="17fcb-103">Добавляет конфигурацию правил в балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="17fcb-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="17fcb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17fcb-104">SYNTAX</span></span>

### <span data-ttu-id="17fcb-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17fcb-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17fcb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="17fcb-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17fcb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17fcb-107">DESCRIPTION</span></span>
<span data-ttu-id="17fcb-108">Для балансиента нагрузки Azure конфигурацию правил добавляет **add-AzLoadBalancerRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="17fcb-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="17fcb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17fcb-109">EXAMPLES</span></span>

### <span data-ttu-id="17fcb-110">Пример 1. Добавление конфигурации правил для балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="17fcb-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="17fcb-111">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="17fcb-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="17fcb-112">Вторая команда передает балансиру нагрузки в $slb **add-AzLoadBalancerRuleConfig,** который добавляет конфигурацию правил с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="17fcb-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="17fcb-113">Третья команда обновляет балансировку нагрузки в Azure с помощью нового config для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="17fcb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17fcb-114">PARAMETERS</span></span>

### <span data-ttu-id="17fcb-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="17fcb-115">-BackendAddressPool</span></span>
<span data-ttu-id="17fcb-116">Определяет пул адресов для загрузки, который нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="17fcb-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="17fcb-118">Определяет ID объекта **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="17fcb-119">-BackendPort</span></span>
<span data-ttu-id="17fcb-120">Определяет порт для трафика, который соответствует конфигурации правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fcb-121">-DefaultProfile</span></span>
<span data-ttu-id="17fcb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17fcb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17fcb-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="17fcb-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="17fcb-124">Настраивает SNAT для VMs в пуле backend, чтобы использовать общедоступный АДРЕСIP, указанный на переднем панели правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="17fcb-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="17fcb-125">-EnableFloatingIP</span></span>
<span data-ttu-id="17fcb-126">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="17fcb-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="17fcb-127">-EnableTcpReset</span></span>
<span data-ttu-id="17fcb-128">Получите раздвивный TCP-сброс при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="17fcb-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="17fcb-129">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="17fcb-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="17fcb-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="17fcb-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="17fcb-131">Список IP-адресов, которые нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="17fcb-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="17fcb-133">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="17fcb-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="17fcb-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="17fcb-134">-FrontendPort</span></span>
<span data-ttu-id="17fcb-135">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="17fcb-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="17fcb-137">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="17fcb-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17fcb-138">-LoadBalancer</span></span>
<span data-ttu-id="17fcb-139">Определяет объект **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="17fcb-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="17fcb-140">Этот cmdlet добавляет конфигурацию правил к балансе нагрузки, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="17fcb-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="17fcb-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="17fcb-141">-LoadDistribution</span></span>
<span data-ttu-id="17fcb-142">Определяет распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="17fcb-143">-Name</span><span class="sxs-lookup"><span data-stu-id="17fcb-143">-Name</span></span>
<span data-ttu-id="17fcb-144">Указывает имя конфигурации правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-145">-Разротные</span><span class="sxs-lookup"><span data-stu-id="17fcb-145">-Probe</span></span>
<span data-ttu-id="17fcb-146">Указывает, к каковую измеримую конфигурацию правил балансиров нагрузки можно связать.</span><span class="sxs-lookup"><span data-stu-id="17fcb-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-147">-Вадим-ИД</span><span class="sxs-lookup"><span data-stu-id="17fcb-147">-ProbeId</span></span>
<span data-ttu-id="17fcb-148">Определяет, как будет связываться этот документ с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="17fcb-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="17fcb-149">-Protocol</span></span>
<span data-ttu-id="17fcb-150">Протокол, который соответствует правилу балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17fcb-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="17fcb-151">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="17fcb-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="17fcb-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17fcb-152">-Confirm</span></span>
<span data-ttu-id="17fcb-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fcb-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17fcb-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fcb-154">-WhatIf</span></span>
<span data-ttu-id="17fcb-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fcb-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17fcb-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17fcb-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17fcb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fcb-157">CommonParameters</span></span>
<span data-ttu-id="17fcb-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fcb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fcb-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fcb-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fcb-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17fcb-160">INPUTS</span></span>

### <span data-ttu-id="17fcb-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17fcb-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="17fcb-162">System.String</span><span class="sxs-lookup"><span data-stu-id="17fcb-162">System.String</span></span>

### <span data-ttu-id="17fcb-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="17fcb-163">System.Int32</span></span>

### <span data-ttu-id="17fcb-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="17fcb-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="17fcb-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="17fcb-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="17fcb-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="17fcb-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="17fcb-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17fcb-167">OUTPUTS</span></span>

### <span data-ttu-id="17fcb-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17fcb-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="17fcb-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17fcb-169">NOTES</span></span>

## <span data-ttu-id="17fcb-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17fcb-170">RELATED LINKS</span></span>

[<span data-ttu-id="17fcb-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17fcb-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="17fcb-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17fcb-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="17fcb-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17fcb-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="17fcb-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17fcb-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="17fcb-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17fcb-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


