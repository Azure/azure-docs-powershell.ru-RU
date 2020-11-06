---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564247"
---
# <span data-ttu-id="f30b8-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f30b8-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="f30b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f30b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f30b8-103">Создание конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f30b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f30b8-104">SYNTAX</span></span>

### <span data-ttu-id="f30b8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f30b8-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f30b8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f30b8-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30b8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f30b8-107">DESCRIPTION</span></span>
<span data-ttu-id="f30b8-108">Командлет **New-AzureRmLoadBalancerRuleConfig** создает конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="f30b8-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f30b8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f30b8-109">EXAMPLES</span></span>

### <span data-ttu-id="f30b8-110">1: создание конфигурации правила для подсистемы балансировки нагрузки Azure</span><span class="sxs-lookup"><span data-stu-id="f30b8-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="f30b8-111">Первые три команды настроили общедоступный IP-адрес, интерфейсный сервер и пробную конфигурацию для конфигурации правила в команде "вперед".</span><span class="sxs-lookup"><span data-stu-id="f30b8-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="f30b8-112">Для создания нового правила с именем MyLBrule с определенными характеристиками.</span><span class="sxs-lookup"><span data-stu-id="f30b8-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="f30b8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f30b8-113">PARAMETERS</span></span>

### <span data-ttu-id="f30b8-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f30b8-114">-BackendAddressPool</span></span>
<span data-ttu-id="f30b8-115">Указывает объект **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f30b8-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="f30b8-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f30b8-118">-BackendPort</span></span>
<span data-ttu-id="f30b8-119">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30b8-120">-DefaultProfile</span></span>
<span data-ttu-id="f30b8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f30b8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30b8-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="f30b8-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="f30b8-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="f30b8-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f30b8-124">-EnableFloatingIP</span></span>
<span data-ttu-id="f30b8-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f30b8-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="f30b8-126">-EnableTcpReset</span></span>
<span data-ttu-id="f30b8-127">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="f30b8-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="f30b8-128">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="f30b8-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="f30b8-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f30b8-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f30b8-130">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f30b8-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f30b8-132">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f30b8-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f30b8-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f30b8-133">-FrontendPort</span></span>
<span data-ttu-id="f30b8-134">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f30b8-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f30b8-136">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f30b8-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="f30b8-137">-LoadDistribution</span></span>
<span data-ttu-id="f30b8-138">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-138">Specifies a load distribution.</span></span>
<span data-ttu-id="f30b8-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f30b8-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f30b8-140">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="f30b8-140">Default</span></span>
- <span data-ttu-id="f30b8-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="f30b8-141">SourceIP</span></span>
- <span data-ttu-id="f30b8-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="f30b8-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="f30b8-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f30b8-143">-Name</span></span>
<span data-ttu-id="f30b8-144">Указывает имя правила балансировки нагрузки, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f30b8-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f30b8-145">-Зонд</span><span class="sxs-lookup"><span data-stu-id="f30b8-145">-Probe</span></span>
<span data-ttu-id="f30b8-146">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="f30b8-147">-ProbeId</span></span>
<span data-ttu-id="f30b8-148">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f30b8-149">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f30b8-149">-Protocol</span></span>
<span data-ttu-id="f30b8-150">Указывает протокол, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f30b8-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="f30b8-151">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="f30b8-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f30b8-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f30b8-152">-Confirm</span></span>
<span data-ttu-id="f30b8-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f30b8-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30b8-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30b8-154">-WhatIf</span></span>
<span data-ttu-id="f30b8-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f30b8-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f30b8-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f30b8-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30b8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30b8-157">CommonParameters</span></span>
<span data-ttu-id="f30b8-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f30b8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30b8-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30b8-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30b8-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f30b8-160">INPUTS</span></span>

### <span data-ttu-id="f30b8-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="f30b8-161">None</span></span>

## <span data-ttu-id="f30b8-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f30b8-162">OUTPUTS</span></span>

### <span data-ttu-id="f30b8-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="f30b8-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="f30b8-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="f30b8-164">NOTES</span></span>

## <span data-ttu-id="f30b8-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f30b8-165">RELATED LINKS</span></span>

[<span data-ttu-id="f30b8-166">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f30b8-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f30b8-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f30b8-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f30b8-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f30b8-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="f30b8-169">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f30b8-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


