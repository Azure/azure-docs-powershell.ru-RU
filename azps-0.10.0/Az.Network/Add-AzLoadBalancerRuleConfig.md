---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 52e1759f82ba6663215907a93f89f562df1b6afa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910132"
---
# <span data-ttu-id="a093f-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a093f-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a093f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a093f-102">SYNOPSIS</span></span>
<span data-ttu-id="a093f-103">Добавляет конфигурацию правила в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="a093f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a093f-104">SYNTAX</span></span>

### <span data-ttu-id="a093f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a093f-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a093f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a093f-106">SetByResource</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a093f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a093f-107">DESCRIPTION</span></span>
<span data-ttu-id="a093f-108">Командлет **Add-AzLoadBalancerRuleConfig** добавляет конфигурацию правил в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a093f-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a093f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a093f-109">EXAMPLES</span></span>

### <span data-ttu-id="a093f-110">Пример 1: Добавление конфигурации правила в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a093f-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="a093f-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="a093f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="a093f-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzLoadBalancerRuleConfig** , который добавляет конфигурацию правила с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="a093f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="a093f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a093f-113">PARAMETERS</span></span>

### <span data-ttu-id="a093f-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a093f-114">-BackendAddressPool</span></span>
<span data-ttu-id="a093f-115">Указывает пул серверных адресов, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a093f-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="a093f-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a093f-118">-BackendPort</span></span>
<span data-ttu-id="a093f-119">Указывает внутренний порт для трафика, соответствующего конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a093f-120">-DefaultProfile</span></span>
<span data-ttu-id="a093f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a093f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="a093f-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="a093f-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a093f-124">-EnableFloatingIP</span></span>
<span data-ttu-id="a093f-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="a093f-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a093f-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a093f-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a093f-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a093f-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a093f-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a093f-130">-FrontendPort</span></span>
<span data-ttu-id="a093f-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a093f-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a093f-133">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-134">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a093f-134">-LoadBalancer</span></span>
<span data-ttu-id="a093f-135">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="a093f-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a093f-136">Этот командлет добавляет конфигурацию правила в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="a093f-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="a093f-137">-LoadDistribution</span></span>
<span data-ttu-id="a093f-138">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-138">Specifies a load distribution.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a093f-139">-Name</span></span>
<span data-ttu-id="a093f-140">Указывает имя конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-140">Specifies the name of the load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-141">-Зонд</span><span class="sxs-lookup"><span data-stu-id="a093f-141">-Probe</span></span>
<span data-ttu-id="a093f-142">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a093f-143">-ProbeId</span></span>
<span data-ttu-id="a093f-144">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-145">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="a093f-145">-Protocol</span></span>
<span data-ttu-id="a093f-146">Specfies протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a093f-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="a093f-147">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="a093f-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a093f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a093f-148">CommonParameters</span></span>
<span data-ttu-id="a093f-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a093f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a093f-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a093f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a093f-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a093f-151">INPUTS</span></span>

### <span data-ttu-id="a093f-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a093f-152">PSLoadBalancer</span></span>
<span data-ttu-id="a093f-153">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a093f-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a093f-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a093f-154">OUTPUTS</span></span>

### <span data-ttu-id="a093f-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a093f-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a093f-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a093f-156">NOTES</span></span>

## <span data-ttu-id="a093f-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a093f-157">RELATED LINKS</span></span>

[<span data-ttu-id="a093f-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a093f-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a093f-159">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a093f-159">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a093f-160">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a093f-160">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a093f-161">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a093f-161">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="a093f-162">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a093f-162">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


