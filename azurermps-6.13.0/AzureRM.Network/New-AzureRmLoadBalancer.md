---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancer.md
ms.openlocfilehash: db7d531b83dabe3bb5fc9dc79d86c3153d1553a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734929"
---
# <span data-ttu-id="4ec73-101">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ec73-101">New-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="4ec73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ec73-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec73-103">Создает подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-103">Creates a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ec73-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-OutboundRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ec73-105">DESCRIPTION</span></span>
<span data-ttu-id="4ec73-106">Командлет **New-AzureRmLoadBalancer** создает подсистему балансировки нагрузки для Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec73-106">The **New-AzureRmLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="4ec73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ec73-107">EXAMPLES</span></span>

### <span data-ttu-id="4ec73-108">Пример 1: Создание подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="4ec73-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4ec73-109">Для развертывания подсистемы балансировки нагрузки необходимо сначала создать несколько объектов, а первые семь команд покажут, как создать эти объекты.</span><span class="sxs-lookup"><span data-stu-id="4ec73-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="4ec73-110">Восьмая команда создает подсистему балансировки нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4ec73-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="4ec73-111">Девятая и последняя команды получит новую подсистему балансировки нагрузки, чтобы убедиться, что она была успешно создана.</span><span class="sxs-lookup"><span data-stu-id="4ec73-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="4ec73-112">Обратите внимание, что в этом примере показано, как создать подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="4ec73-113">Кроме того, вы должны настроить ее с помощью командлета Add-AzureRmNetworkInterfaceIpConfig, чтобы назначить сетевые адаптеры для разных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="4ec73-113">You must also configure it using the Add-AzureRmNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="4ec73-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ec73-114">PARAMETERS</span></span>

### <span data-ttu-id="4ec73-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ec73-115">-AsJob</span></span>
<span data-ttu-id="4ec73-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ec73-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ec73-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4ec73-117">-BackendAddressPool</span></span>
<span data-ttu-id="4ec73-118">Указывает пул серверных адресов, который нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec73-119">-DefaultProfile</span></span>
<span data-ttu-id="4ec73-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ec73-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ec73-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4ec73-121">-Force</span></span>
<span data-ttu-id="4ec73-122">Указывает на то, что этот командлет создает подсистему балансировки нагрузки, даже если уже существует подсистема балансировки нагрузки с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="4ec73-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="4ec73-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ec73-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4ec73-124">Задает список интерфейсных IP-адресов, которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="4ec73-125">-InboundNatPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="4ec73-126">-InboundNatRule</span></span>
<span data-ttu-id="4ec73-127">Указывает список правил преобразования сетевых адресов (NAT), которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="4ec73-128">-LoadBalancingRule</span></span>
<span data-ttu-id="4ec73-129">Указывает список правил балансировки нагрузки, которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-130">-Location</span><span class="sxs-lookup"><span data-stu-id="4ec73-130">-Location</span></span>
<span data-ttu-id="4ec73-131">Указывает область, в которой нужно создать подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="4ec73-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ec73-132">-Name</span></span>
<span data-ttu-id="4ec73-133">Указывает имя подсистемы балансировки нагрузки, создаваемой этим.</span><span class="sxs-lookup"><span data-stu-id="4ec73-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="4ec73-134">-OutboundRule</span></span>
<span data-ttu-id="4ec73-135">Исходящие правила.</span><span class="sxs-lookup"><span data-stu-id="4ec73-135">The outbound rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSOutboundRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-136">-Зонд</span><span class="sxs-lookup"><span data-stu-id="4ec73-136">-Probe</span></span>
<span data-ttu-id="4ec73-137">Указывает список зондов, которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec73-138">-ResourceGroupName</span></span>
<span data-ttu-id="4ec73-139">Указывает имя группы ресурсов, в которой нужно создать подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="4ec73-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="4ec73-140">-Sku</span></span>
<span data-ttu-id="4ec73-141">Имя SKU подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ec73-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="4ec73-142">-Тег</span><span class="sxs-lookup"><span data-stu-id="4ec73-142">-Tag</span></span>
<span data-ttu-id="4ec73-143">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ec73-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ec73-144">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4ec73-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ec73-145">-Confirm</span></span>
<span data-ttu-id="4ec73-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ec73-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec73-147">-WhatIf</span></span>
<span data-ttu-id="4ec73-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ec73-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec73-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ec73-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec73-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec73-150">CommonParameters</span></span>
<span data-ttu-id="4ec73-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ec73-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec73-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec73-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec73-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ec73-153">INPUTS</span></span>

### <span data-ttu-id="4ec73-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4ec73-154">System.String</span></span>

### <span data-ttu-id="4ec73-155">System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Networking. Models. PSFrontendIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4ec73-155">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ec73-156">System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Networking. Models. PSBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4ec73-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ec73-157">System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Networking. Models. PSProbe, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4ec73-157">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ec73-158">System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Networking. Models. PSInboundNatRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4ec73-158">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ec73-159">System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Networking. Models. PSLoadBalancingRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4ec73-159">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ec73-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ec73-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4ec73-161">System. Collections. Generic. List \` 1 [[Microsoft. Azure. Commands. Networking. Models. PSInboundNatPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="4ec73-161">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4ec73-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ec73-162">OUTPUTS</span></span>

### <span data-ttu-id="4ec73-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ec73-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4ec73-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ec73-164">NOTES</span></span>

## <span data-ttu-id="4ec73-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ec73-165">RELATED LINKS</span></span>

[<span data-ttu-id="4ec73-166">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4ec73-166">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4ec73-167">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ec73-167">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4ec73-168">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ec73-168">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="4ec73-169">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ec73-169">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)
