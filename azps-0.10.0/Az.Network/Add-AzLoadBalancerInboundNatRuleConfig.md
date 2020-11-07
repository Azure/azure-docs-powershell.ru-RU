---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6a699907b70256995973bfdbde4e11b08c594669
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910138"
---
# <span data-ttu-id="26fdf-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26fdf-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="26fdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="26fdf-103">Добавляет конфигурацию правила NAT для входящего трафика в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="26fdf-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="26fdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26fdf-104">SYNTAX</span></span>

### <span data-ttu-id="26fdf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="26fdf-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26fdf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="26fdf-106">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26fdf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26fdf-107">DESCRIPTION</span></span>
<span data-ttu-id="26fdf-108">Командлет **Add-AzLoadBalancerInboundNatRuleConfig** добавляет конфигурацию правила трансляции сетевых адресов (NAT) в подсистему балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="26fdf-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="26fdf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26fdf-109">EXAMPLES</span></span>

### <span data-ttu-id="26fdf-110">Пример 1: Добавление конфигурации правила входящего NAT в подсистему балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="26fdf-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="26fdf-111">Первая команда получает подсистему балансировки нагрузки с именем MyloadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="26fdf-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="26fdf-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на **Add-AzLoadBalancerInboundNatRuleConfig** , который добавляет конфигурацию правила входящего NAT в подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="26fdf-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="26fdf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26fdf-113">PARAMETERS</span></span>

### <span data-ttu-id="26fdf-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="26fdf-114">-BackendPort</span></span>
<span data-ttu-id="26fdf-115">Указывает внутренний порт для трафика, соответствующего конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="26fdf-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="26fdf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fdf-116">-DefaultProfile</span></span>
<span data-ttu-id="26fdf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26fdf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26fdf-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="26fdf-118">-EnableFloatingIP</span></span>
<span data-ttu-id="26fdf-119">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="26fdf-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="26fdf-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="26fdf-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="26fdf-121">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила входящего трафика NAT.</span><span class="sxs-lookup"><span data-stu-id="26fdf-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="26fdf-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="26fdf-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="26fdf-123">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="26fdf-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="26fdf-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="26fdf-124">-FrontendPort</span></span>
<span data-ttu-id="26fdf-125">Указывает порт переднего плана, совпадающий с конфигурацией правила.</span><span class="sxs-lookup"><span data-stu-id="26fdf-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="26fdf-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="26fdf-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="26fdf-127">Указывает продолжительность времени (в минутах), в течение которого сохраняется состояние бесед в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="26fdf-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="26fdf-128">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="26fdf-128">-LoadBalancer</span></span>
<span data-ttu-id="26fdf-129">Указывает объект подсистемы **балансировки нагрузки** .</span><span class="sxs-lookup"><span data-stu-id="26fdf-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="26fdf-130">Этот командлет добавляет конфигурацию правила входящего трафика NAT в подсистему балансировки нагрузки, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="26fdf-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="26fdf-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26fdf-131">-Name</span></span>
<span data-ttu-id="26fdf-132">Указывает имя конфигурации правила входящего NAT для добавления.</span><span class="sxs-lookup"><span data-stu-id="26fdf-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="26fdf-133">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="26fdf-133">-Protocol</span></span>
<span data-ttu-id="26fdf-134">Указывает протокол, совпадающий с правилом входящего NAT.</span><span class="sxs-lookup"><span data-stu-id="26fdf-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="26fdf-135">Допустимые значения этого параметра: TCP или UDP.</span><span class="sxs-lookup"><span data-stu-id="26fdf-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="26fdf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fdf-136">CommonParameters</span></span>
<span data-ttu-id="26fdf-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26fdf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fdf-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26fdf-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fdf-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26fdf-139">INPUTS</span></span>

### <span data-ttu-id="26fdf-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26fdf-140">PSLoadBalancer</span></span>
<span data-ttu-id="26fdf-141">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="26fdf-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="26fdf-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26fdf-142">OUTPUTS</span></span>

### <span data-ttu-id="26fdf-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26fdf-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="26fdf-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="26fdf-144">NOTES</span></span>

## <span data-ttu-id="26fdf-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26fdf-145">RELATED LINKS</span></span>

[<span data-ttu-id="26fdf-146">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26fdf-146">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="26fdf-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26fdf-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="26fdf-148">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26fdf-148">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="26fdf-149">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26fdf-149">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="26fdf-150">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="26fdf-150">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="26fdf-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26fdf-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


