---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: 9608dfd5a780006d2ab050a1ca2e85ee26949f97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961731"
---
# <span data-ttu-id="ef07a-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ef07a-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="ef07a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef07a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef07a-103">Создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ef07a-103">Creates a virtual network.</span></span>

## <span data-ttu-id="ef07a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef07a-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef07a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef07a-105">DESCRIPTION</span></span>
<span data-ttu-id="ef07a-106">Командлет **New-AzVirtualNetwork** создает виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="ef07a-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="ef07a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef07a-107">EXAMPLES</span></span>

### <span data-ttu-id="ef07a-108">Пример 1. Создание виртуальной сети с двумя подсетями</span><span class="sxs-lookup"><span data-stu-id="ef07a-108">Example 1: Create a virtual network with two subnets</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="ef07a-109">В этом примере создается виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="ef07a-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="ef07a-110">Во-первых, в центральном регионе создается новая группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef07a-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="ef07a-111">Затем в этом примере в памяти создаются представления двух подсетей.</span><span class="sxs-lookup"><span data-stu-id="ef07a-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="ef07a-112">С New-AzVirtualNetworkSubnetConfig не будет создаваться подсеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="ef07a-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="ef07a-113">Существует одна подсеть подсети под названием frontendSubnet, а одна — backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="ef07a-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="ef07a-114">Затем New-AzVirtualNetwork создает виртуальную сеть с использованием CIDR 10.0.0.0/16 в качестве префикса адреса и двух подсетей.</span><span class="sxs-lookup"><span data-stu-id="ef07a-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="ef07a-115">Пример 2. Создание виртуальной сети с помощью параметров DNS</span><span class="sxs-lookup"><span data-stu-id="ef07a-115">Example 2: Create a virtual network with DNS settings</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="ef07a-116">В этом примере создается виртуальная сеть с двумя подсетями и двумя DNS-серверами.</span><span class="sxs-lookup"><span data-stu-id="ef07a-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="ef07a-117">В результате настройки DNS-серверов в виртуальной сети развертывание в этой виртуальной сети наследуют эти DNS-серверы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef07a-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="ef07a-118">Эти значения по умолчанию можно перезаписать для NIC с помощью параметра уровня NIC.</span><span class="sxs-lookup"><span data-stu-id="ef07a-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="ef07a-119">Если на VNET не указаны DNS-серверы и ни один из них, для разрешения DNS используются стандартные DNS-серверы Azure.</span><span class="sxs-lookup"><span data-stu-id="ef07a-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="ef07a-120">Пример 3. Создание виртуальной сети с подсетей, ссылаемой на группу безопасности сети</span><span class="sxs-lookup"><span data-stu-id="ef07a-120">Example 3: Create a virtual network with a subnet referencing a network security group</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="ef07a-121">В этом примере создается виртуальная сеть с подсетями, которые ссылались на группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ef07a-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="ef07a-122">Во-первых, в примере создается группа ресурсов в качестве контейнера для созданных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef07a-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="ef07a-123">Затем создается группа безопасности сети, которая обеспечивает входящий доступ к RDP, но в противном случае применяет правила группы безопасности сети по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef07a-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="ef07a-124">Затем New-AzVirtualNetworkSubnetConfig создает в памяти представления двух подсетей, ссылаясь на созданную группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ef07a-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="ef07a-125">После New-AzVirtualNetwork создается виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="ef07a-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="ef07a-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef07a-126">PARAMETERS</span></span>

### <span data-ttu-id="ef07a-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ef07a-127">-AddressPrefix</span></span>
<span data-ttu-id="ef07a-128">Диапазон IP-адресов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef07a-128">Specifies a range of IP addresses for a virtual network.</span></span>

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

### <span data-ttu-id="ef07a-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef07a-129">-AsJob</span></span>
<span data-ttu-id="ef07a-130">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ef07a-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef07a-131">-BgpCommunity</span><span class="sxs-lookup"><span data-stu-id="ef07a-131">-BgpCommunity</span></span>
<span data-ttu-id="ef07a-132">Сообщество BGP, объявляемая через ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ef07a-132">The BGP Community advertised over ExpressRoute.</span></span>

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

