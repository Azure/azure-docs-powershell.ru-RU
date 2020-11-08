---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247044"
---
# <span data-ttu-id="a24c6-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a24c6-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a24c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a24c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a24c6-103">Добавляет конфигурацию правила в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="a24c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a24c6-104">SYNTAX</span></span>

### <span data-ttu-id="a24c6-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a24c6-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24c6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a24c6-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24c6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a24c6-107">DESCRIPTION</span></span>
<span data-ttu-id="a24c6-108">Командлет **Add-AzLoadBalancerRuleConfig** добавляет конфигурацию правил в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a24c6-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a24c6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a24c6-109">EXAMPLES</span></span>

### <span data-ttu-id="a24c6-110">Пример 1: Добавление конфигурации правила в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a24c6-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="a24c6-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="a24c6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="a24c6-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzLoadBalancerRuleConfig** , который добавляет конфигурацию правила с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="a24c6-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="a24c6-113">Третья команда обновит подсистему балансировки нагрузки в Azure с помощью новой конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="a24c6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a24c6-114">PARAMETERS</span></span>

### <span data-ttu-id="a24c6-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a24c6-115">-BackendAddressPool</span></span>
<span data-ttu-id="a24c6-116">Указывает пул серверных адресов, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a24c6-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="a24c6-118">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a24c6-119">-BackendPort</span></span>
<span data-ttu-id="a24c6-120">Указывает внутренний порт для трафика, соответствующего конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24c6-121">-DefaultProfile</span></span>
<span data-ttu-id="a24c6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a24c6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24c6-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="a24c6-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="a24c6-124">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="a24c6-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a24c6-125">-EnableFloatingIP</span></span>
<span data-ttu-id="a24c6-126">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="a24c6-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a24c6-127">-EnableTcpReset</span></span>
<span data-ttu-id="a24c6-128">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="a24c6-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a24c6-129">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="a24c6-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a24c6-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24c6-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a24c6-131">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a24c6-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a24c6-133">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a24c6-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a24c6-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a24c6-134">-FrontendPort</span></span>
<span data-ttu-id="a24c6-135">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a24c6-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a24c6-137">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="a24c6-138">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a24c6-138">-LoadBalancer</span></span>
<span data-ttu-id="a24c6-139">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="a24c6-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a24c6-140">Этот командлет добавляет конфигурацию правила в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="a24c6-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24c6-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="a24c6-141">-LoadDistribution</span></span>
<span data-ttu-id="a24c6-142">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="a24c6-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a24c6-143">-Name</span></span>
<span data-ttu-id="a24c6-144">Указывает имя конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-145">-Зонд</span><span class="sxs-lookup"><span data-stu-id="a24c6-145">-Probe</span></span>
<span data-ttu-id="a24c6-146">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a24c6-147">-ProbeId</span></span>
<span data-ttu-id="a24c6-148">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a24c6-149">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="a24c6-149">-Protocol</span></span>
<span data-ttu-id="a24c6-150">Указывает протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a24c6-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="a24c6-151">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="a24c6-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a24c6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a24c6-152">-Confirm</span></span>
<span data-ttu-id="a24c6-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a24c6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a24c6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24c6-154">-WhatIf</span></span>
<span data-ttu-id="a24c6-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a24c6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a24c6-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a24c6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a24c6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24c6-157">CommonParameters</span></span>
<span data-ttu-id="a24c6-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a24c6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24c6-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24c6-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24c6-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a24c6-160">INPUTS</span></span>

### <span data-ttu-id="a24c6-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a24c6-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a24c6-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a24c6-162">System.String</span></span>

### <span data-ttu-id="a24c6-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a24c6-163">System.Int32</span></span>

### <span data-ttu-id="a24c6-164">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24c6-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="a24c6-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a24c6-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="a24c6-166">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="a24c6-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="a24c6-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a24c6-167">OUTPUTS</span></span>

### <span data-ttu-id="a24c6-168">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a24c6-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a24c6-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="a24c6-169">NOTES</span></span>

## <span data-ttu-id="a24c6-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a24c6-170">RELATED LINKS</span></span>

[<span data-ttu-id="a24c6-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a24c6-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a24c6-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a24c6-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a24c6-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a24c6-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a24c6-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a24c6-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a24c6-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a24c6-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


