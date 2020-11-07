---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: 0708540cbb0ccac2f445fc0692c3c91f9358213c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914434"
---
# <span data-ttu-id="a48b8-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a48b8-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a48b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a48b8-102">SYNOPSIS</span></span>
<span data-ttu-id="a48b8-103">Добавляет конфигурацию правила в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a48b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a48b8-104">SYNTAX</span></span>

### <span data-ttu-id="a48b8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a48b8-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a48b8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a48b8-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a48b8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a48b8-107">DESCRIPTION</span></span>
<span data-ttu-id="a48b8-108">Командлет **Add-AzureRmLoadBalancerRuleConfig** добавляет конфигурацию правил в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a48b8-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="a48b8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a48b8-109">EXAMPLES</span></span>

### <span data-ttu-id="a48b8-110">Пример 1: Добавление конфигурации правила в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a48b8-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="a48b8-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="a48b8-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="a48b8-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzureRmLoadBalancerRuleConfig** , который добавляет конфигурацию правила с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="a48b8-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="a48b8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a48b8-113">PARAMETERS</span></span>

### <span data-ttu-id="a48b8-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a48b8-114">-BackendAddressPool</span></span>
<span data-ttu-id="a48b8-115">Указывает пул серверных адресов, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a48b8-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="a48b8-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a48b8-118">-BackendPort</span></span>
<span data-ttu-id="a48b8-119">Указывает внутренний порт для трафика, соответствующего конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a48b8-120">-DefaultProfile</span></span>
<span data-ttu-id="a48b8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a48b8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a48b8-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="a48b8-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="a48b8-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="a48b8-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a48b8-124">-EnableFloatingIP</span></span>
<span data-ttu-id="a48b8-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="a48b8-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a48b8-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a48b8-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a48b8-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a48b8-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a48b8-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a48b8-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a48b8-130">-FrontendPort</span></span>
<span data-ttu-id="a48b8-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a48b8-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a48b8-133">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="a48b8-134">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a48b8-134">-LoadBalancer</span></span>
<span data-ttu-id="a48b8-135">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="a48b8-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="a48b8-136">Этот командлет добавляет конфигурацию правила в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="a48b8-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a48b8-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="a48b8-137">-LoadDistribution</span></span>
<span data-ttu-id="a48b8-138">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="a48b8-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a48b8-139">-Name</span></span>
<span data-ttu-id="a48b8-140">Указывает имя конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-141">-Зонд</span><span class="sxs-lookup"><span data-stu-id="a48b8-141">-Probe</span></span>
<span data-ttu-id="a48b8-142">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-143">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a48b8-143">-ProbeId</span></span>
<span data-ttu-id="a48b8-144">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a48b8-145">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="a48b8-145">-Protocol</span></span>
<span data-ttu-id="a48b8-146">Specfies протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a48b8-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="a48b8-147">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="a48b8-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a48b8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a48b8-148">CommonParameters</span></span>
<span data-ttu-id="a48b8-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a48b8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a48b8-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a48b8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a48b8-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a48b8-151">INPUTS</span></span>

### <span data-ttu-id="a48b8-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a48b8-152">PSLoadBalancer</span></span>
<span data-ttu-id="a48b8-153">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a48b8-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a48b8-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a48b8-154">OUTPUTS</span></span>

### <span data-ttu-id="a48b8-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a48b8-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a48b8-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a48b8-156">NOTES</span></span>

## <span data-ttu-id="a48b8-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a48b8-157">RELATED LINKS</span></span>

[<span data-ttu-id="a48b8-158">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a48b8-158">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a48b8-159">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a48b8-159">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a48b8-160">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a48b8-160">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a48b8-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a48b8-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a48b8-162">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a48b8-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


