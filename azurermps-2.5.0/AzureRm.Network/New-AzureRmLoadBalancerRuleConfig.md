---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: f3e256def28dff292efc5ba4278dc4f56b3ec721
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915122"
---
# <span data-ttu-id="a509d-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a509d-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="a509d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a509d-102">SYNOPSIS</span></span>
<span data-ttu-id="a509d-103">Создание конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a509d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a509d-104">SYNTAX</span></span>

### <span data-ttu-id="a509d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a509d-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a509d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a509d-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a509d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a509d-107">DESCRIPTION</span></span>
<span data-ttu-id="a509d-108">Командлет **New-AzureRmLoadBalancerRuleConfig** создает конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a509d-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a509d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a509d-109">EXAMPLES</span></span>

### <span data-ttu-id="a509d-110">1: создание конфигурации правила для подсистемы балансировки нагрузки Azure</span><span class="sxs-lookup"><span data-stu-id="a509d-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="a509d-111">Первые три команды настроили общедоступный IP-адрес, интерфейсный сервер и пробную конфигурацию для конфигурации правила в команде "вперед".</span><span class="sxs-lookup"><span data-stu-id="a509d-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="a509d-112">Для создания нового правила с именем MyLBrule с определенными характеристиками.</span><span class="sxs-lookup"><span data-stu-id="a509d-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="a509d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a509d-113">PARAMETERS</span></span>

### <span data-ttu-id="a509d-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a509d-114">-BackendAddressPool</span></span>
<span data-ttu-id="a509d-115">Указывает объект **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a509d-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="a509d-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a509d-118">-BackendPort</span></span>
<span data-ttu-id="a509d-119">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a509d-120">-DefaultProfile</span></span>
<span data-ttu-id="a509d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a509d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a509d-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="a509d-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="a509d-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="a509d-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a509d-124">-EnableFloatingIP</span></span>
<span data-ttu-id="a509d-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="a509d-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a509d-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a509d-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a509d-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a509d-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a509d-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a509d-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a509d-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a509d-130">-FrontendPort</span></span>
<span data-ttu-id="a509d-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a509d-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a509d-133">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a509d-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="a509d-134">-LoadDistribution</span></span>
<span data-ttu-id="a509d-135">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-135">Specifies a load distribution.</span></span>
<span data-ttu-id="a509d-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a509d-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a509d-137">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a509d-137">Default</span></span>
- <span data-ttu-id="a509d-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="a509d-138">SourceIP</span></span>
- <span data-ttu-id="a509d-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="a509d-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="a509d-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a509d-140">-Name</span></span>
<span data-ttu-id="a509d-141">Указывает имя правила балансировки нагрузки, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a509d-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a509d-142">-Зонд</span><span class="sxs-lookup"><span data-stu-id="a509d-142">-Probe</span></span>
<span data-ttu-id="a509d-143">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a509d-144">-ProbeId</span></span>
<span data-ttu-id="a509d-145">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a509d-146">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="a509d-146">-Protocol</span></span>
<span data-ttu-id="a509d-147">Указывает протокол, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a509d-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="a509d-148">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="a509d-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a509d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a509d-149">CommonParameters</span></span>
<span data-ttu-id="a509d-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a509d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a509d-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a509d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a509d-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a509d-152">INPUTS</span></span>

## <span data-ttu-id="a509d-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a509d-153">OUTPUTS</span></span>

### <span data-ttu-id="a509d-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a509d-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="a509d-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="a509d-155">NOTES</span></span>

## <span data-ttu-id="a509d-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a509d-156">RELATED LINKS</span></span>

[<span data-ttu-id="a509d-157">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a509d-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a509d-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a509d-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a509d-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a509d-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="a509d-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a509d-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