### <span data-ttu-id="ef07a-133">-DdosProtectionPlanId</span><span class="sxs-lookup"><span data-stu-id="ef07a-133">-DdosProtectionPlanId</span></span>
<span data-ttu-id="ef07a-134">Ссылка на ресурс плана защиты DDoS, связанный с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="ef07a-134">Reference to the DDoS protection plan resource associated with the virtual network.</span></span>

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

### <span data-ttu-id="ef07a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef07a-135">-DefaultProfile</span></span>
<span data-ttu-id="ef07a-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef07a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef07a-137">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="ef07a-137">-DnsServer</span></span>
<span data-ttu-id="ef07a-138">Указывает DNS-сервер подсети.</span><span class="sxs-lookup"><span data-stu-id="ef07a-138">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="ef07a-139">-EnableDdosProtection</span><span class="sxs-lookup"><span data-stu-id="ef07a-139">-EnableDdosProtection</span></span>
<span data-ttu-id="ef07a-140">Переключатель, который представляет, включена ли защита DDoS.</span><span class="sxs-lookup"><span data-stu-id="ef07a-140">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

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

### <span data-ttu-id="ef07a-141">-Force</span><span class="sxs-lookup"><span data-stu-id="ef07a-141">-Force</span></span>
<span data-ttu-id="ef07a-142">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ef07a-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef07a-143">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="ef07a-143">-IpAllocation</span></span>
<span data-ttu-id="ef07a-144">IpAllocations для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef07a-144">Specifies IpAllocations for a virtual network.</span></span>

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

### <span data-ttu-id="ef07a-145">-Location</span><span class="sxs-lookup"><span data-stu-id="ef07a-145">-Location</span></span>
<span data-ttu-id="ef07a-146">Определяет регион для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef07a-146">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="ef07a-147">-Name</span><span class="sxs-lookup"><span data-stu-id="ef07a-147">-Name</span></span>
<span data-ttu-id="ef07a-148">Указывает имя виртуальной сети, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef07a-148">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ef07a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef07a-149">-ResourceGroupName</span></span>
<span data-ttu-id="ef07a-150">Имя группы ресурсов, которая должна содержать виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="ef07a-150">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="ef07a-151">-Subnet</span><span class="sxs-lookup"><span data-stu-id="ef07a-151">-Subnet</span></span>
<span data-ttu-id="ef07a-152">Список подсетей, которые нужно связать с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="ef07a-152">Specifies a list of subnets to associate with the virtual network.</span></span>

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

### <span data-ttu-id="ef07a-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef07a-153">-Tag</span></span>
<span data-ttu-id="ef07a-154">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="ef07a-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ef07a-155">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ef07a-155">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ef07a-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef07a-156">-Confirm</span></span>
<span data-ttu-id="ef07a-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef07a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef07a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef07a-158">-WhatIf</span></span>
<span data-ttu-id="ef07a-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef07a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef07a-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef07a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef07a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef07a-161">CommonParameters</span></span>
<span data-ttu-id="ef07a-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef07a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef07a-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef07a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef07a-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef07a-164">INPUTS</span></span>

### <span data-ttu-id="ef07a-165">System.String</span><span class="sxs-lookup"><span data-stu-id="ef07a-165">System.String</span></span>

### <span data-ttu-id="ef07a-166">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ef07a-166">System.String[]</span></span>

### <span data-ttu-id="ef07a-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span><span class="sxs-lookup"><span data-stu-id="ef07a-167">Microsoft.Azure.Commands.Network.Models.PSSubnet[]</span></span>

### <span data-ttu-id="ef07a-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ef07a-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ef07a-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef07a-169">OUTPUTS</span></span>

### <span data-ttu-id="ef07a-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ef07a-170">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="ef07a-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef07a-171">NOTES</span></span>

## <span data-ttu-id="ef07a-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef07a-172">RELATED LINKS</span></span>

[<span data-ttu-id="ef07a-173">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ef07a-173">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="ef07a-174">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ef07a-174">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="ef07a-175">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ef07a-175">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="ef07a-176">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="ef07a-176">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)
