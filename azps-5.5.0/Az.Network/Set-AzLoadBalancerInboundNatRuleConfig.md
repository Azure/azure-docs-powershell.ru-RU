---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218260"
---
# <span data-ttu-id="a5680-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5680-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a5680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5680-102">SYNOPSIS</span></span>
<span data-ttu-id="a5680-103">Настраивает правила NAT для входящие остаток на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a5680-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a5680-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5680-104">SYNTAX</span></span>

### <span data-ttu-id="a5680-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5680-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5680-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5680-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5680-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5680-107">DESCRIPTION</span></span>
<span data-ttu-id="a5680-108">Cmdlet **Set-AzLoadBalancerInboundNatRuleConfig** задает конфигурацию правила перевода сетевых адресов (NAT) для балансиров нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a5680-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a5680-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5680-109">EXAMPLES</span></span>

### <span data-ttu-id="a5680-110">Пример 1. Изменение конфигурации входящие правила NAT для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="a5680-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="a5680-111">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="a5680-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a5680-112">Вторая команда передает балансиру нагрузки в $slb add-AzLoadBalancerInboundNatRuleConfig, который добавляет в него конфигурацию правила NAT для входящие проектов.</span><span class="sxs-lookup"><span data-stu-id="a5680-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="a5680-113">Третья команда передает балансиру нагрузки в **set-AzLoadBalancerInboundNatRuleConfig,** который сохраняет и обновляет конфигурацию входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="a5680-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="a5680-114">Обратите внимание, что конфигурация правила была настроена без включения плавающего IP-адреса, который был включен предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="a5680-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="a5680-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5680-115">PARAMETERS</span></span>

### <span data-ttu-id="a5680-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a5680-116">-BackendPort</span></span>
<span data-ttu-id="a5680-117">Определяет порт для трафика, на который совме задана конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="a5680-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="a5680-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5680-118">-DefaultProfile</span></span>
<span data-ttu-id="a5680-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5680-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5680-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a5680-120">-EnableFloatingIP</span></span>
<span data-ttu-id="a5680-121">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="a5680-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a5680-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a5680-122">-EnableTcpReset</span></span>
<span data-ttu-id="a5680-123">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="a5680-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a5680-124">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="a5680-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a5680-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5680-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a5680-126">Список IP-адресов, которые нужно связать с конфигурацией правила NAT входящие.</span><span class="sxs-lookup"><span data-stu-id="a5680-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a5680-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a5680-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a5680-128">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a5680-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a5680-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a5680-129">-FrontendPort</span></span>
<span data-ttu-id="a5680-130">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a5680-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a5680-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a5680-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a5680-132">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a5680-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a5680-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5680-133">-LoadBalancer</span></span>
<span data-ttu-id="a5680-134">Определяет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a5680-134">Specifies a load balancer.</span></span>
<span data-ttu-id="a5680-135">Этот cmdlet задает конфигурацию входящие правила NAT для балансироса нагрузки, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a5680-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a5680-136">-Name</span><span class="sxs-lookup"><span data-stu-id="a5680-136">-Name</span></span>
<span data-ttu-id="a5680-137">Указывает имя конфигурации входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="a5680-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a5680-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a5680-138">-Protocol</span></span>
<span data-ttu-id="a5680-139">Определяет протокол, который соответствует конфигурации входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="a5680-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="a5680-140">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="a5680-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a5680-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5680-141">-Confirm</span></span>
<span data-ttu-id="a5680-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a5680-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5680-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5680-143">-WhatIf</span></span>
<span data-ttu-id="a5680-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5680-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5680-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5680-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5680-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5680-146">CommonParameters</span></span>
<span data-ttu-id="a5680-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5680-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5680-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5680-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5680-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5680-149">INPUTS</span></span>

### <span data-ttu-id="a5680-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5680-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a5680-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a5680-151">System.String</span></span>

### <span data-ttu-id="a5680-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a5680-152">System.Int32</span></span>

### <span data-ttu-id="a5680-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5680-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a5680-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5680-154">OUTPUTS</span></span>

### <span data-ttu-id="a5680-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5680-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a5680-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5680-156">NOTES</span></span>

## <span data-ttu-id="a5680-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5680-157">RELATED LINKS</span></span>

[<span data-ttu-id="a5680-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5680-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a5680-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a5680-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a5680-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5680-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a5680-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5680-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a5680-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a5680-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


