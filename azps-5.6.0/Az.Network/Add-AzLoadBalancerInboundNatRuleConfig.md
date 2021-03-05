---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006504"
---
# <span data-ttu-id="34333-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34333-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="34333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34333-102">SYNOPSIS</span></span>
<span data-ttu-id="34333-103">Добавляет конфигурацию правила NAT для входящие в балансилет нагрузки.</span><span class="sxs-lookup"><span data-stu-id="34333-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="34333-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34333-104">SYNTAX</span></span>

### <span data-ttu-id="34333-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34333-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34333-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="34333-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34333-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34333-107">DESCRIPTION</span></span>
<span data-ttu-id="34333-108">Для балансиента нагрузки Azure к балансору нагрузки Azure добавляется конфигурация правила перевода сетевых адресов (NAT) **Add-AzLoadBalancerInboundNatRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="34333-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="34333-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34333-109">EXAMPLES</span></span>

### <span data-ttu-id="34333-110">Пример 1. Добавление входящий конфигурации правила NAT для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="34333-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="34333-111">Первая команда получает балансировку нагрузки с именем MyloadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="34333-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="34333-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb **add-AzLoadBalancerInboundNatRuleConfig,** который добавляет конфигурацию правила NAT для входящие в баланс.</span><span class="sxs-lookup"><span data-stu-id="34333-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="34333-113">Последняя команда задает для конфигурации балансировую нагрузку, если не выполнить командную команду Set-AzLoadBalancer, изменения не будут применены к загрузчику.</span><span class="sxs-lookup"><span data-stu-id="34333-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="34333-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34333-114">PARAMETERS</span></span>

### <span data-ttu-id="34333-115">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="34333-115">-BackendPort</span></span>
<span data-ttu-id="34333-116">Указывает порт для трафика, который соответствует конфигурации правил.</span><span class="sxs-lookup"><span data-stu-id="34333-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="34333-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34333-117">-DefaultProfile</span></span>
<span data-ttu-id="34333-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34333-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34333-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="34333-119">-EnableFloatingIP</span></span>
<span data-ttu-id="34333-120">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="34333-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="34333-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="34333-121">-EnableTcpReset</span></span>
<span data-ttu-id="34333-122">Получите раздвивный TCP-сброс при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="34333-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="34333-123">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="34333-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="34333-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="34333-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="34333-125">Список IP-адресов, которые нужно связать с конфигурацией правила NAT входящие.</span><span class="sxs-lookup"><span data-stu-id="34333-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="34333-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="34333-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="34333-127">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="34333-127">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="34333-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="34333-128">-FrontendPort</span></span>
<span data-ttu-id="34333-129">Указывает порт переднего адреса, который соответствует конфигурации правил.</span><span class="sxs-lookup"><span data-stu-id="34333-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="34333-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="34333-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="34333-131">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="34333-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="34333-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34333-132">-LoadBalancer</span></span>
<span data-ttu-id="34333-133">Определяет объект **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="34333-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="34333-134">Этот cmdlet добавляет конфигурацию входящие правила NAT к балансе нагрузки, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="34333-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="34333-135">-Name</span><span class="sxs-lookup"><span data-stu-id="34333-135">-Name</span></span>
<span data-ttu-id="34333-136">Указывает имя добавляемой конфигурации правила NAT.</span><span class="sxs-lookup"><span data-stu-id="34333-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="34333-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="34333-137">-Protocol</span></span>
<span data-ttu-id="34333-138">Определяет протокол, который соответствует правилу NAT для входящий сообщений.</span><span class="sxs-lookup"><span data-stu-id="34333-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="34333-139">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="34333-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="34333-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34333-140">-Confirm</span></span>
<span data-ttu-id="34333-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34333-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34333-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34333-142">-WhatIf</span></span>
<span data-ttu-id="34333-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34333-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34333-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34333-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34333-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34333-145">CommonParameters</span></span>
<span data-ttu-id="34333-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34333-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34333-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34333-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34333-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34333-148">INPUTS</span></span>

### <span data-ttu-id="34333-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34333-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="34333-150">System.String</span><span class="sxs-lookup"><span data-stu-id="34333-150">System.String</span></span>

### <span data-ttu-id="34333-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="34333-151">System.Int32</span></span>

### <span data-ttu-id="34333-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="34333-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="34333-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34333-153">OUTPUTS</span></span>

### <span data-ttu-id="34333-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34333-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="34333-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34333-155">NOTES</span></span>

## <span data-ttu-id="34333-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34333-156">RELATED LINKS</span></span>

[<span data-ttu-id="34333-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34333-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="34333-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34333-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34333-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34333-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34333-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34333-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="34333-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="34333-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="34333-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34333-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


