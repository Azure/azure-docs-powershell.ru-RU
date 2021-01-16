---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413972"
---
# <span data-ttu-id="d3c0d-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c0d-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d3c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c0d-103">Добавляет конфигурацию правила NAT для входящие в балансилет нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="d3c0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3c0d-104">SYNTAX</span></span>

### <span data-ttu-id="d3c0d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3c0d-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c0d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3c0d-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c0d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3c0d-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c0d-108">Для балансиента нагрузки Azure к балансору нагрузки Azure добавляется конфигурация правила перевода сетевых адресов (NAT) **Add-AzLoadBalancerInboundNatRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="d3c0d-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d3c0d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3c0d-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c0d-110">Пример 1. Добавление входящий конфигурации правила NAT для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="d3c0d-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="d3c0d-111">Первая команда получает балансировку нагрузки с именем MyloadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d3c0d-112">Вторая команда использует оператор конвейера для передать балансиру нагрузки в $slb **add-AzLoadBalancerInboundNatRuleConfig,** который добавляет конфигурацию правила NAT для входящие в баланс.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="d3c0d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3c0d-113">PARAMETERS</span></span>

### <span data-ttu-id="d3c0d-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d3c0d-114">-BackendPort</span></span>
<span data-ttu-id="d3c0d-115">Указывает порт для трафика, который соответствует конфигурации правил.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d3c0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c0d-116">-DefaultProfile</span></span>
<span data-ttu-id="d3c0d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3c0d-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d3c0d-118">-EnableFloatingIP</span></span>
<span data-ttu-id="d3c0d-119">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d3c0d-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d3c0d-120">-EnableTcpReset</span></span>
<span data-ttu-id="d3c0d-121">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d3c0d-122">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d3c0d-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3c0d-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d3c0d-124">Список IP-адресов, которые нужно связать с конфигурацией правила NAT входящие.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d3c0d-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d3c0d-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d3c0d-126">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d3c0d-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d3c0d-127">-FrontendPort</span></span>
<span data-ttu-id="d3c0d-128">Указывает порт переднего адреса, который соответствует конфигурации правил.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d3c0d-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3c0d-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d3c0d-130">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d3c0d-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c0d-131">-LoadBalancer</span></span>
<span data-ttu-id="d3c0d-132">Определяет объект **LoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="d3c0d-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d3c0d-133">Этот cmdlet добавляет конфигурацию входящие правила NAT к балансе нагрузки, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3c0d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d3c0d-134">-Name</span></span>
<span data-ttu-id="d3c0d-135">Указывает имя добавляемой конфигурации правила NAT для входящий сообщений.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="d3c0d-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d3c0d-136">-Protocol</span></span>
<span data-ttu-id="d3c0d-137">Определяет протокол, который соответствует правилу NAT для входящий сообщений.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="d3c0d-138">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d3c0d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3c0d-139">-Confirm</span></span>
<span data-ttu-id="d3c0d-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c0d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c0d-141">-WhatIf</span></span>
<span data-ttu-id="d3c0d-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3c0d-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c0d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c0d-144">CommonParameters</span></span>
<span data-ttu-id="d3c0d-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c0d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c0d-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c0d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c0d-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3c0d-147">INPUTS</span></span>

### <span data-ttu-id="d3c0d-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c0d-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d3c0d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d3c0d-149">System.String</span></span>

### <span data-ttu-id="d3c0d-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d3c0d-150">System.Int32</span></span>

### <span data-ttu-id="d3c0d-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3c0d-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d3c0d-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3c0d-152">OUTPUTS</span></span>

### <span data-ttu-id="d3c0d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c0d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d3c0d-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3c0d-154">NOTES</span></span>

## <span data-ttu-id="d3c0d-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3c0d-155">RELATED LINKS</span></span>

[<span data-ttu-id="d3c0d-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c0d-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d3c0d-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c0d-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d3c0d-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c0d-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d3c0d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c0d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d3c0d-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3c0d-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="d3c0d-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d3c0d-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


