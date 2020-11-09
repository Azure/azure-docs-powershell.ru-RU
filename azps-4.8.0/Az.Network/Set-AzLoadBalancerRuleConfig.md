---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244775"
---
# <span data-ttu-id="39c98-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c98-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="39c98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39c98-102">SYNOPSIS</span></span>
<span data-ttu-id="39c98-103">Обновляет конфигурацию правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="39c98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39c98-104">SYNTAX</span></span>

### <span data-ttu-id="39c98-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39c98-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39c98-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="39c98-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c98-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c98-107">DESCRIPTION</span></span>
<span data-ttu-id="39c98-108">Командлет **Set-AzLoadBalancerRuleConfig** обновляет конфигурацию правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="39c98-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39c98-109">EXAMPLES</span></span>

### <span data-ttu-id="39c98-110">Пример 1: изменение конфигурации правила балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="39c98-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="39c98-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="39c98-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="39c98-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerRuleConfig, который добавляет к нему правило с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="39c98-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="39c98-113">Третья команда передает балансировщик нагрузки на **Set-AzLoadBalancerRuleConfig** , который задает новую конфигурацию правила.</span><span class="sxs-lookup"><span data-stu-id="39c98-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="39c98-114">Обратите внимание, что в конфигурации не разрешается использование плавающего IP-адреса, который был включен с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="39c98-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="39c98-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39c98-115">PARAMETERS</span></span>

### <span data-ttu-id="39c98-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39c98-116">-BackendAddressPool</span></span>
<span data-ttu-id="39c98-117">Указывает объект **BackendAddressPool** , который нужно связать с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="39c98-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="39c98-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="39c98-119">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39c98-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="39c98-120">-BackendPort</span></span>
<span data-ttu-id="39c98-121">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="39c98-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="39c98-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c98-122">-DefaultProfile</span></span>
<span data-ttu-id="39c98-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39c98-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c98-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="39c98-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="39c98-125">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="39c98-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="39c98-126">-EnableFloatingIP</span></span>
<span data-ttu-id="39c98-127">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="39c98-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="39c98-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="39c98-128">-EnableTcpReset</span></span>
<span data-ttu-id="39c98-129">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="39c98-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="39c98-130">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="39c98-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="39c98-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="39c98-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="39c98-132">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39c98-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="39c98-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="39c98-134">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="39c98-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="39c98-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="39c98-135">-FrontendPort</span></span>
<span data-ttu-id="39c98-136">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39c98-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="39c98-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="39c98-138">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="39c98-139">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="39c98-139">-LoadBalancer</span></span>
<span data-ttu-id="39c98-140">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-140">Specifies a load balancer.</span></span>
<span data-ttu-id="39c98-141">Этот командлет обновляет конфигурацию правила для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="39c98-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="39c98-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="39c98-142">-LoadDistribution</span></span>
<span data-ttu-id="39c98-143">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-143">Specifies a load distribution.</span></span>
<span data-ttu-id="39c98-144">Допустимые значения этого параметра: SourceIP и SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="39c98-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="39c98-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39c98-145">-Name</span></span>
<span data-ttu-id="39c98-146">Указывает имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="39c98-147">-Зонд</span><span class="sxs-lookup"><span data-stu-id="39c98-147">-Probe</span></span>
<span data-ttu-id="39c98-148">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39c98-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="39c98-149">-ProbeId</span></span>
<span data-ttu-id="39c98-150">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="39c98-151">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="39c98-151">-Protocol</span></span>
<span data-ttu-id="39c98-152">Указывает протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="39c98-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="39c98-153">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="39c98-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="39c98-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c98-154">-Confirm</span></span>
<span data-ttu-id="39c98-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39c98-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c98-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c98-156">-WhatIf</span></span>
<span data-ttu-id="39c98-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39c98-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39c98-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39c98-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c98-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c98-159">CommonParameters</span></span>
<span data-ttu-id="39c98-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39c98-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c98-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39c98-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c98-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39c98-162">INPUTS</span></span>

### <span data-ttu-id="39c98-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39c98-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="39c98-164">System. String</span><span class="sxs-lookup"><span data-stu-id="39c98-164">System.String</span></span>

### <span data-ttu-id="39c98-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="39c98-165">System.Int32</span></span>

### <span data-ttu-id="39c98-166">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="39c98-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="39c98-167">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="39c98-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="39c98-168">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="39c98-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="39c98-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c98-169">OUTPUTS</span></span>

### <span data-ttu-id="39c98-170">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="39c98-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="39c98-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="39c98-171">NOTES</span></span>

## <span data-ttu-id="39c98-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39c98-172">RELATED LINKS</span></span>

[<span data-ttu-id="39c98-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c98-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39c98-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c98-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39c98-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c98-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39c98-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c98-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="39c98-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39c98-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

