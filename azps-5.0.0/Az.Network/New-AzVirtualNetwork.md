---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248524"
---
# <span data-ttu-id="a4175-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4175-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="a4175-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4175-102">SYNOPSIS</span></span>
<span data-ttu-id="a4175-103">Создание виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a4175-103">Creates a virtual network.</span></span>

## <span data-ttu-id="a4175-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4175-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4175-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4175-105">DESCRIPTION</span></span>
<span data-ttu-id="a4175-106">Командлет **New-AzVirtualNetwork** создает виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="a4175-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="a4175-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4175-107">EXAMPLES</span></span>

### <span data-ttu-id="a4175-108">Пример 1: создание виртуальной сети с двумя подсетями</span><span class="sxs-lookup"><span data-stu-id="a4175-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="a4175-109">В этом примере создается виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="a4175-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="a4175-110">Сначала создается новая группа ресурсов в области centralus.</span><span class="sxs-lookup"><span data-stu-id="a4175-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="a4175-111">Затем в примере создаются представления двух подсетей в памяти.</span><span class="sxs-lookup"><span data-stu-id="a4175-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="a4175-112">Командлет New-AzVirtualNetworkSubnetConfig не создаст подсеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a4175-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="a4175-113">Одна подсеть называется frontendSubnet и одной подсетью под названием backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="a4175-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="a4175-114">Затем командлет New-AzVirtualNetwork создает виртуальную сеть, используя CIDR 10.0.0.0/16 в качестве префикса адреса и двух подсетей.</span><span class="sxs-lookup"><span data-stu-id="a4175-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="a4175-115">Пример 2: создание виртуальной сети с параметрами DNS</span><span class="sxs-lookup"><span data-stu-id="a4175-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="a4175-116">В этом примере создается виртуальная сеть с двумя подсетями и двумя DNS-серверами.</span><span class="sxs-lookup"><span data-stu-id="a4175-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="a4175-117">Результат задания DNS-серверов в виртуальной сети заключается в том, что сетевые адаптеры и виртуальные машины, развернутые в этой виртуальной сети, наследуют эти DNS-серверы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4175-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="a4175-118">Эти значения по умолчанию могут быть заменены на NIC с помощью параметра уровня NIC.</span><span class="sxs-lookup"><span data-stu-id="a4175-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="a4175-119">Если в виртуальной сети не указаны DNS-серверы и DNS-серверы на сетевых адаптерах, то для разрешения DNS используются DNS-серверы Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4175-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="a4175-120">Пример 3: создание виртуальной сети с подсетью, ссылающейся на сетевую группу безопасности</span><span class="sxs-lookup"><span data-stu-id="a4175-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="a4175-121">В этом примере создается виртуальная сеть с подсетями, которые ссылаются на сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="a4175-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="a4175-122">Сначала в примере создается группа ресурсов в качестве контейнера для ресурсов, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="a4175-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="a4175-123">Затем создается группа безопасности сети, разрешающая входящий доступ к удаленному рабочему столу, но в противном случае принудительно применяет правила групповой безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4175-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="a4175-124">Затем командлет New-AzVirtualNetworkSubnetConfig создает в памяти одновременные представления двух подсетей, которые ссылаются на созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="a4175-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="a4175-125">Затем команда New-AzVirtualNetwork создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a4175-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="a4175-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4175-126">PARAMETERS</span></span>

### <span data-ttu-id="a4175-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a4175-127">-AddressPrefix</span></span>
<span data-ttu-id="a4175-128">Указывает диапазон IP-адресов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a4175-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4175-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4175-129">-AsJob</span></span>
<span data-ttu-id="a4175-130">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a4175-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4175-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="a4175-131">-BgpCommunity</span></span>
<span data-ttu-id="a4175-132">Сообщество BGP, объявленное через ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a4175-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="a4175-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="a4175-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="a4175-134">Ссылка на ресурс плана защиты Distributed, связанный с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="a4175-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="a4175-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4175-135">-DefaultProfile</span></span>
<span data-ttu-id="a4175-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4175-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4175-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="a4175-137">-DnsServer</span></span>
<span data-ttu-id="a4175-138">Указывает DNS-сервер для подсети.</span><span class="sxs-lookup"><span data-stu-id="a4175-138">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4175-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="a4175-139">-EnableDdosProtection</span></span>
<span data-ttu-id="a4175-140">Параметр Switch, обозначающий, включена ли защита Distributed или нет.</span><span class="sxs-lookup"><span data-stu-id="a4175-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4175-141">-Force</span><span class="sxs-lookup"><span data-stu-id="a4175-141">-Force</span></span>
<span data-ttu-id="a4175-142">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4175-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4175-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="a4175-143">-IpAllocation</span></span>
<span data-ttu-id="a4175-144">Указывает IpAllocations для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a4175-144">Specifies IpAllocations for a virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4175-145">-Location</span><span class="sxs-lookup"><span data-stu-id="a4175-145">-Location</span></span>
<span data-ttu-id="a4175-146">Указывает регион для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a4175-146">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="a4175-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4175-147">-Name</span></span>
<span data-ttu-id="a4175-148">Указывает имя виртуальной сети, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a4175-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a4175-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4175-149">-ResourceGroupName</span></span>
<span data-ttu-id="a4175-150">Указывает имя группы ресурсов, которая будет содержать виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a4175-150">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="a4175-151">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="a4175-151">-Subnet</span></span>
<span data-ttu-id="a4175-152">Указывает список подсетей, которые нужно связать с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="a4175-152">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4175-153">-Тег</span><span class="sxs-lookup"><span data-stu-id="a4175-153">-Tag</span></span>
<span data-ttu-id="a4175-154">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a4175-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a4175-155">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a4175-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a4175-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4175-156">-Confirm</span></span>
<span data-ttu-id="a4175-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4175-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4175-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4175-158">-WhatIf</span></span>
<span data-ttu-id="a4175-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4175-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4175-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4175-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4175-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4175-161">CommonParameters</span></span>
<span data-ttu-id="a4175-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4175-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4175-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4175-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4175-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4175-164">INPUTS</span></span>

### <span data-ttu-id="a4175-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a4175-165">System.String</span></span>

### <span data-ttu-id="a4175-166">System. String []</span><span class="sxs-lookup"><span data-stu-id="a4175-166">System.String[]</span></span>

### <span data-ttu-id="a4175-167">Microsoft. Azure. Commands. Network. Models. PSSubnet []</span><span class="sxs-lookup"><span data-stu-id="a4175-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="a4175-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a4175-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a4175-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4175-169">OUTPUTS</span></span>

### <span data-ttu-id="a4175-170">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4175-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a4175-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4175-171">NOTES</span></span>

## <span data-ttu-id="a4175-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4175-172">RELATED LINKS</span></span>

[<span data-ttu-id="a4175-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4175-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="a4175-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4175-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="a4175-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a4175-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="a4175-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="a4175-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
