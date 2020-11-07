---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b02b2abec8138170d574492c8429f463fc6a28a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732795"
---
# <span data-ttu-id="9d041-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d041-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9d041-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d041-102">SYNOPSIS</span></span>
<span data-ttu-id="9d041-103">Создание конфигурации правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9d041-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d041-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d041-104">SYNTAX</span></span>

### <span data-ttu-id="9d041-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d041-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d041-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d041-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d041-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d041-107">DESCRIPTION</span></span>
<span data-ttu-id="9d041-108">Командлет **New-AzureRmLoadBalancerInboundNatRuleConfig** создает конфигурацию правила трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9d041-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9d041-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d041-109">EXAMPLES</span></span>

### <span data-ttu-id="9d041-110">Пример 1: создание конфигурации правила входящего NAT для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="9d041-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="9d041-111">Первая команда создает общедоступный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="9d041-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="9d041-112">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет его в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="9d041-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="9d041-113">Третья команда создает конфигурацию правила входящего трафика NAT с именем MyInboundNatRule, используя объект переднего плана в $frontend.</span><span class="sxs-lookup"><span data-stu-id="9d041-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="9d041-114">Указан протокол TCP, а интерфейсный порт — 3389, то же, что и внутренний порт в данном случае.</span><span class="sxs-lookup"><span data-stu-id="9d041-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="9d041-115">Параметры *FrontendIpConfiguration* , *Procotol* , *FrontendPort* и *BACKENDPORT* необходимы для создания конфигурации правила входящей NAT.</span><span class="sxs-lookup"><span data-stu-id="9d041-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="9d041-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d041-116">PARAMETERS</span></span>

### <span data-ttu-id="9d041-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9d041-117">-BackendPort</span></span>
<span data-ttu-id="9d041-118">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="9d041-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="9d041-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d041-119">-DefaultProfile</span></span>
<span data-ttu-id="9d041-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d041-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d041-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9d041-121">-EnableFloatingIP</span></span>
<span data-ttu-id="9d041-122">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="9d041-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9d041-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9d041-123">-EnableTcpReset</span></span>
<span data-ttu-id="9d041-124">Получение межпортового TCP-сброса в течение тайм-аута простоя потока TCP или неожиданного завершения подключения.</span><span class="sxs-lookup"><span data-stu-id="9d041-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9d041-125">Этот элемент используется только в том случае, если для протокола задано значение TCP.</span><span class="sxs-lookup"><span data-stu-id="9d041-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9d041-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d041-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9d041-127">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9d041-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9d041-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9d041-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9d041-129">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="9d041-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9d041-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9d041-130">-FrontendPort</span></span>
<span data-ttu-id="9d041-131">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9d041-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="9d041-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9d041-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9d041-133">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9d041-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="9d041-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d041-134">-Name</span></span>
<span data-ttu-id="9d041-135">Указывает имя конфигурации правила, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9d041-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9d041-136">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9d041-136">-Protocol</span></span>
<span data-ttu-id="9d041-137">Указывает протокол.</span><span class="sxs-lookup"><span data-stu-id="9d041-137">Specifies a protocol.</span></span>
<span data-ttu-id="9d041-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9d041-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d041-139">Номера</span><span class="sxs-lookup"><span data-stu-id="9d041-139">Tcp</span></span>
- <span data-ttu-id="9d041-140">Трафика</span><span class="sxs-lookup"><span data-stu-id="9d041-140">Udp</span></span>

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

### <span data-ttu-id="9d041-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d041-141">-Confirm</span></span>
<span data-ttu-id="9d041-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d041-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d041-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d041-143">-WhatIf</span></span>
<span data-ttu-id="9d041-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d041-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d041-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d041-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d041-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d041-146">CommonParameters</span></span>
<span data-ttu-id="9d041-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d041-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d041-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d041-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d041-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d041-149">INPUTS</span></span>

### <span data-ttu-id="9d041-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="9d041-150">None</span></span>

## <span data-ttu-id="9d041-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d041-151">OUTPUTS</span></span>

### <span data-ttu-id="9d041-152">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="9d041-152">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="9d041-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d041-153">NOTES</span></span>

## <span data-ttu-id="9d041-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d041-154">RELATED LINKS</span></span>

[<span data-ttu-id="9d041-155">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d041-155">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d041-156">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d041-156">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d041-157">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9d041-157">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="9d041-158">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9d041-158">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9d041-159">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d041-159">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9d041-160">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9d041-160">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


