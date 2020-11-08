---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079473"
---
# <span data-ttu-id="da5e5-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da5e5-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="da5e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="da5e5-103">Создание конфигурации исходящего правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="da5e5-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="da5e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da5e5-104">SYNTAX</span></span>

### <span data-ttu-id="da5e5-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da5e5-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da5e5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da5e5-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da5e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da5e5-107">DESCRIPTION</span></span>
<span data-ttu-id="da5e5-108">Командлет **New-AzLoadBalancerOutboundRuleConfig** создает конфигурацию исходящего правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="da5e5-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="da5e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da5e5-109">EXAMPLES</span></span>

### <span data-ttu-id="da5e5-110">Пример 1: создание конфигурации исходящего правила для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="da5e5-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="da5e5-111">Первая команда создает общедоступный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="da5e5-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="da5e5-112">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет его в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="da5e5-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="da5e5-113">Третья команда создает конфигурацию пула конечных адресов с именем BackendAddressPool01 и сохраняет ее в переменной $backend.</span><span class="sxs-lookup"><span data-stu-id="da5e5-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="da5e5-114">Четвертая команда создает конфигурацию исходящего правила с именем MyOutboundRule с помощью внешних и серверных объектов в $frontend и $backend.</span><span class="sxs-lookup"><span data-stu-id="da5e5-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="da5e5-115">Для создания конфигурации исходящего правила необходимы параметры " *протокол* ", " *FrontendIPConfiguration* " и " *BackendAddressPool* ".</span><span class="sxs-lookup"><span data-stu-id="da5e5-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="da5e5-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="da5e5-116">Example 2</span></span>

<span data-ttu-id="da5e5-117">Создание конфигурации исходящего правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="da5e5-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="da5e5-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="da5e5-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="da5e5-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da5e5-119">PARAMETERS</span></span>

### <span data-ttu-id="da5e5-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="da5e5-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="da5e5-121">Количество исходящих портов, используемых для NAT.</span><span class="sxs-lookup"><span data-stu-id="da5e5-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="da5e5-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da5e5-122">-BackendAddressPool</span></span>
<span data-ttu-id="da5e5-123">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="da5e5-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="da5e5-124">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="da5e5-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="da5e5-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="da5e5-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="da5e5-126">Ссылка на пул DIP.</span><span class="sxs-lookup"><span data-stu-id="da5e5-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="da5e5-127">Исходящий трафик по каналам IP в адресах IP внутренней нагрузки проходит случайным образом.</span><span class="sxs-lookup"><span data-stu-id="da5e5-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="da5e5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5e5-128">-DefaultProfile</span></span>
<span data-ttu-id="da5e5-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da5e5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da5e5-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="da5e5-130">-EnableTcpReset</span></span>
<span data-ttu-id="da5e5-131">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="da5e5-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="da5e5-132">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="da5e5-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="da5e5-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="da5e5-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="da5e5-134">IP-адреса переднего плана для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="da5e5-134">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="da5e5-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="da5e5-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="da5e5-136">Время ожидания для подключения по протоколу бездействия TCP</span><span class="sxs-lookup"><span data-stu-id="da5e5-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="da5e5-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da5e5-137">-Name</span></span>
<span data-ttu-id="da5e5-138">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="da5e5-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="da5e5-139">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="da5e5-139">-Protocol</span></span>
<span data-ttu-id="da5e5-140">Протокол TCP, UDP или ALL</span><span class="sxs-lookup"><span data-stu-id="da5e5-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="da5e5-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da5e5-141">-Confirm</span></span>
<span data-ttu-id="da5e5-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da5e5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da5e5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da5e5-143">-WhatIf</span></span>
<span data-ttu-id="da5e5-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da5e5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da5e5-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da5e5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da5e5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5e5-146">CommonParameters</span></span>
<span data-ttu-id="da5e5-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da5e5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5e5-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da5e5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5e5-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da5e5-149">INPUTS</span></span>

### <span data-ttu-id="da5e5-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="da5e5-150">System.Int32</span></span>

### <span data-ttu-id="da5e5-151">System. String</span><span class="sxs-lookup"><span data-stu-id="da5e5-151">System.String</span></span>

### <span data-ttu-id="da5e5-152">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="da5e5-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="da5e5-153">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da5e5-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="da5e5-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da5e5-154">OUTPUTS</span></span>

### <span data-ttu-id="da5e5-155">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="da5e5-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="da5e5-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="da5e5-156">NOTES</span></span>

## <span data-ttu-id="da5e5-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da5e5-157">RELATED LINKS</span></span>

[<span data-ttu-id="da5e5-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da5e5-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="da5e5-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da5e5-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="da5e5-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da5e5-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="da5e5-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da5e5-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
