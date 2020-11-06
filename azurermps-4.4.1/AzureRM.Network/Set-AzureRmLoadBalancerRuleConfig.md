---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 2b9c835e99a088a075656cd985004663e5ef094a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562419"
---
# <span data-ttu-id="b1994-101">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1994-101">Set-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b1994-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1994-102">SYNOPSIS</span></span>
<span data-ttu-id="b1994-103">Задает состояние цели для конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-103">Sets the goal state for a load balancer rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1994-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1994-104">SYNTAX</span></span>

### <span data-ttu-id="b1994-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1994-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1994-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b1994-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1994-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1994-107">DESCRIPTION</span></span>
<span data-ttu-id="b1994-108">Командлет **Set-AzureRmLoadBalancerRuleConfig** задает состояние цели для конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-108">The **Set-AzureRmLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="b1994-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1994-109">EXAMPLES</span></span>

### <span data-ttu-id="b1994-110">Пример 1: изменение конфигурации правила балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="b1994-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="b1994-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="b1994-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="b1994-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerRuleConfig, который добавляет к нему правило с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="b1994-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="b1994-113">Третья команда передает балансировщик нагрузки на **Set-AzureRmLoadBalancerRuleConfig** , который задает новую конфигурацию правила.</span><span class="sxs-lookup"><span data-stu-id="b1994-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="b1994-114">Обратите внимание, что в конфигурации не разрешается использование плавающего IP-адреса, который был включен с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="b1994-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="b1994-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1994-115">PARAMETERS</span></span>

### <span data-ttu-id="b1994-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b1994-116">-BackendAddressPool</span></span>
<span data-ttu-id="b1994-117">Указывает объект **BackendAddressPool** , который нужно связать с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b1994-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="b1994-119">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b1994-120">-BackendPort</span></span>
<span data-ttu-id="b1994-121">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="b1994-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="b1994-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="b1994-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="b1994-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b1994-124">-EnableFloatingIP</span></span>
<span data-ttu-id="b1994-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="b1994-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b1994-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1994-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b1994-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b1994-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b1994-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="b1994-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b1994-130">-FrontendPort</span></span>
<span data-ttu-id="b1994-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b1994-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b1994-133">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-134">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="b1994-134">-LoadBalancer</span></span>
<span data-ttu-id="b1994-135">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-135">Specifies a load balancer.</span></span>
<span data-ttu-id="b1994-136">Этот командлет задает конфигурацию правила состояния цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b1994-136">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="b1994-137">-LoadDistribution</span></span>
<span data-ttu-id="b1994-138">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-138">Specifies a load distribution.</span></span>
<span data-ttu-id="b1994-139">Допустимые значения этого параметра: SourceIP и SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="b1994-139">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1994-140">-Name</span></span>
<span data-ttu-id="b1994-141">Указывает имя подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-141">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="b1994-142">-Зонд</span><span class="sxs-lookup"><span data-stu-id="b1994-142">-Probe</span></span>
<span data-ttu-id="b1994-143">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="b1994-144">-ProbeId</span></span>
<span data-ttu-id="b1994-145">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-146">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="b1994-146">-Protocol</span></span>
<span data-ttu-id="b1994-147">Указывает протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b1994-147">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="b1994-148">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="b1994-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1994-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1994-149">-DefaultProfile</span></span>
<span data-ttu-id="b1994-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1994-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1994-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1994-151">CommonParameters</span></span>
<span data-ttu-id="b1994-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1994-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1994-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1994-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1994-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1994-154">INPUTS</span></span>

### <span data-ttu-id="b1994-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1994-155">PSLoadBalancer</span></span>
<span data-ttu-id="b1994-156">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b1994-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b1994-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1994-157">OUTPUTS</span></span>

### <span data-ttu-id="b1994-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1994-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b1994-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1994-159">NOTES</span></span>

## <span data-ttu-id="b1994-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1994-160">RELATED LINKS</span></span>

[<span data-ttu-id="b1994-161">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1994-161">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1994-162">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1994-162">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1994-163">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1994-163">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1994-164">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1994-164">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="b1994-165">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b1994-165">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)


