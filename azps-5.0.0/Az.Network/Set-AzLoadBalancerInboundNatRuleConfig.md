---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247590"
---
# <span data-ttu-id="d8982-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8982-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d8982-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8982-102">SYNOPSIS</span></span>
<span data-ttu-id="d8982-103">Задает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d8982-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="d8982-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8982-104">SYNTAX</span></span>

### <span data-ttu-id="d8982-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8982-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8982-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8982-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8982-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8982-107">DESCRIPTION</span></span>
<span data-ttu-id="d8982-108">Командлет **Set-AzLoadBalancerInboundNatRuleConfig** устанавливает конфигурацию правила трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="d8982-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d8982-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8982-109">EXAMPLES</span></span>

### <span data-ttu-id="d8982-110">Пример 1: изменение конфигурации правила входящего NAT для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="d8982-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="d8982-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="d8982-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="d8982-112">Вторая команда использует оператор Pipeline для передачи подсистемы балансировки нагрузки в $slb на Add-AzLoadBalancerInboundNatRuleConfig, который добавляет в него конфигурацию правила входящей сети NAT.</span><span class="sxs-lookup"><span data-stu-id="d8982-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="d8982-113">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancerInboundNatRuleConfig** , которая сохраняет и обновляет конфигурацию правила входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="d8982-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="d8982-114">Обратите внимание, что конфигурация правила задана без включения плавающего IP-адреса, которая была включена предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="d8982-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="d8982-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8982-115">PARAMETERS</span></span>

### <span data-ttu-id="d8982-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d8982-116">-BackendPort</span></span>
<span data-ttu-id="d8982-117">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="d8982-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="d8982-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8982-118">-DefaultProfile</span></span>
<span data-ttu-id="d8982-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8982-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8982-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d8982-120">-EnableFloatingIP</span></span>
<span data-ttu-id="d8982-121">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="d8982-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d8982-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d8982-122">-EnableTcpReset</span></span>
<span data-ttu-id="d8982-123">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="d8982-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d8982-124">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="d8982-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d8982-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8982-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d8982-126">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="d8982-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d8982-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d8982-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d8982-128">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="d8982-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d8982-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d8982-129">-FrontendPort</span></span>
<span data-ttu-id="d8982-130">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d8982-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="d8982-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d8982-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d8982-132">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d8982-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d8982-133">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="d8982-133">-LoadBalancer</span></span>
<span data-ttu-id="d8982-134">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d8982-134">Specifies a load balancer.</span></span>
<span data-ttu-id="d8982-135">Этот командлет задает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d8982-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8982-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8982-136">-Name</span></span>
<span data-ttu-id="d8982-137">Указывает имя конфигурации правила входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="d8982-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d8982-138">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="d8982-138">-Protocol</span></span>
<span data-ttu-id="d8982-139">Указывает протокол, совпадающий с конфигурацией правила входящей NAT.</span><span class="sxs-lookup"><span data-stu-id="d8982-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="d8982-140">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="d8982-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d8982-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8982-141">-Confirm</span></span>
<span data-ttu-id="d8982-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8982-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8982-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8982-143">-WhatIf</span></span>
<span data-ttu-id="d8982-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8982-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8982-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8982-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8982-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8982-146">CommonParameters</span></span>
<span data-ttu-id="d8982-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8982-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8982-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8982-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8982-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8982-149">INPUTS</span></span>

### <span data-ttu-id="d8982-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8982-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d8982-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d8982-151">System.String</span></span>

### <span data-ttu-id="d8982-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d8982-152">System.Int32</span></span>

### <span data-ttu-id="d8982-153">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8982-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d8982-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8982-154">OUTPUTS</span></span>

### <span data-ttu-id="d8982-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8982-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d8982-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8982-156">NOTES</span></span>

## <span data-ttu-id="d8982-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8982-157">RELATED LINKS</span></span>

[<span data-ttu-id="d8982-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8982-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d8982-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8982-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d8982-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8982-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d8982-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8982-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d8982-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d8982-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

