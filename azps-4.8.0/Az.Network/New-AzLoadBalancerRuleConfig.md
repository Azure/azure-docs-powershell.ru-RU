---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236034"
---
# <span data-ttu-id="caa8c-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="caa8c-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="caa8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="caa8c-102">SYNOPSIS</span></span>
<span data-ttu-id="caa8c-103">Создание конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="caa8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="caa8c-104">SYNTAX</span></span>

### <span data-ttu-id="caa8c-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="caa8c-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caa8c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="caa8c-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caa8c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caa8c-107">DESCRIPTION</span></span>
<span data-ttu-id="caa8c-108">Командлет **New-AzLoadBalancerRuleConfig** создает конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="caa8c-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="caa8c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="caa8c-109">EXAMPLES</span></span>

### <span data-ttu-id="caa8c-110">Пример 1: создание конфигурации правила для подсистемы балансировки нагрузки Azure</span><span class="sxs-lookup"><span data-stu-id="caa8c-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="caa8c-111">Первые три команды настроили общедоступный IP-адрес, интерфейсный сервер и пробную конфигурацию для конфигурации правила в команде "вперед".</span><span class="sxs-lookup"><span data-stu-id="caa8c-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="caa8c-112">Для создания нового правила с именем MyLBrule с определенными характеристиками.</span><span class="sxs-lookup"><span data-stu-id="caa8c-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="caa8c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="caa8c-113">PARAMETERS</span></span>

### <span data-ttu-id="caa8c-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="caa8c-114">-BackendAddressPool</span></span>
<span data-ttu-id="caa8c-115">Указывает объект **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="caa8c-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="caa8c-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="caa8c-118">-BackendPort</span></span>
<span data-ttu-id="caa8c-119">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa8c-120">-DefaultProfile</span></span>
<span data-ttu-id="caa8c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caa8c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caa8c-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="caa8c-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="caa8c-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="caa8c-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="caa8c-124">-EnableFloatingIP</span></span>
<span data-ttu-id="caa8c-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="caa8c-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="caa8c-126">-EnableTcpReset</span></span>
<span data-ttu-id="caa8c-127">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="caa8c-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="caa8c-128">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="caa8c-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="caa8c-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="caa8c-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="caa8c-130">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="caa8c-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="caa8c-132">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="caa8c-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="caa8c-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="caa8c-133">-FrontendPort</span></span>
<span data-ttu-id="caa8c-134">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="caa8c-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="caa8c-136">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="caa8c-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="caa8c-137">-LoadDistribution</span></span>
<span data-ttu-id="caa8c-138">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-138">Specifies a load distribution.</span></span>
<span data-ttu-id="caa8c-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="caa8c-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="caa8c-140">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="caa8c-140">Default</span></span>
- <span data-ttu-id="caa8c-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="caa8c-141">SourceIP</span></span>
- <span data-ttu-id="caa8c-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="caa8c-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="caa8c-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="caa8c-143">-Name</span></span>
<span data-ttu-id="caa8c-144">Указывает имя правила балансировки нагрузки, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="caa8c-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="caa8c-145">-Зонд</span><span class="sxs-lookup"><span data-stu-id="caa8c-145">-Probe</span></span>
<span data-ttu-id="caa8c-146">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="caa8c-147">-ProbeId</span></span>
<span data-ttu-id="caa8c-148">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="caa8c-149">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="caa8c-149">-Protocol</span></span>
<span data-ttu-id="caa8c-150">Указывает протокол, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="caa8c-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="caa8c-151">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="caa8c-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="caa8c-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caa8c-152">-Confirm</span></span>
<span data-ttu-id="caa8c-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="caa8c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa8c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa8c-154">-WhatIf</span></span>
<span data-ttu-id="caa8c-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="caa8c-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="caa8c-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="caa8c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa8c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa8c-157">CommonParameters</span></span>
<span data-ttu-id="caa8c-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="caa8c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa8c-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa8c-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa8c-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="caa8c-160">INPUTS</span></span>

### <span data-ttu-id="caa8c-161">System. String</span><span class="sxs-lookup"><span data-stu-id="caa8c-161">System.String</span></span>

### <span data-ttu-id="caa8c-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="caa8c-162">System.Int32</span></span>

### <span data-ttu-id="caa8c-163">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="caa8c-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="caa8c-164">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="caa8c-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="caa8c-165">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="caa8c-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="caa8c-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="caa8c-166">OUTPUTS</span></span>

### <span data-ttu-id="caa8c-167">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="caa8c-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="caa8c-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="caa8c-168">NOTES</span></span>

## <span data-ttu-id="caa8c-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caa8c-169">RELATED LINKS</span></span>

[<span data-ttu-id="caa8c-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="caa8c-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="caa8c-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="caa8c-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="caa8c-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="caa8c-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="caa8c-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="caa8c-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


