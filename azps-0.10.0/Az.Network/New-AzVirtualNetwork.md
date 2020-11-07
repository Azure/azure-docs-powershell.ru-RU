---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: c1a8381bd7f8172d972092e0a95bf2b50c6bd585
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909614"
---
# <span data-ttu-id="aa4dc-101">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa4dc-101">New-AzVirtualNetwork</span></span>

## <span data-ttu-id="aa4dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4dc-103">Создание виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-103">Creates a virtual network.</span></span>

## <span data-ttu-id="aa4dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa4dc-104">SYNTAX</span></span>

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa4dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa4dc-105">DESCRIPTION</span></span>
<span data-ttu-id="aa4dc-106">Командлет **New-AzVirtualNetwork** создает виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-106">The **New-AzVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="aa4dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa4dc-107">EXAMPLES</span></span>

### <span data-ttu-id="aa4dc-108">1: создание виртуальной сети с двумя подсетями</span><span class="sxs-lookup"><span data-stu-id="aa4dc-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="aa4dc-109">В этом примере создается виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="aa4dc-110">Сначала создается новая группа ресурсов в области centralus.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="aa4dc-111">Затем в примере создаются представления двух подсетей в памяти.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="aa4dc-112">Командлет New-AzVirtualNetworkSubnetConfig не создаст подсеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-112">The New-AzVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="aa4dc-113">Одна подсеть называется frontendSubnet и одной подсетью под названием backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="aa4dc-114">Затем командлет New-AzVirtualNetwork создает виртуальную сеть, используя CIDR 10.0.0.0/16 в качестве префикса адреса и двух подсетей.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-114">The New-AzVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="aa4dc-115">2. Создание виртуальной сети с помощью параметров DNS</span><span class="sxs-lookup"><span data-stu-id="aa4dc-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="aa4dc-116">В этом примере создается виртуальная сеть с двумя подсетями и двумя DNS-серверами.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="aa4dc-117">Результат задания DNS-серверов в виртуальной сети заключается в том, что сетевые адаптеры и виртуальные машины, развернутые в этой виртуальной сети, наследуют эти DNS-серверы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="aa4dc-118">Эти значения по умолчанию могут быть заменены на NIC с помощью параметра уровня NIC.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="aa4dc-119">Если в виртуальной сети не указаны DNS-серверы и DNS-серверы на сетевых адаптерах, то для разрешения DNS используются DNS-серверы Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="aa4dc-120">3. Создание виртуальной сети с подсетью, ссылающейся на сетевую группу безопасности</span><span class="sxs-lookup"><span data-stu-id="aa4dc-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="aa4dc-121">В этом примере создается виртуальная сеть с подсетями, которые ссылаются на сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="aa4dc-122">Сначала в примере создается группа ресурсов в качестве контейнера для ресурсов, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="aa4dc-123">Затем создается группа безопасности сети, разрешающая входящий доступ к удаленному рабочему столу, но в противном случае принудительно применяет правила групповой безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="aa4dc-124">Затем командлет New-AzVirtualNetworkSubnetConfig создает в памяти одновременные представления двух подсетей, которые ссылаются на созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-124">The New-AzVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="aa4dc-125">Затем команда New-AzVirtualNetwork создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-125">The New-AzVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="aa4dc-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa4dc-126">PARAMETERS</span></span>

### <span data-ttu-id="aa4dc-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aa4dc-127">-AddressPrefix</span></span>
<span data-ttu-id="aa4dc-128">Указывает диапазон IP-адресов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4dc-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa4dc-129">-AsJob</span></span>
<span data-ttu-id="aa4dc-130">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa4dc-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa4dc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4dc-131">-DefaultProfile</span></span>
<span data-ttu-id="aa4dc-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa4dc-133">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="aa4dc-133">-DnsServer</span></span>
<span data-ttu-id="aa4dc-134">Указывает DNS-сервер для подсети.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-134">Specifies the DNS server for a subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4dc-135">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="aa4dc-135">-EnableDDoSProtection</span></span>
<span data-ttu-id="aa4dc-136">Параметр Switch, обозначающий, включена ли защита Distributed или нет.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-136">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4dc-137">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="aa4dc-137">-EnableVmProtection</span></span>
<span data-ttu-id="aa4dc-138">Параметр переключателя, который обозначает, включена ли защита виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-138">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4dc-139">-Force</span><span class="sxs-lookup"><span data-stu-id="aa4dc-139">-Force</span></span>
<span data-ttu-id="aa4dc-140">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa4dc-141">-Location</span><span class="sxs-lookup"><span data-stu-id="aa4dc-141">-Location</span></span>
<span data-ttu-id="aa4dc-142">Указывает регион для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-142">Specifies the region for the virtual network.</span></span>

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

### <span data-ttu-id="aa4dc-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa4dc-143">-Name</span></span>
<span data-ttu-id="aa4dc-144">Указывает имя виртуальной сети, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-144">Specifies the name of the virtual network that this cmdlet creates.</span></span>

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

### <span data-ttu-id="aa4dc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa4dc-145">-ResourceGroupName</span></span>
<span data-ttu-id="aa4dc-146">Указывает имя группы ресурсов, которая будет содержать виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-146">Specifies the name of a resource group to contain the virtual network.</span></span>

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

### <span data-ttu-id="aa4dc-147">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="aa4dc-147">-Subnet</span></span>
<span data-ttu-id="aa4dc-148">Указывает список подсетей, которые нужно связать с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-148">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4dc-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="aa4dc-149">-Tag</span></span>
<span data-ttu-id="aa4dc-150">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aa4dc-151">Например:</span><span class="sxs-lookup"><span data-stu-id="aa4dc-151">For example:</span></span>

<span data-ttu-id="aa4dc-152">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="aa4dc-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aa4dc-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa4dc-153">-Confirm</span></span>
<span data-ttu-id="aa4dc-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa4dc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa4dc-155">-WhatIf</span></span>
<span data-ttu-id="aa4dc-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa4dc-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa4dc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4dc-158">CommonParameters</span></span>
<span data-ttu-id="aa4dc-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa4dc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4dc-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4dc-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4dc-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa4dc-161">INPUTS</span></span>

## <span data-ttu-id="aa4dc-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa4dc-162">OUTPUTS</span></span>

### <span data-ttu-id="aa4dc-163">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa4dc-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="aa4dc-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa4dc-164">NOTES</span></span>

## <span data-ttu-id="aa4dc-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa4dc-165">RELATED LINKS</span></span>

[<span data-ttu-id="aa4dc-166">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa4dc-166">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="aa4dc-167">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa4dc-167">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="aa4dc-168">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa4dc-168">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)
