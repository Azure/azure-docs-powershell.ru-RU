---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236080"
---
# <span data-ttu-id="f583d-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f583d-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f583d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f583d-102">SYNOPSIS</span></span>
<span data-ttu-id="f583d-103">Добавляет конфигурацию правила NAT для входящего трафика в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f583d-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="f583d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f583d-104">SYNTAX</span></span>

### <span data-ttu-id="f583d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f583d-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f583d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f583d-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f583d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f583d-107">DESCRIPTION</span></span>
<span data-ttu-id="f583d-108">Командлет **Add-AzLoadBalancerInboundNatRuleConfig** добавляет конфигурацию правила трансляции сетевых адресов (NAT) в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="f583d-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="f583d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f583d-109">EXAMPLES</span></span>

### <span data-ttu-id="f583d-110">Пример 1: Добавление конфигурации правила входящего NAT в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="f583d-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="f583d-111">Первая команда получает подсистему балансировки нагрузки с именем MyloadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="f583d-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="f583d-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzLoadBalancerInboundNatRuleConfig** , который добавляет конфигурацию правила входящего NAT в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f583d-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="f583d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f583d-113">PARAMETERS</span></span>

### <span data-ttu-id="f583d-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f583d-114">-BackendPort</span></span>
<span data-ttu-id="f583d-115">Указывает внутренний порт для трафика, соответствующего конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f583d-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="f583d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f583d-116">-DefaultProfile</span></span>
<span data-ttu-id="f583d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f583d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f583d-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f583d-118">-EnableFloatingIP</span></span>
<span data-ttu-id="f583d-119">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f583d-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f583d-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f583d-120">-EnableTcpReset</span></span>
<span data-ttu-id="f583d-121">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="f583d-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f583d-122">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="f583d-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f583d-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f583d-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f583d-124">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="f583d-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f583d-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f583d-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f583d-126">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f583d-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f583d-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f583d-127">-FrontendPort</span></span>
<span data-ttu-id="f583d-128">Указывает порт переднего плана, совпадающий с конфигурацией правила.</span><span class="sxs-lookup"><span data-stu-id="f583d-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="f583d-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f583d-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f583d-130">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f583d-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f583d-131">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="f583d-131">-LoadBalancer</span></span>
<span data-ttu-id="f583d-132">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="f583d-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="f583d-133">Этот командлет добавляет конфигурацию правила входящего трафика NAT в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="f583d-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f583d-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f583d-134">-Name</span></span>
<span data-ttu-id="f583d-135">Указывает имя конфигурации правила входящего NAT для добавления.</span><span class="sxs-lookup"><span data-stu-id="f583d-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="f583d-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f583d-136">-Protocol</span></span>
<span data-ttu-id="f583d-137">Указывает протокол, совпадающий с правилом входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="f583d-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="f583d-138">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="f583d-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f583d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f583d-139">-Confirm</span></span>
<span data-ttu-id="f583d-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f583d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f583d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f583d-141">-WhatIf</span></span>
<span data-ttu-id="f583d-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f583d-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f583d-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f583d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f583d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f583d-144">CommonParameters</span></span>
<span data-ttu-id="f583d-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f583d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f583d-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f583d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f583d-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f583d-147">INPUTS</span></span>

### <span data-ttu-id="f583d-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f583d-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="f583d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f583d-149">System.String</span></span>

### <span data-ttu-id="f583d-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f583d-150">System.Int32</span></span>

### <span data-ttu-id="f583d-151">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f583d-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="f583d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f583d-152">OUTPUTS</span></span>

### <span data-ttu-id="f583d-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f583d-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f583d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="f583d-154">NOTES</span></span>

## <span data-ttu-id="f583d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f583d-155">RELATED LINKS</span></span>

[<span data-ttu-id="f583d-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f583d-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f583d-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f583d-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f583d-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f583d-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f583d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f583d-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f583d-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f583d-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="f583d-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f583d-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


