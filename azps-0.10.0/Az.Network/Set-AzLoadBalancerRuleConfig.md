---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911036"
---
# <span data-ttu-id="f2718-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2718-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f2718-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2718-102">SYNOPSIS</span></span>
<span data-ttu-id="f2718-103">Задает состояние цели для конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="f2718-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2718-104">SYNTAX</span></span>

### <span data-ttu-id="f2718-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2718-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2718-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f2718-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2718-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2718-107">DESCRIPTION</span></span>
<span data-ttu-id="f2718-108">Командлет **Set-AzLoadBalancerRuleConfig** задает состояние цели для конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="f2718-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2718-109">EXAMPLES</span></span>

### <span data-ttu-id="f2718-110">Пример 1: изменение конфигурации правила балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="f2718-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="f2718-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="f2718-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="f2718-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerRuleConfig, который добавляет к нему правило с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="f2718-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="f2718-113">Третья команда передает балансировщик нагрузки на **Set-AzLoadBalancerRuleConfig** , который задает новую конфигурацию правила.</span><span class="sxs-lookup"><span data-stu-id="f2718-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="f2718-114">Обратите внимание, что в конфигурации не разрешается использование плавающего IP-адреса, который был включен с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="f2718-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="f2718-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2718-115">PARAMETERS</span></span>

### <span data-ttu-id="f2718-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2718-116">-BackendAddressPool</span></span>
<span data-ttu-id="f2718-117">Указывает объект **BackendAddressPool** , который нужно связать с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="f2718-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f2718-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f2718-119">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f2718-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f2718-120">-BackendPort</span></span>
<span data-ttu-id="f2718-121">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f2718-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="f2718-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2718-122">-DefaultProfile</span></span>
<span data-ttu-id="f2718-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2718-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2718-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="f2718-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="f2718-125">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="f2718-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f2718-126">-EnableFloatingIP</span></span>
<span data-ttu-id="f2718-127">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f2718-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f2718-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2718-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f2718-129">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f2718-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f2718-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f2718-131">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f2718-131">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f2718-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f2718-132">-FrontendPort</span></span>
<span data-ttu-id="f2718-133">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f2718-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f2718-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f2718-135">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f2718-136">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="f2718-136">-LoadBalancer</span></span>
<span data-ttu-id="f2718-137">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-137">Specifies a load balancer.</span></span>
<span data-ttu-id="f2718-138">Этот командлет задает конфигурацию правила состояния цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f2718-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2718-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="f2718-139">-LoadDistribution</span></span>
<span data-ttu-id="f2718-140">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-140">Specifies a load distribution.</span></span>
<span data-ttu-id="f2718-141">Допустимые значения этого параметра: SourceIP и SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="f2718-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="f2718-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2718-142">-Name</span></span>
<span data-ttu-id="f2718-143">Указывает имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-143">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="f2718-144">-Зонд</span><span class="sxs-lookup"><span data-stu-id="f2718-144">-Probe</span></span>
<span data-ttu-id="f2718-145">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f2718-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="f2718-146">-ProbeId</span></span>
<span data-ttu-id="f2718-147">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f2718-148">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f2718-148">-Protocol</span></span>
<span data-ttu-id="f2718-149">Указывает протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f2718-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="f2718-150">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="f2718-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f2718-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2718-151">CommonParameters</span></span>
<span data-ttu-id="f2718-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2718-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2718-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2718-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2718-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2718-154">INPUTS</span></span>

### <span data-ttu-id="f2718-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2718-155">PSLoadBalancer</span></span>
<span data-ttu-id="f2718-156">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f2718-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f2718-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2718-157">OUTPUTS</span></span>

### <span data-ttu-id="f2718-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f2718-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f2718-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2718-159">NOTES</span></span>

## <span data-ttu-id="f2718-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2718-160">RELATED LINKS</span></span>

[<span data-ttu-id="f2718-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2718-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f2718-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2718-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f2718-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2718-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f2718-164">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2718-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="f2718-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f2718-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


