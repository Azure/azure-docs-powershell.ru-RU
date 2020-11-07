---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909674"
---
# <span data-ttu-id="efe7e-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efe7e-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="efe7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efe7e-102">SYNOPSIS</span></span>
<span data-ttu-id="efe7e-103">Создание конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="efe7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efe7e-104">SYNTAX</span></span>

### <span data-ttu-id="efe7e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="efe7e-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efe7e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="efe7e-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efe7e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efe7e-107">DESCRIPTION</span></span>
<span data-ttu-id="efe7e-108">Командлет **New-AzLoadBalancerRuleConfig** создает конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="efe7e-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="efe7e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efe7e-109">EXAMPLES</span></span>

### <span data-ttu-id="efe7e-110">1: создание конфигурации правила для подсистемы балансировки нагрузки Azure</span><span class="sxs-lookup"><span data-stu-id="efe7e-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="efe7e-111">Первые три команды настроили общедоступный IP-адрес, интерфейсный сервер и пробную конфигурацию для конфигурации правила в команде "вперед".</span><span class="sxs-lookup"><span data-stu-id="efe7e-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="efe7e-112">Для создания нового правила с именем MyLBrule с определенными характеристиками.</span><span class="sxs-lookup"><span data-stu-id="efe7e-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="efe7e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efe7e-113">PARAMETERS</span></span>

### <span data-ttu-id="efe7e-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="efe7e-114">-BackendAddressPool</span></span>
<span data-ttu-id="efe7e-115">Указывает объект **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="efe7e-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="efe7e-117">Указывает идентификатор объекта **BackendAddressPool** , который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="efe7e-118">-BackendPort</span></span>
<span data-ttu-id="efe7e-119">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe7e-120">-DefaultProfile</span></span>
<span data-ttu-id="efe7e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efe7e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efe7e-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="efe7e-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="efe7e-123">Настраивает SNAT для виртуальных машин в пуле баз данных, чтобы использовать адрес publicIP, указанный на интерфейсе правила балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="efe7e-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="efe7e-124">-EnableFloatingIP</span></span>
<span data-ttu-id="efe7e-125">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="efe7e-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="efe7e-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="efe7e-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="efe7e-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="efe7e-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="efe7e-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="efe7e-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="efe7e-130">-FrontendPort</span></span>
<span data-ttu-id="efe7e-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="efe7e-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="efe7e-133">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="efe7e-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="efe7e-134">-LoadDistribution</span></span>
<span data-ttu-id="efe7e-135">Указывает распределение нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-135">Specifies a load distribution.</span></span>
<span data-ttu-id="efe7e-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="efe7e-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efe7e-137">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="efe7e-137">Default</span></span>
- <span data-ttu-id="efe7e-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="efe7e-138">SourceIP</span></span>
- <span data-ttu-id="efe7e-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="efe7e-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="efe7e-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="efe7e-140">-Name</span></span>
<span data-ttu-id="efe7e-141">Указывает имя правила балансировки нагрузки, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="efe7e-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="efe7e-142">-Зонд</span><span class="sxs-lookup"><span data-stu-id="efe7e-142">-Probe</span></span>
<span data-ttu-id="efe7e-143">Указывает зонд для связи с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="efe7e-144">-ProbeId</span></span>
<span data-ttu-id="efe7e-145">Указывает идентификатор зонда, который нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="efe7e-146">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="efe7e-146">-Protocol</span></span>
<span data-ttu-id="efe7e-147">Указывает протокол, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="efe7e-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="efe7e-148">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="efe7e-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="efe7e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe7e-149">CommonParameters</span></span>
<span data-ttu-id="efe7e-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efe7e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe7e-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efe7e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe7e-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efe7e-152">INPUTS</span></span>

## <span data-ttu-id="efe7e-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efe7e-153">OUTPUTS</span></span>

### <span data-ttu-id="efe7e-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="efe7e-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="efe7e-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="efe7e-155">NOTES</span></span>

## <span data-ttu-id="efe7e-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efe7e-156">RELATED LINKS</span></span>

[<span data-ttu-id="efe7e-157">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efe7e-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="efe7e-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efe7e-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="efe7e-159">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efe7e-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="efe7e-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="efe7e-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


