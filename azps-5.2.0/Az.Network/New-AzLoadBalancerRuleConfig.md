---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413276"
---
# <span data-ttu-id="268e6-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="268e6-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="268e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268e6-102">SYNOPSIS</span></span>
<span data-ttu-id="268e6-103">Создает конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="268e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="268e6-104">SYNTAX</span></span>

### <span data-ttu-id="268e6-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="268e6-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="268e6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="268e6-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="268e6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="268e6-107">DESCRIPTION</span></span>
<span data-ttu-id="268e6-108">Для балансиров нагрузки Azure создается конфигурация правил для **new-AzLoadBalancerRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="268e6-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="268e6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="268e6-109">EXAMPLES</span></span>

### <span data-ttu-id="268e6-110">Пример 1. Создание конфигурации правил для azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="268e6-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="268e6-111">Первые три команды настроили общедоступный IP-адрес, передний и другие команды для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="268e6-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="268e6-112">С помощью этой команды создается новое правило "МойLBrule" с определенными спецификациями.</span><span class="sxs-lookup"><span data-stu-id="268e6-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="268e6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="268e6-113">PARAMETERS</span></span>

### <span data-ttu-id="268e6-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="268e6-114">-BackendAddressPool</span></span>
<span data-ttu-id="268e6-115">Объект **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="268e6-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="268e6-117">Определяет ID объекта **BackendAddressPool,** который нужно связать с конфигурацией правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="268e6-118">-BackendPort</span></span>
<span data-ttu-id="268e6-119">Определяет порт для трафика, который соответствует конфигурации этого правила балансировации нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268e6-120">-DefaultProfile</span></span>
<span data-ttu-id="268e6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="268e6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268e6-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="268e6-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="268e6-123">Настраивает SNAT для VMs в пуле backend, чтобы использовать общедоступный IP-адрес, указанный на переднем панели правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="268e6-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="268e6-124">-EnableFloatingIP</span></span>
<span data-ttu-id="268e6-125">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="268e6-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="268e6-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="268e6-126">-EnableTcpReset</span></span>
<span data-ttu-id="268e6-127">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="268e6-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="268e6-128">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="268e6-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="268e6-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="268e6-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="268e6-130">Список IP-адресов, которые нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="268e6-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="268e6-132">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="268e6-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="268e6-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="268e6-133">-FrontendPort</span></span>
<span data-ttu-id="268e6-134">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="268e6-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="268e6-136">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="268e6-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="268e6-137">-LoadDistribution</span></span>
<span data-ttu-id="268e6-138">Определяет распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-138">Specifies a load distribution.</span></span>
<span data-ttu-id="268e6-139">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="268e6-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="268e6-140">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="268e6-140">Default</span></span>
- <span data-ttu-id="268e6-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="268e6-141">SourceIP</span></span>
- <span data-ttu-id="268e6-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="268e6-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="268e6-143">-Name</span><span class="sxs-lookup"><span data-stu-id="268e6-143">-Name</span></span>
<span data-ttu-id="268e6-144">Указывает имя правила балансировки нагрузки, которое создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="268e6-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="268e6-145">-Разротные</span><span class="sxs-lookup"><span data-stu-id="268e6-145">-Probe</span></span>
<span data-ttu-id="268e6-146">Указывает, к каковую измеримую конфигурацию правил балансиров нагрузки можно связать.</span><span class="sxs-lookup"><span data-stu-id="268e6-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-147">-Вадим-ИД</span><span class="sxs-lookup"><span data-stu-id="268e6-147">-ProbeId</span></span>
<span data-ttu-id="268e6-148">Определяет, как будет связываться этот документ с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="268e6-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="268e6-149">-Protocol</span></span>
<span data-ttu-id="268e6-150">Протокол, который соответствует конфигурации правила балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="268e6-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="268e6-151">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="268e6-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="268e6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="268e6-152">-Confirm</span></span>
<span data-ttu-id="268e6-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="268e6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="268e6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="268e6-154">-WhatIf</span></span>
<span data-ttu-id="268e6-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="268e6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="268e6-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="268e6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="268e6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268e6-157">CommonParameters</span></span>
<span data-ttu-id="268e6-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268e6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268e6-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268e6-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268e6-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="268e6-160">INPUTS</span></span>

### <span data-ttu-id="268e6-161">System.String</span><span class="sxs-lookup"><span data-stu-id="268e6-161">System.String</span></span>

### <span data-ttu-id="268e6-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="268e6-162">System.Int32</span></span>

### <span data-ttu-id="268e6-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="268e6-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="268e6-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="268e6-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="268e6-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="268e6-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="268e6-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="268e6-166">OUTPUTS</span></span>

### <span data-ttu-id="268e6-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="268e6-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="268e6-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="268e6-168">NOTES</span></span>

## <span data-ttu-id="268e6-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="268e6-169">RELATED LINKS</span></span>

[<span data-ttu-id="268e6-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="268e6-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="268e6-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="268e6-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="268e6-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="268e6-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="268e6-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="268e6-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


