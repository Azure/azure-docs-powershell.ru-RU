---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1c813a7ac23ae8bc161f10df02ac618d5f6a7a81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565851"
---
# <span data-ttu-id="44c32-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44c32-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="44c32-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44c32-102">SYNOPSIS</span></span>
<span data-ttu-id="44c32-103">Задает конфигурацию исходящего правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="44c32-103">Sets an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44c32-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44c32-104">SYNTAX</span></span>

### <span data-ttu-id="44c32-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44c32-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44c32-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="44c32-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44c32-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c32-107">DESCRIPTION</span></span>
<span data-ttu-id="44c32-108">Командлет **Set-AzureRmLoadBalancerOutboundRuleConfig** задает конфигурацию исходящего правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="44c32-108">The **Set-AzureRmLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="44c32-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44c32-109">EXAMPLES</span></span>

### <span data-ttu-id="44c32-110">Пример 1: изменение конфигурации правила исходящего трафика для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="44c32-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="44c32-111">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="44c32-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="44c32-112">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerOutboundRuleConfig, который добавляет в него конфигурацию исходящего правила.</span><span class="sxs-lookup"><span data-stu-id="44c32-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="44c32-113">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancerOutboundRuleConfig** , которая сохраняет и обновляет конфигурацию исходящего правила.</span><span class="sxs-lookup"><span data-stu-id="44c32-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="44c32-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44c32-114">PARAMETERS</span></span>

### <span data-ttu-id="44c32-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="44c32-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="44c32-116">Количество исходящих портов, используемых для NAT.</span><span class="sxs-lookup"><span data-stu-id="44c32-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="44c32-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="44c32-117">-BackendAddressPool</span></span>
<span data-ttu-id="44c32-118">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="44c32-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="44c32-119">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="44c32-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c32-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="44c32-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="44c32-121">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="44c32-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="44c32-122">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="44c32-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c32-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c32-123">-DefaultProfile</span></span>
<span data-ttu-id="44c32-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44c32-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c32-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="44c32-125">-EnableTcpReset</span></span>
<span data-ttu-id="44c32-126">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="44c32-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="44c32-127">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="44c32-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="44c32-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="44c32-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="44c32-129">IP-адреса переднего плана для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="44c32-129">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c32-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="44c32-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="44c32-131">Время ожидания для подключения по протоколу бездействия TCP</span><span class="sxs-lookup"><span data-stu-id="44c32-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="44c32-132">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="44c32-132">-LoadBalancer</span></span>
<span data-ttu-id="44c32-133">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="44c32-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="44c32-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44c32-134">-Name</span></span>
<span data-ttu-id="44c32-135">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="44c32-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="44c32-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="44c32-136">-Protocol</span></span>
<span data-ttu-id="44c32-137">Протокол TCP, UDP или ALL</span><span class="sxs-lookup"><span data-stu-id="44c32-137">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44c32-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44c32-138">-Confirm</span></span>
<span data-ttu-id="44c32-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44c32-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c32-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c32-140">-WhatIf</span></span>
<span data-ttu-id="44c32-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44c32-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c32-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44c32-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c32-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c32-143">CommonParameters</span></span>
<span data-ttu-id="44c32-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44c32-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c32-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c32-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c32-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44c32-146">INPUTS</span></span>

### <span data-ttu-id="44c32-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44c32-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="44c32-148">System. Int32 System. String System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Network, Version = 6.5.0.0, культура = Neutral, PublicKeyToken = NULL]] Microsoft. Azure. Commands. Network. remodels. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="44c32-148">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="44c32-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c32-149">OUTPUTS</span></span>

### <span data-ttu-id="44c32-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44c32-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="44c32-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="44c32-151">NOTES</span></span>

## <span data-ttu-id="44c32-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44c32-152">RELATED LINKS</span></span>
