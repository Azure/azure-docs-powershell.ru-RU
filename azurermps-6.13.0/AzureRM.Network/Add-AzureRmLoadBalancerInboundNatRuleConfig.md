---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 402235f4d98b39ec78ffdc67bd0a01ab16e0400a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560111"
---
# <span data-ttu-id="89477-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89477-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="89477-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89477-102">SYNOPSIS</span></span>
<span data-ttu-id="89477-103">Добавляет конфигурацию правила NAT для входящего трафика в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="89477-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89477-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89477-104">SYNTAX</span></span>

### <span data-ttu-id="89477-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89477-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89477-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="89477-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89477-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89477-107">DESCRIPTION</span></span>
<span data-ttu-id="89477-108">Командлет **Add-AzureRmLoadBalancerInboundNatRuleConfig** добавляет конфигурацию правила трансляции сетевых адресов (NAT) в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="89477-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="89477-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89477-109">EXAMPLES</span></span>

### <span data-ttu-id="89477-110">Пример 1: Добавление конфигурации правила входящего NAT в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="89477-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="89477-111">Первая команда получает подсистему балансировки нагрузки с именем MyloadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="89477-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="89477-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzureRmLoadBalancerInboundNatRuleConfig** , который добавляет конфигурацию правила входящего NAT в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="89477-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="89477-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89477-113">PARAMETERS</span></span>

### <span data-ttu-id="89477-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="89477-114">-BackendPort</span></span>
<span data-ttu-id="89477-115">Указывает внутренний порт для трафика, соответствующего конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="89477-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="89477-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89477-116">-DefaultProfile</span></span>
<span data-ttu-id="89477-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89477-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89477-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="89477-118">-EnableFloatingIP</span></span>
<span data-ttu-id="89477-119">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="89477-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="89477-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="89477-120">-EnableTcpReset</span></span>
<span data-ttu-id="89477-121">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="89477-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="89477-122">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="89477-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="89477-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="89477-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="89477-124">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="89477-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="89477-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="89477-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="89477-126">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="89477-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="89477-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="89477-127">-FrontendPort</span></span>
<span data-ttu-id="89477-128">Указывает порт переднего плана, совпадающий с конфигурацией правила.</span><span class="sxs-lookup"><span data-stu-id="89477-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="89477-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="89477-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="89477-130">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="89477-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="89477-131">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="89477-131">-LoadBalancer</span></span>
<span data-ttu-id="89477-132">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="89477-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="89477-133">Этот командлет добавляет конфигурацию правила входящего трафика NAT в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="89477-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="89477-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89477-134">-Name</span></span>
<span data-ttu-id="89477-135">Указывает имя конфигурации правила входящего NAT для добавления.</span><span class="sxs-lookup"><span data-stu-id="89477-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="89477-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="89477-136">-Protocol</span></span>
<span data-ttu-id="89477-137">Указывает протокол, совпадающий с правилом входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="89477-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="89477-138">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="89477-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="89477-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89477-139">-Confirm</span></span>
<span data-ttu-id="89477-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89477-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89477-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89477-141">-WhatIf</span></span>
<span data-ttu-id="89477-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89477-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89477-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89477-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89477-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89477-144">CommonParameters</span></span>
<span data-ttu-id="89477-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89477-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89477-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89477-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89477-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89477-147">INPUTS</span></span>

### <span data-ttu-id="89477-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89477-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="89477-149">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89477-149">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="89477-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89477-150">OUTPUTS</span></span>

### <span data-ttu-id="89477-151">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89477-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="89477-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="89477-152">NOTES</span></span>

## <span data-ttu-id="89477-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89477-153">RELATED LINKS</span></span>

[<span data-ttu-id="89477-154">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89477-154">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="89477-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89477-155">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="89477-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89477-156">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="89477-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89477-157">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="89477-158">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="89477-158">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="89477-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="89477-159">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


