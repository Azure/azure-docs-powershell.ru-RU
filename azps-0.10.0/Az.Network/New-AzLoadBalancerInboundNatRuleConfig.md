---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 52aad9586840875cf63a27a8f27ff7296d080bd7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909678"
---
# <span data-ttu-id="eead3-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eead3-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="eead3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eead3-102">SYNOPSIS</span></span>
<span data-ttu-id="eead3-103">Создание конфигурации правила входящего NAT для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="eead3-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="eead3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eead3-104">SYNTAX</span></span>

### <span data-ttu-id="eead3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eead3-105">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eead3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="eead3-106">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eead3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eead3-107">DESCRIPTION</span></span>
<span data-ttu-id="eead3-108">Командлет **New-AzLoadBalancerInboundNatRuleConfig** создает конфигурацию правила трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="eead3-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="eead3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eead3-109">EXAMPLES</span></span>

### <span data-ttu-id="eead3-110">Пример 1: создание конфигурации правила входящего NAT для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="eead3-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="eead3-111">Первая команда создает общедоступный IP-адрес с именем MyPublicIP в группе ресурсов с именем MyResourceGroup и сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="eead3-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="eead3-112">Вторая команда создает клиентскую IP-конфигурацию с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет его в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="eead3-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="eead3-113">Третья команда создает конфигурацию правила входящего трафика NAT с именем MyInboundNatRule, используя объект переднего плана в $frontend.</span><span class="sxs-lookup"><span data-stu-id="eead3-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="eead3-114">Указан протокол TCP, а интерфейсный порт — 3389, то же, что и внутренний порт в данном случае.</span><span class="sxs-lookup"><span data-stu-id="eead3-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="eead3-115">Параметры *FrontendIpConfiguration* , *Procotol* , *FrontendPort* и *BACKENDPORT* необходимы для создания конфигурации правила входящей NAT.</span><span class="sxs-lookup"><span data-stu-id="eead3-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="eead3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eead3-116">PARAMETERS</span></span>

### <span data-ttu-id="eead3-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="eead3-117">-BackendPort</span></span>
<span data-ttu-id="eead3-118">Указывает внутренний порт для трафика, соответствующего данной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="eead3-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="eead3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eead3-119">-DefaultProfile</span></span>
<span data-ttu-id="eead3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eead3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eead3-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="eead3-121">-EnableFloatingIP</span></span>
<span data-ttu-id="eead3-122">Указывает на то, что этот командлет включает плавающий IP-адрес для конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="eead3-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="eead3-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="eead3-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="eead3-124">Задает список IP-адресов интерфейсов, которые нужно связать с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="eead3-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="eead3-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="eead3-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="eead3-126">Указывает идентификатор конфигурации интерфейсаный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="eead3-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="eead3-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="eead3-127">-FrontendPort</span></span>
<span data-ttu-id="eead3-128">Указывает порт переднего плана, совпадающий с конфигурацией правила подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="eead3-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="eead3-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="eead3-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="eead3-130">Указывает интервал времени (в минутах), в течение которого состояние бесед сохраняется в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="eead3-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="eead3-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eead3-131">-Name</span></span>
<span data-ttu-id="eead3-132">Указывает имя конфигурации правила, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eead3-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="eead3-133">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="eead3-133">-Protocol</span></span>
<span data-ttu-id="eead3-134">Указывает протокол.</span><span class="sxs-lookup"><span data-stu-id="eead3-134">Specifies a protocol.</span></span>
<span data-ttu-id="eead3-135">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eead3-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eead3-136">Номера</span><span class="sxs-lookup"><span data-stu-id="eead3-136">Tcp</span></span>
- <span data-ttu-id="eead3-137">Трафика</span><span class="sxs-lookup"><span data-stu-id="eead3-137">Udp</span></span>

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

### <span data-ttu-id="eead3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eead3-138">CommonParameters</span></span>
<span data-ttu-id="eead3-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eead3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eead3-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eead3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eead3-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eead3-141">INPUTS</span></span>

## <span data-ttu-id="eead3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eead3-142">OUTPUTS</span></span>

### <span data-ttu-id="eead3-143">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="eead3-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="eead3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="eead3-144">NOTES</span></span>

## <span data-ttu-id="eead3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eead3-145">RELATED LINKS</span></span>

[<span data-ttu-id="eead3-146">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eead3-146">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="eead3-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eead3-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="eead3-148">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="eead3-148">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="eead3-149">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="eead3-149">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="eead3-150">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eead3-150">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="eead3-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eead3-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


