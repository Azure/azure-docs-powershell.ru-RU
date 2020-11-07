---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ed21aec1be522ac145fe255065b650ca4c09dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734947"
---
# <span data-ttu-id="08494-101">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08494-101">Add-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="08494-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08494-102">SYNOPSIS</span></span>
<span data-ttu-id="08494-103">Добавляет конфигурацию правила в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-103">Adds a rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08494-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08494-104">SYNTAX</span></span>

### <span data-ttu-id="08494-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08494-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08494-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="08494-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08494-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08494-107">DESCRIPTION</span></span>
<span data-ttu-id="08494-108">Командлет **Add-AzureRmLoadBalancerRuleConfig** добавляет конфигурацию правил в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="08494-108">The **Add-AzureRmLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="08494-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08494-109">EXAMPLES</span></span>

### <span data-ttu-id="08494-110">Пример 1: Добавление конфигурации правила в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="08494-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="08494-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="08494-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="08494-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzureRmLoadBalancerRuleConfig** , который добавляет конфигурацию правила с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="08494-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="08494-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08494-113">PARAMETERS</span></span>

### <span data-ttu-id="08494-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="08494-114">-BackendAddressPool</span></span>
<span data-ttu-id="08494-115">Указывает пул серверных адресов, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08494-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="08494-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="08494-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="08494-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="08494-118">-BackendPort</span></span>
<span data-ttu-id="08494-119">Указывает внутренний порт для трафика, соответствующего конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="08494-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08494-120">-DefaultProfile</span></span>
<span data-ttu-id="08494-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08494-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08494-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="08494-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="08494-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="08494-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="08494-124">-EnableFloatingIP</span></span>
<span data-ttu-id="08494-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="08494-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="08494-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="08494-126">-EnableTcpReset</span></span>
<span data-ttu-id="08494-127">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="08494-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="08494-128">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="08494-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="08494-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="08494-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="08494-130">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="08494-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="08494-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="08494-132">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="08494-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="08494-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="08494-133">-FrontendPort</span></span>
<span data-ttu-id="08494-134">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="08494-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="08494-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="08494-136">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-136">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="08494-137">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="08494-137">-LoadBalancer</span></span>
<span data-ttu-id="08494-138">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="08494-138">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="08494-139">Этот командлет добавляет конфигурацию правила в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="08494-139">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="08494-140">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="08494-140">-LoadDistribution</span></span>
<span data-ttu-id="08494-141">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-141">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="08494-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08494-142">-Name</span></span>
<span data-ttu-id="08494-143">Указывает имя конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-143">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="08494-144">-Зонд</span><span class="sxs-lookup"><span data-stu-id="08494-144">-Probe</span></span>
<span data-ttu-id="08494-145">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08494-146">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="08494-146">-ProbeId</span></span>
<span data-ttu-id="08494-147">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="08494-148">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="08494-148">-Protocol</span></span>
<span data-ttu-id="08494-149">Specfies протокол, совпадающий с правилом подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08494-149">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="08494-150">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="08494-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="08494-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08494-151">-Confirm</span></span>
<span data-ttu-id="08494-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08494-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08494-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08494-153">-WhatIf</span></span>
<span data-ttu-id="08494-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08494-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08494-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08494-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08494-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08494-156">CommonParameters</span></span>
<span data-ttu-id="08494-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08494-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08494-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08494-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08494-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08494-159">INPUTS</span></span>

### <span data-ttu-id="08494-160">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08494-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="08494-161">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="08494-161">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="08494-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08494-162">OUTPUTS</span></span>

### <span data-ttu-id="08494-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08494-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="08494-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="08494-164">NOTES</span></span>

## <span data-ttu-id="08494-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08494-165">RELATED LINKS</span></span>

[<span data-ttu-id="08494-166">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08494-166">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="08494-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08494-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="08494-168">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08494-168">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="08494-169">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08494-169">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="08494-170">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08494-170">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


