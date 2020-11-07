---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: a089f5b9e27a6fd7458dc02937a8bb75d1cbbb02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911848"
---
# <span data-ttu-id="c9d5a-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9d5a-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c9d5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d5a-103">Создание конфигурации исходящего правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c9d5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9d5a-104">SYNTAX</span></span>

### <span data-ttu-id="c9d5a-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9d5a-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9d5a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9d5a-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d5a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d5a-107">DESCRIPTION</span></span>
<span data-ttu-id="c9d5a-108">Командлет **New-AzLoadBalancerOutboundRuleConfig** создает конфигурацию исходящего правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c9d5a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9d5a-109">EXAMPLES</span></span>

### <span data-ttu-id="c9d5a-110">Пример 1: создание конфигурации исходящего правила для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="c9d5a-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="c9d5a-111">Первая команда создает общедоступный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="c9d5a-112">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет его в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="c9d5a-113">Третья команда создает конфигурацию пула конечных адресов с именем BackendAddressPool01 и сохраняет ее в переменной $backend.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="c9d5a-114">Четвертая команда создает конфигурацию исходящего правила с именем MyOutboundRule с помощью внешних и серверных объектов в $frontend и $backend.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="c9d5a-115">Для создания конфигурации исходящего правила необходимы параметры " *протокол* ", " *FrontendIPConfiguration* " и " *BackendAddressPool* ".</span><span class="sxs-lookup"><span data-stu-id="c9d5a-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="c9d5a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9d5a-116">PARAMETERS</span></span>

### <span data-ttu-id="c9d5a-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="c9d5a-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c9d5a-118">Количество исходящих портов, используемых для NAT.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="c9d5a-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c9d5a-119">-BackendAddressPool</span></span>
<span data-ttu-id="c9d5a-120">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c9d5a-121">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c9d5a-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c9d5a-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="c9d5a-123">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c9d5a-124">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c9d5a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d5a-125">-DefaultProfile</span></span>
<span data-ttu-id="c9d5a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9d5a-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c9d5a-127">-EnableTcpReset</span></span>
<span data-ttu-id="c9d5a-128">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c9d5a-129">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c9d5a-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9d5a-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c9d5a-131">IP-адреса переднего плана для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d5a-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c9d5a-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c9d5a-133">Время ожидания для подключения по протоколу бездействия TCP</span><span class="sxs-lookup"><span data-stu-id="c9d5a-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="c9d5a-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9d5a-134">-Name</span></span>
<span data-ttu-id="c9d5a-135">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c9d5a-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c9d5a-136">-Protocol</span></span>
<span data-ttu-id="c9d5a-137">Протокол TCP, UDP или ALL</span><span class="sxs-lookup"><span data-stu-id="c9d5a-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="c9d5a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9d5a-138">-Confirm</span></span>
<span data-ttu-id="c9d5a-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d5a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d5a-140">-WhatIf</span></span>
<span data-ttu-id="c9d5a-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d5a-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d5a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d5a-143">CommonParameters</span></span>
<span data-ttu-id="c9d5a-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9d5a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d5a-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d5a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d5a-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9d5a-146">INPUTS</span></span>

### <span data-ttu-id="c9d5a-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c9d5a-147">System.Int32</span></span>

### <span data-ttu-id="c9d5a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d5a-148">System.String</span></span>

### <span data-ttu-id="c9d5a-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="c9d5a-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="c9d5a-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c9d5a-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c9d5a-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9d5a-151">OUTPUTS</span></span>

### <span data-ttu-id="c9d5a-152">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="c9d5a-152">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="c9d5a-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9d5a-153">NOTES</span></span>

## <span data-ttu-id="c9d5a-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9d5a-154">RELATED LINKS</span></span>

[<span data-ttu-id="c9d5a-155">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9d5a-155">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c9d5a-156">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9d5a-156">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c9d5a-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9d5a-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c9d5a-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c9d5a-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
