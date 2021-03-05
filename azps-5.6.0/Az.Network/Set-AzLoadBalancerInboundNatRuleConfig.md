---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: a0d5adbc1e3fb2b38ded91431ab0cf349c541ebd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963891"
---
# <span data-ttu-id="fcf12-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcf12-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="fcf12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf12-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf12-103">Настраивает правила NAT для входящие остаток на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fcf12-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="fcf12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fcf12-104">SYNTAX</span></span>

### <span data-ttu-id="fcf12-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcf12-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcf12-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fcf12-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcf12-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf12-107">DESCRIPTION</span></span>
<span data-ttu-id="fcf12-108">Cmdlet **Set-AzLoadBalancerInboundNatRuleConfig** задает конфигурацию правила перевода сетевых адресов (NAT) для балансиров нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf12-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="fcf12-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fcf12-109">EXAMPLES</span></span>

### <span data-ttu-id="fcf12-110">Пример 1. Изменение конфигурации входящие правила NAT для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="fcf12-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="fcf12-111">Первая команда получает балансировку нагрузки с именем MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="fcf12-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="fcf12-112">Вторая команда передает балансиру нагрузки в $slb add-AzLoadBalancerInboundNatRuleConfig, который добавляет в него конфигурацию правила NAT для входящие проектов.</span><span class="sxs-lookup"><span data-stu-id="fcf12-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="fcf12-113">Третья команда передает балансиру нагрузки в **set-AzLoadBalancerInboundNatRuleConfig,** который сохраняет и обновляет конфигурацию входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="fcf12-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="fcf12-114">Обратите внимание, что конфигурация правила была настроена без включения плавающего IP-адреса, который был включен предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="fcf12-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="fcf12-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcf12-115">PARAMETERS</span></span>

### <span data-ttu-id="fcf12-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fcf12-116">-BackendPort</span></span>
<span data-ttu-id="fcf12-117">Определяет порт для трафика, на который совме задана конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="fcf12-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="fcf12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf12-118">-DefaultProfile</span></span>
<span data-ttu-id="fcf12-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf12-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf12-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="fcf12-120">-EnableFloatingIP</span></span>
<span data-ttu-id="fcf12-121">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="fcf12-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="fcf12-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="fcf12-122">-EnableTcpReset</span></span>
<span data-ttu-id="fcf12-123">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="fcf12-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="fcf12-124">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="fcf12-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="fcf12-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcf12-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="fcf12-126">Список IP-адресов, которые нужно связать с конфигурацией правила NAT входящие.</span><span class="sxs-lookup"><span data-stu-id="fcf12-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="fcf12-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fcf12-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="fcf12-128">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="fcf12-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="fcf12-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="fcf12-129">-FrontendPort</span></span>
<span data-ttu-id="fcf12-130">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fcf12-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="fcf12-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fcf12-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fcf12-132">Определяет продолжительность бесед (в минутах), которая сохраняется в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="fcf12-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="fcf12-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcf12-133">-LoadBalancer</span></span>
<span data-ttu-id="fcf12-134">Определяет балансировую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="fcf12-134">Specifies a load balancer.</span></span>
<span data-ttu-id="fcf12-135">Этот cmdlet задает конфигурацию правила NAT для балансиростной нагрузки, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="fcf12-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcf12-136">-Name</span><span class="sxs-lookup"><span data-stu-id="fcf12-136">-Name</span></span>
<span data-ttu-id="fcf12-137">Указывает имя конфигурации входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="fcf12-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="fcf12-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="fcf12-138">-Protocol</span></span>
<span data-ttu-id="fcf12-139">Определяет протокол, который соответствует конфигурации входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="fcf12-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="fcf12-140">Допустимыми значениями для этого параметра являются Tcp или UDP.</span><span class="sxs-lookup"><span data-stu-id="fcf12-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="fcf12-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcf12-141">-Confirm</span></span>
<span data-ttu-id="fcf12-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf12-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf12-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf12-143">-WhatIf</span></span>
<span data-ttu-id="fcf12-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf12-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcf12-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fcf12-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf12-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf12-146">CommonParameters</span></span>
<span data-ttu-id="fcf12-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf12-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf12-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf12-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf12-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf12-149">INPUTS</span></span>

### <span data-ttu-id="fcf12-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcf12-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="fcf12-151">System.String</span><span class="sxs-lookup"><span data-stu-id="fcf12-151">System.String</span></span>

### <span data-ttu-id="fcf12-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fcf12-152">System.Int32</span></span>

### <span data-ttu-id="fcf12-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fcf12-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="fcf12-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf12-154">OUTPUTS</span></span>

### <span data-ttu-id="fcf12-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcf12-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fcf12-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fcf12-156">NOTES</span></span>

## <span data-ttu-id="fcf12-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcf12-157">RELATED LINKS</span></span>

[<span data-ttu-id="fcf12-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcf12-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fcf12-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fcf12-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="fcf12-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcf12-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fcf12-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcf12-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="fcf12-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fcf12-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


