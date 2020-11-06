---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: a584d473354fd900b117f5661dc738b239f3a92d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565849"
---
# <span data-ttu-id="4997a-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4997a-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4997a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4997a-102">SYNOPSIS</span></span>
<span data-ttu-id="4997a-103">Задает состояние цели для конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4997a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4997a-104">SYNTAX</span></span>

### <span data-ttu-id="4997a-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4997a-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4997a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4997a-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4997a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4997a-107">DESCRIPTION</span></span>
<span data-ttu-id="4997a-108">Командлет **Set-AzureRmLoadBalancerRuleConfig** задает состояние цели для конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="4997a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4997a-109">EXAMPLES</span></span>

### <span data-ttu-id="4997a-110">Пример 1: изменение конфигурации правила балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="4997a-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="4997a-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="4997a-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4997a-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerRuleConfig, который добавляет к нему правило с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="4997a-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="4997a-113">Третья команда передает балансировщик нагрузки на **Set-AzureRmLoadBalancerRuleConfig** , который задает новую конфигурацию правила.</span><span class="sxs-lookup"><span data-stu-id="4997a-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="4997a-114">Обратите внимание, что в конфигурации не разрешается использование плавающего IP-адреса, который был включен с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="4997a-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="4997a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4997a-115">PARAMETERS</span></span>

### <span data-ttu-id="4997a-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4997a-116">-BackendAddressPool</span></span>
<span data-ttu-id="4997a-117">Указывает объект **BackendAddressPool** , который нужно связать с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="4997a-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4997a-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="4997a-119">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4997a-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4997a-120">-BackendPort</span></span>
<span data-ttu-id="4997a-121">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="4997a-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="4997a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4997a-122">-DefaultProfile</span></span>
<span data-ttu-id="4997a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4997a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4997a-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="4997a-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="4997a-125">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="4997a-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4997a-126">-EnableFloatingIP</span></span>
<span data-ttu-id="4997a-127">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="4997a-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4997a-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4997a-128">-EnableTcpReset</span></span>
<span data-ttu-id="4997a-129">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="4997a-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4997a-130">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="4997a-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4997a-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4997a-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4997a-132">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4997a-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4997a-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4997a-134">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="4997a-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="4997a-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4997a-135">-FrontendPort</span></span>
<span data-ttu-id="4997a-136">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4997a-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4997a-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4997a-138">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="4997a-139">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="4997a-139">-LoadBalancer</span></span>
<span data-ttu-id="4997a-140">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-140">Specifies a load balancer.</span></span>
<span data-ttu-id="4997a-141">Этот командлет задает конфигурацию правила состояния цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4997a-141">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4997a-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="4997a-142">-LoadDistribution</span></span>
<span data-ttu-id="4997a-143">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-143">Specifies a load distribution.</span></span>
<span data-ttu-id="4997a-144">Допустимые значения этого параметра: SourceIP и SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="4997a-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="4997a-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4997a-145">-Name</span></span>
<span data-ttu-id="4997a-146">Указывает имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="4997a-147">-Зонд</span><span class="sxs-lookup"><span data-stu-id="4997a-147">-Probe</span></span>
<span data-ttu-id="4997a-148">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4997a-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="4997a-149">-ProbeId</span></span>
<span data-ttu-id="4997a-150">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="4997a-151">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="4997a-151">-Protocol</span></span>
<span data-ttu-id="4997a-152">Указывает протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4997a-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="4997a-153">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="4997a-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="4997a-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4997a-154">-Confirm</span></span>
<span data-ttu-id="4997a-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4997a-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4997a-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4997a-156">-WhatIf</span></span>
<span data-ttu-id="4997a-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4997a-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4997a-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4997a-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4997a-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4997a-159">CommonParameters</span></span>
<span data-ttu-id="4997a-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4997a-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4997a-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4997a-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4997a-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4997a-162">INPUTS</span></span>

### <span data-ttu-id="4997a-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4997a-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4997a-164">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4997a-164">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="4997a-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4997a-165">OUTPUTS</span></span>

### <span data-ttu-id="4997a-166">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4997a-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4997a-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="4997a-167">NOTES</span></span>

## <span data-ttu-id="4997a-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4997a-168">RELATED LINKS</span></span>

[<span data-ttu-id="4997a-169">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4997a-169">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="4997a-170">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4997a-170">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="4997a-171">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4997a-171">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="4997a-172">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4997a-172">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="4997a-173">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4997a-173">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


