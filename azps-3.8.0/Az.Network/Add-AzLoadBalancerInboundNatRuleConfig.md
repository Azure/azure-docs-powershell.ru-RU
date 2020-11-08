---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065502"
---
# <span data-ttu-id="222cb-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="222cb-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="222cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="222cb-102">SYNOPSIS</span></span>
<span data-ttu-id="222cb-103">Добавляет конфигурацию правила NAT для входящего трафика в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="222cb-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="222cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="222cb-104">SYNTAX</span></span>

### <span data-ttu-id="222cb-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="222cb-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="222cb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="222cb-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="222cb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="222cb-107">DESCRIPTION</span></span>
<span data-ttu-id="222cb-108">Командлет **Add-AzLoadBalancerInboundNatRuleConfig** добавляет конфигурацию правила трансляции сетевых адресов (NAT) в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="222cb-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="222cb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="222cb-109">EXAMPLES</span></span>

### <span data-ttu-id="222cb-110">Пример 1: Добавление конфигурации правила входящего NAT в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="222cb-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="222cb-111">Первая команда получает подсистему балансировки нагрузки с именем MyloadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="222cb-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="222cb-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzLoadBalancerInboundNatRuleConfig** , который добавляет конфигурацию правила входящего NAT в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="222cb-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="222cb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="222cb-113">PARAMETERS</span></span>

### <span data-ttu-id="222cb-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="222cb-114">-BackendPort</span></span>
<span data-ttu-id="222cb-115">Указывает внутренний порт для трафика, соответствующего конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="222cb-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="222cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222cb-116">-DefaultProfile</span></span>
<span data-ttu-id="222cb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="222cb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="222cb-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="222cb-118">-EnableFloatingIP</span></span>
<span data-ttu-id="222cb-119">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="222cb-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="222cb-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="222cb-120">-EnableTcpReset</span></span>
<span data-ttu-id="222cb-121">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="222cb-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="222cb-122">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="222cb-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="222cb-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="222cb-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="222cb-124">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="222cb-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="222cb-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="222cb-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="222cb-126">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="222cb-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="222cb-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="222cb-127">-FrontendPort</span></span>
<span data-ttu-id="222cb-128">Указывает порт переднего плана, совпадающий с конфигурацией правила.</span><span class="sxs-lookup"><span data-stu-id="222cb-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="222cb-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="222cb-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="222cb-130">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="222cb-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="222cb-131">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="222cb-131">-LoadBalancer</span></span>
<span data-ttu-id="222cb-132">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="222cb-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="222cb-133">Этот командлет добавляет конфигурацию правила входящего трафика NAT в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="222cb-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="222cb-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="222cb-134">-Name</span></span>
<span data-ttu-id="222cb-135">Указывает имя конфигурации правила входящего NAT для добавления.</span><span class="sxs-lookup"><span data-stu-id="222cb-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="222cb-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="222cb-136">-Protocol</span></span>
<span data-ttu-id="222cb-137">Указывает протокол, совпадающий с правилом входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="222cb-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="222cb-138">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="222cb-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="222cb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="222cb-139">-Confirm</span></span>
<span data-ttu-id="222cb-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="222cb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="222cb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="222cb-141">-WhatIf</span></span>
<span data-ttu-id="222cb-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="222cb-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="222cb-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="222cb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="222cb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222cb-144">CommonParameters</span></span>
<span data-ttu-id="222cb-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="222cb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222cb-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="222cb-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222cb-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="222cb-147">INPUTS</span></span>

### <span data-ttu-id="222cb-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="222cb-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="222cb-149">System. String</span><span class="sxs-lookup"><span data-stu-id="222cb-149">System.String</span></span>

### <span data-ttu-id="222cb-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="222cb-150">System.Int32</span></span>

### <span data-ttu-id="222cb-151">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="222cb-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="222cb-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="222cb-152">OUTPUTS</span></span>

### <span data-ttu-id="222cb-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="222cb-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="222cb-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="222cb-154">NOTES</span></span>

## <span data-ttu-id="222cb-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="222cb-155">RELATED LINKS</span></span>

[<span data-ttu-id="222cb-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="222cb-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="222cb-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="222cb-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="222cb-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="222cb-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="222cb-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="222cb-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="222cb-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="222cb-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="222cb-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="222cb-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


