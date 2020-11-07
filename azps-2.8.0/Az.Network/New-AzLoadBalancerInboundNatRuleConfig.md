---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6f724cb7208afb1a5f9474048b5e2dc46c17f5af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903638"
---
# <span data-ttu-id="c15d8-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c15d8-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="c15d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c15d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c15d8-103">Создание конфигурации правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c15d8-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c15d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c15d8-104">SYNTAX</span></span>

### <span data-ttu-id="c15d8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c15d8-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c15d8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c15d8-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c15d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c15d8-107">DESCRIPTION</span></span>
<span data-ttu-id="c15d8-108">Командлет **New-AzLoadBalancerInboundNatRuleConfig** создает конфигурацию правила трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="c15d8-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c15d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c15d8-109">EXAMPLES</span></span>

### <span data-ttu-id="c15d8-110">Пример 1: создание конфигурации правила входящего NAT для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="c15d8-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="c15d8-111">Первая команда создает общедоступный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="c15d8-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="c15d8-112">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет его в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="c15d8-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="c15d8-113">Третья команда создает конфигурацию правила входящего трафика NAT с именем MyInboundNatRule, используя объект переднего плана в $frontend.</span><span class="sxs-lookup"><span data-stu-id="c15d8-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="c15d8-114">Указан протокол TCP, а интерфейсный порт — 3389, то же, что и внутренний порт в данном случае.</span><span class="sxs-lookup"><span data-stu-id="c15d8-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="c15d8-115">Параметры *FrontendIpConfiguration* , *Protocol* , *FrontendPort* и *BACKENDPORT* необходимы для создания конфигурации правила входящей NAT.</span><span class="sxs-lookup"><span data-stu-id="c15d8-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="c15d8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c15d8-116">PARAMETERS</span></span>

### <span data-ttu-id="c15d8-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c15d8-117">-BackendPort</span></span>
<span data-ttu-id="c15d8-118">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="c15d8-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="c15d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15d8-119">-DefaultProfile</span></span>
<span data-ttu-id="c15d8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c15d8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c15d8-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c15d8-121">-EnableFloatingIP</span></span>
<span data-ttu-id="c15d8-122">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="c15d8-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c15d8-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c15d8-123">-EnableTcpReset</span></span>
<span data-ttu-id="c15d8-124">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="c15d8-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c15d8-125">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="c15d8-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c15d8-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c15d8-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c15d8-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c15d8-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c15d8-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c15d8-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c15d8-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c15d8-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c15d8-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c15d8-130">-FrontendPort</span></span>
<span data-ttu-id="c15d8-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c15d8-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c15d8-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c15d8-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c15d8-133">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c15d8-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c15d8-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c15d8-134">-Name</span></span>
<span data-ttu-id="c15d8-135">Указывает имя конфигурации правила, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c15d8-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c15d8-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c15d8-136">-Protocol</span></span>
<span data-ttu-id="c15d8-137">Указывает протокол.</span><span class="sxs-lookup"><span data-stu-id="c15d8-137">Specifies a protocol.</span></span>
<span data-ttu-id="c15d8-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c15d8-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c15d8-139">Номера</span><span class="sxs-lookup"><span data-stu-id="c15d8-139">Tcp</span></span>
- <span data-ttu-id="c15d8-140">Трафика</span><span class="sxs-lookup"><span data-stu-id="c15d8-140">Udp</span></span>

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

### <span data-ttu-id="c15d8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c15d8-141">-Confirm</span></span>
<span data-ttu-id="c15d8-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c15d8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c15d8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c15d8-143">-WhatIf</span></span>
<span data-ttu-id="c15d8-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c15d8-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c15d8-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c15d8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c15d8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15d8-146">CommonParameters</span></span>
<span data-ttu-id="c15d8-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c15d8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15d8-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15d8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15d8-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c15d8-149">INPUTS</span></span>

### <span data-ttu-id="c15d8-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c15d8-150">System.String</span></span>

### <span data-ttu-id="c15d8-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c15d8-151">System.Int32</span></span>

### <span data-ttu-id="c15d8-152">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c15d8-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="c15d8-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c15d8-153">OUTPUTS</span></span>

### <span data-ttu-id="c15d8-154">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="c15d8-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="c15d8-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="c15d8-155">NOTES</span></span>

## <span data-ttu-id="c15d8-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c15d8-156">RELATED LINKS</span></span>

[<span data-ttu-id="c15d8-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c15d8-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c15d8-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c15d8-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c15d8-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c15d8-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c15d8-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c15d8-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="c15d8-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c15d8-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="c15d8-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c15d8-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


