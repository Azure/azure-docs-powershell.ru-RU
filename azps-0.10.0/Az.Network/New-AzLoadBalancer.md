---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: fac34080ed9b96c30c9003cef57f73f416711ac5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909706"
---
# <span data-ttu-id="4cb25-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cb25-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="4cb25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4cb25-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb25-103">Создает подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-103">Creates a load balancer.</span></span>

## <span data-ttu-id="4cb25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4cb25-104">SYNTAX</span></span>

```
New-AzLoadBalancer -Name <String> -ResourceGroupName <String> -Location <String> [-Sku <String>]
 [-FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration]>]
 [-BackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-Probe <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSProbe]>]
 [-InboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-LoadBalancingRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule]>]
 [-Tag <Hashtable>]
 [-InboundNatPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatPool]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cb25-105">DESCRIPTION</span></span>
<span data-ttu-id="4cb25-106">Командлет **New-AzLoadBalancer** создает подсистему балансировки нагрузки для Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb25-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="4cb25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4cb25-107">EXAMPLES</span></span>

### <span data-ttu-id="4cb25-108">Пример 1: Создание подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="4cb25-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="4cb25-109">Для развертывания подсистемы балансировки нагрузки необходимо сначала создать несколько объектов, а первые семь команд покажут, как создать эти объекты.</span><span class="sxs-lookup"><span data-stu-id="4cb25-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>

<span data-ttu-id="4cb25-110">Восьмая команда создает подсистему балансировки нагрузки с именем MyLoadBalancer в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4cb25-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

<span data-ttu-id="4cb25-111">Девятая и последняя команды получит новую подсистему балансировки нагрузки, чтобы убедиться, что она была успешно создана.</span><span class="sxs-lookup"><span data-stu-id="4cb25-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>

<span data-ttu-id="4cb25-112">Обратите внимание, что в этом примере показано, как создать подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="4cb25-113">Кроме того, вы должны настроить ее с помощью командлета Add-AzNetworkInterfaceIpConfig, чтобы назначить сетевые адаптеры для разных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="4cb25-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="4cb25-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4cb25-114">PARAMETERS</span></span>

### <span data-ttu-id="4cb25-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cb25-115">-AsJob</span></span>
<span data-ttu-id="4cb25-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4cb25-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cb25-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4cb25-117">-BackendAddressPool</span></span>
<span data-ttu-id="4cb25-118">Указывает пул серверных адресов, который нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-118">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4cb25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb25-119">-DefaultProfile</span></span>
<span data-ttu-id="4cb25-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4cb25-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cb25-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4cb25-121">-Force</span></span>
<span data-ttu-id="4cb25-122">Указывает на то, что этот командлет создает подсистему балансировки нагрузки, даже если уже существует подсистема балансировки нагрузки с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="4cb25-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="4cb25-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cb25-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4cb25-124">Задает список интерфейсных IP-адресов, которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4cb25-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="4cb25-125">-InboundNatPool</span></span>
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

### <span data-ttu-id="4cb25-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="4cb25-126">-InboundNatRule</span></span>
<span data-ttu-id="4cb25-127">Указывает список правил преобразования сетевых адресов (NAT), которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4cb25-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="4cb25-128">-LoadBalancingRule</span></span>
<span data-ttu-id="4cb25-129">Указывает список правил балансировки нагрузки, которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4cb25-130">-Location</span><span class="sxs-lookup"><span data-stu-id="4cb25-130">-Location</span></span>
<span data-ttu-id="4cb25-131">Указывает область, в которой нужно создать подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-131">Specifies the region in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4cb25-132">-Name</span></span>
<span data-ttu-id="4cb25-133">Указывает имя подсистемы балансировки нагрузки, создаваемой этим.</span><span class="sxs-lookup"><span data-stu-id="4cb25-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-134">-Зонд</span><span class="sxs-lookup"><span data-stu-id="4cb25-134">-Probe</span></span>
<span data-ttu-id="4cb25-135">Указывает список зондов, которые нужно связать с подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-135">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="4cb25-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb25-136">-ResourceGroupName</span></span>
<span data-ttu-id="4cb25-137">Указывает имя группы ресурсов, в которой нужно создать подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-137">Specifies the name of the resource group in which to create a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="4cb25-138">-Sku</span></span>
<span data-ttu-id="4cb25-139">Имя SKU подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4cb25-139">The load balancer Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-140">-Тег</span><span class="sxs-lookup"><span data-stu-id="4cb25-140">-Tag</span></span>
<span data-ttu-id="4cb25-141">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4cb25-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4cb25-142">Например:</span><span class="sxs-lookup"><span data-stu-id="4cb25-142">For example:</span></span>

<span data-ttu-id="4cb25-143">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4cb25-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cb25-144">-Confirm</span></span>
<span data-ttu-id="4cb25-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4cb25-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb25-146">-WhatIf</span></span>
<span data-ttu-id="4cb25-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4cb25-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cb25-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4cb25-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb25-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb25-149">CommonParameters</span></span>
<span data-ttu-id="4cb25-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4cb25-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb25-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb25-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb25-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4cb25-152">INPUTS</span></span>

## <span data-ttu-id="4cb25-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cb25-153">OUTPUTS</span></span>

### <span data-ttu-id="4cb25-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cb25-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4cb25-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="4cb25-155">NOTES</span></span>

## <span data-ttu-id="4cb25-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cb25-156">RELATED LINKS</span></span>

[<span data-ttu-id="4cb25-157">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4cb25-157">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4cb25-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cb25-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4cb25-159">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cb25-159">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="4cb25-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4cb25-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
