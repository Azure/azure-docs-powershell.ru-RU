---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507869"
---
# <span data-ttu-id="0ea84-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ea84-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0ea84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ea84-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea84-103">Создает конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0ea84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ea84-104">SYNTAX</span></span>

### <span data-ttu-id="0ea84-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ea84-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ea84-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ea84-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea84-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ea84-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea84-108">Для балансиров нагрузки Azure создается конфигурация правил **для new-AzLoadBalancerRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="0ea84-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0ea84-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ea84-109">EXAMPLES</span></span>

### <span data-ttu-id="0ea84-110">Пример 1. Создание конфигурации правил для azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="0ea84-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="0ea84-111">Первые три команды настроили общедоступный IP-адрес, передний и другие команды для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="0ea84-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="0ea84-112">С помощью этой команды создается новое правило myLBrule с определенными спецификациями.</span><span class="sxs-lookup"><span data-stu-id="0ea84-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="0ea84-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ea84-113">PARAMETERS</span></span>

### <span data-ttu-id="0ea84-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0ea84-114">-BackendAddressPool</span></span>
<span data-ttu-id="0ea84-115">Объект **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0ea84-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="0ea84-117">Определяет ID объекта **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0ea84-118">-BackendPort</span></span>
<span data-ttu-id="0ea84-119">Определяет порт для трафика, который соответствует конфигурации этого правила балансировации нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea84-120">-DefaultProfile</span></span>
<span data-ttu-id="0ea84-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea84-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ea84-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="0ea84-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="0ea84-123">Настраивает SNAT для VMs в пуле backend, чтобы использовать общедоступный АДРЕСIP, указанный на переднем панели правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="0ea84-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0ea84-124">-EnableFloatingIP</span></span>
<span data-ttu-id="0ea84-125">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="0ea84-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0ea84-126">-EnableTcpReset</span></span>
<span data-ttu-id="0ea84-127">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="0ea84-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0ea84-128">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="0ea84-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0ea84-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ea84-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0ea84-130">Список IP-адресов, которые нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0ea84-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0ea84-132">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="0ea84-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0ea84-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0ea84-133">-FrontendPort</span></span>
<span data-ttu-id="0ea84-134">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0ea84-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0ea84-136">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="0ea84-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="0ea84-137">-LoadDistribution</span></span>
<span data-ttu-id="0ea84-138">Определяет распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-138">Specifies a load distribution.</span></span>
<span data-ttu-id="0ea84-139">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="0ea84-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ea84-140">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="0ea84-140">Default</span></span>
- <span data-ttu-id="0ea84-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="0ea84-141">SourceIP</span></span>
- <span data-ttu-id="0ea84-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="0ea84-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="0ea84-143">-Name</span><span class="sxs-lookup"><span data-stu-id="0ea84-143">-Name</span></span>
<span data-ttu-id="0ea84-144">Указывает имя правила балансировки нагрузки, которое создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ea84-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0ea84-145">-Разротные</span><span class="sxs-lookup"><span data-stu-id="0ea84-145">-Probe</span></span>
<span data-ttu-id="0ea84-146">Указывает, к каковую измеримую настройку правил балансиров нагрузки можно связать.</span><span class="sxs-lookup"><span data-stu-id="0ea84-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-147">-Тем нее</span><span class="sxs-lookup"><span data-stu-id="0ea84-147">-ProbeId</span></span>
<span data-ttu-id="0ea84-148">Определяет, как будет связываться этот документ с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0ea84-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0ea84-149">-Protocol</span></span>
<span data-ttu-id="0ea84-150">Протокол, который соответствует конфигурации правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0ea84-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="0ea84-151">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="0ea84-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="0ea84-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ea84-152">-Confirm</span></span>
<span data-ttu-id="0ea84-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0ea84-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea84-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea84-154">-WhatIf</span></span>
<span data-ttu-id="0ea84-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ea84-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ea84-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ea84-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea84-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea84-157">CommonParameters</span></span>
<span data-ttu-id="0ea84-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea84-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea84-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea84-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea84-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ea84-160">INPUTS</span></span>

### <span data-ttu-id="0ea84-161">System.String</span><span class="sxs-lookup"><span data-stu-id="0ea84-161">System.String</span></span>

### <span data-ttu-id="0ea84-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0ea84-162">System.Int32</span></span>

### <span data-ttu-id="0ea84-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ea84-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="0ea84-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0ea84-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="0ea84-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="0ea84-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="0ea84-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ea84-166">OUTPUTS</span></span>

### <span data-ttu-id="0ea84-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="0ea84-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="0ea84-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ea84-168">NOTES</span></span>

## <span data-ttu-id="0ea84-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ea84-169">RELATED LINKS</span></span>

[<span data-ttu-id="0ea84-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ea84-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ea84-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ea84-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ea84-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ea84-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="0ea84-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0ea84-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


