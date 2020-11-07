---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911043"
---
# <span data-ttu-id="0f4e0-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f4e0-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="0f4e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4e0-103">Задает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0f4e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f4e0-104">SYNTAX</span></span>

### <span data-ttu-id="0f4e0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f4e0-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f4e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0f4e0-106">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4e0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f4e0-107">DESCRIPTION</span></span>
<span data-ttu-id="0f4e0-108">Командлет **Set-AzLoadBalancerInboundNatRuleConfig** устанавливает конфигурацию правила трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0f4e0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f4e0-109">EXAMPLES</span></span>

### <span data-ttu-id="0f4e0-110">Пример 1: изменение конфигурации правила входящего NAT для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="0f4e0-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="0f4e0-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="0f4e0-112">Вторая команда использует оператор Pipeline для передачи подсистемы балансировки нагрузки в $slb на Add-AzLoadBalancerInboundNatRuleConfig, который добавляет в него конфигурацию правила входящей сети NAT.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="0f4e0-113">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancerInboundNatRuleConfig** , которая сохраняет и обновляет конфигурацию правила входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="0f4e0-114">Обратите внимание, что конфигурация правила задана без включения плавающего IP-адреса, которая была включена предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="0f4e0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f4e0-115">PARAMETERS</span></span>

### <span data-ttu-id="0f4e0-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0f4e0-116">-BackendPort</span></span>
<span data-ttu-id="0f4e0-117">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="0f4e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4e0-118">-DefaultProfile</span></span>
<span data-ttu-id="0f4e0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f4e0-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0f4e0-120">-EnableFloatingIP</span></span>
<span data-ttu-id="0f4e0-121">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0f4e0-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f4e0-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0f4e0-123">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="0f4e0-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0f4e0-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0f4e0-125">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0f4e0-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0f4e0-126">-FrontendPort</span></span>
<span data-ttu-id="0f4e0-127">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="0f4e0-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0f4e0-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0f4e0-129">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="0f4e0-130">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="0f4e0-130">-LoadBalancer</span></span>
<span data-ttu-id="0f4e0-131">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-131">Specifies a load balancer.</span></span>
<span data-ttu-id="0f4e0-132">Этот командлет задает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f4e0-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f4e0-133">-Name</span></span>
<span data-ttu-id="0f4e0-134">Указывает имя конфигурации правила входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="0f4e0-135">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="0f4e0-135">-Protocol</span></span>
<span data-ttu-id="0f4e0-136">Указывает протокол, совпадающий с конфигурацией правила входящей NAT.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="0f4e0-137">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f4e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4e0-138">CommonParameters</span></span>
<span data-ttu-id="0f4e0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4e0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f4e0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4e0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f4e0-141">INPUTS</span></span>

### <span data-ttu-id="0f4e0-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4e0-142">PSLoadBalancer</span></span>
<span data-ttu-id="0f4e0-143">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0f4e0-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="0f4e0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f4e0-144">OUTPUTS</span></span>

### <span data-ttu-id="0f4e0-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4e0-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f4e0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f4e0-146">NOTES</span></span>

## <span data-ttu-id="0f4e0-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f4e0-147">RELATED LINKS</span></span>

[<span data-ttu-id="0f4e0-148">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f4e0-148">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0f4e0-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f4e0-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0f4e0-150">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f4e0-150">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0f4e0-151">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f4e0-151">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0f4e0-152">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0f4e0-152">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


