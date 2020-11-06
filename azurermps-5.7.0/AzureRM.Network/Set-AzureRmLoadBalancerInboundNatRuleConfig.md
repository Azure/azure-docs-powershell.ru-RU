---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 98f7052ab0fa326789242cdebaf34f188684993e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561696"
---
# <span data-ttu-id="f7573-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7573-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f7573-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7573-102">SYNOPSIS</span></span>
<span data-ttu-id="f7573-103">Задает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f7573-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7573-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7573-104">SYNTAX</span></span>

### <span data-ttu-id="f7573-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7573-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7573-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f7573-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7573-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7573-107">DESCRIPTION</span></span>
<span data-ttu-id="f7573-108">Командлет **Set-AzureRmLoadBalancerInboundNatRuleConfig** устанавливает конфигурацию правила трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="f7573-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f7573-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7573-109">EXAMPLES</span></span>

### <span data-ttu-id="f7573-110">Пример 1: изменение конфигурации правила входящего NAT для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="f7573-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="f7573-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="f7573-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="f7573-112">Вторая команда использует оператор Pipeline для передачи подсистемы балансировки нагрузки в $slb на Add-AzureRmLoadBalancerInboundNatRuleConfig, который добавляет в него конфигурацию правила входящей сети NAT.</span><span class="sxs-lookup"><span data-stu-id="f7573-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="f7573-113">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancerInboundNatRuleConfig** , которая сохраняет и обновляет конфигурацию правила входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="f7573-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="f7573-114">Обратите внимание, что конфигурация правила задана без включения плавающего IP-адреса, которая была включена предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="f7573-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="f7573-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7573-115">PARAMETERS</span></span>

### <span data-ttu-id="f7573-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="f7573-116">-BackendPort</span></span>
<span data-ttu-id="f7573-117">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f7573-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="f7573-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7573-118">-DefaultProfile</span></span>
<span data-ttu-id="f7573-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7573-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7573-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="f7573-120">-EnableFloatingIP</span></span>
<span data-ttu-id="f7573-121">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="f7573-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="f7573-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7573-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="f7573-123">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="f7573-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f7573-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f7573-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="f7573-125">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="f7573-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="f7573-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7573-126">-FrontendPort</span></span>
<span data-ttu-id="f7573-127">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f7573-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="f7573-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f7573-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f7573-129">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f7573-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="f7573-130">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="f7573-130">-LoadBalancer</span></span>
<span data-ttu-id="f7573-131">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f7573-131">Specifies a load balancer.</span></span>
<span data-ttu-id="f7573-132">Этот командлет задает конфигурацию правила входящего NAT для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f7573-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="f7573-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7573-133">-Name</span></span>
<span data-ttu-id="f7573-134">Указывает имя конфигурации правила входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="f7573-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="f7573-135">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f7573-135">-Protocol</span></span>
<span data-ttu-id="f7573-136">Указывает протокол, совпадающий с конфигурацией правила входящей NAT.</span><span class="sxs-lookup"><span data-stu-id="f7573-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="f7573-137">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="f7573-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="f7573-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7573-138">CommonParameters</span></span>
<span data-ttu-id="f7573-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7573-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7573-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7573-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7573-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7573-141">INPUTS</span></span>

### <span data-ttu-id="f7573-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7573-142">PSLoadBalancer</span></span>
<span data-ttu-id="f7573-143">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f7573-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f7573-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7573-144">OUTPUTS</span></span>

### <span data-ttu-id="f7573-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7573-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f7573-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7573-146">NOTES</span></span>

## <span data-ttu-id="f7573-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7573-147">RELATED LINKS</span></span>

[<span data-ttu-id="f7573-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7573-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f7573-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7573-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f7573-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7573-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f7573-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7573-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f7573-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f7573-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


