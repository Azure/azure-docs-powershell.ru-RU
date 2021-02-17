---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226092"
---
# <span data-ttu-id="8e2e9-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e2e9-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8e2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2e9-103">Добавляет конфигурацию правила безопасности сети в группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="8e2e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e2e9-104">SYNTAX</span></span>

### <span data-ttu-id="8e2e9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e2e9-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e2e9-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e2e9-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e2e9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e2e9-107">DESCRIPTION</span></span>
<span data-ttu-id="8e2e9-108">Командлет **Add-AzNetworkSecurityRuleConfig** добавляет конфигурацию правил безопасности сети в группу безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="8e2e9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e2e9-109">EXAMPLES</span></span>

### <span data-ttu-id="8e2e9-110">1. Добавление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="8e2e9-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="8e2e9-111">Первая команда извлекает группу безопасности сети Azure "nsg1" из группы ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="8e2e9-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="8e2e9-112">Вторая команда добавляет правило безопасности сети с именем rdp-rule, которое позволяет трафик из Интернета через порт 3389 к извлечению объекта группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="8e2e9-113">Сохраняет измененную группу безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="8e2e9-114">2. Добавление нового правила безопасности с группами безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="8e2e9-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="8e2e9-115">Сначала мы создадим две новые группы безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-115">First, we create two new application security groups.</span></span> <span data-ttu-id="8e2e9-116">Затем мы извлекаем группу безопасности сети Azure "nsg1" из группы ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="8e2e9-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="8e2e9-117">и добавьте в него правило безопасности сети с именем rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="8e2e9-118">Правило разрешает трафик из всех конфигураций IP-адресов в группе безопасности приложений "srcAsg" на все конфигурации IP-адресов в "destAsg" в порте 3389.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="8e2e9-119">После добавления правила измененная группа безопасности сети Azure сохраняется.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="8e2e9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e2e9-120">PARAMETERS</span></span>

### <span data-ttu-id="8e2e9-121">-Access</span><span class="sxs-lookup"><span data-stu-id="8e2e9-121">-Access</span></span>
<span data-ttu-id="8e2e9-122">Указывает, разрешен или запрещен сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="8e2e9-123">Для этого параметра можно использовать допустимые значения: Allow (Разрешить) и Deny (Запретить).</span><span class="sxs-lookup"><span data-stu-id="8e2e9-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2e9-124">-DefaultProfile</span></span>
<span data-ttu-id="8e2e9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e2e9-126">-Description</span><span class="sxs-lookup"><span data-stu-id="8e2e9-126">-Description</span></span>
<span data-ttu-id="8e2e9-127">Описание конфигурации правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8e2e9-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="8e2e9-129">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="8e2e9-130">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8e2e9-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e2e9-131">Адрес CIDR CIDR</span><span class="sxs-lookup"><span data-stu-id="8e2e9-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="8e2e9-132">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="8e2e9-132">A destination IP address range</span></span>
- <span data-ttu-id="8e2e9-133">Подстановка (\*) для совпадения с ЛЮБЫМ IP-адресом, который можно использовать с такими тегами, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e2e9-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="8e2e9-135">Группа безопасности приложений, за установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8e2e9-136">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8e2e9-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="8e2e9-138">Группа безопасности приложений, заемная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8e2e9-139">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="8e2e9-140">-DestinationPortRange</span></span>
<span data-ttu-id="8e2e9-141">Указывает порт назначения или диапазон.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="8e2e9-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8e2e9-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e2e9-143">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="8e2e9-143">An integer</span></span>
- <span data-ttu-id="8e2e9-144">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="8e2e9-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8e2e9-145">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="8e2e9-145">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="8e2e9-146">-Direction</span></span>
<span data-ttu-id="8e2e9-147">Указывает, следует ли оценивать правило для входящих и исходяющих трафика.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="8e2e9-148">Допустимыми значениями для этого параметра являются входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-149">-Name</span><span class="sxs-lookup"><span data-stu-id="8e2e9-149">-Name</span></span>
<span data-ttu-id="8e2e9-150">Указывает имя конфигурации правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="8e2e9-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e2e9-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8e2e9-152">Объект **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="8e2e9-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="8e2e9-153">Этот cmdlet добавляет конфигурацию правила безопасности сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="8e2e9-154">-Priority</span></span>
<span data-ttu-id="8e2e9-155">Определяет приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="8e2e9-156">Допустимыми значениями для этого параметра являются: integer between 100–4096.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="8e2e9-157">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="8e2e9-158">Чем ниже номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-158">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8e2e9-159">-Protocol</span></span>
<span data-ttu-id="8e2e9-160">Определяет сетевой протокол, к который применяется настройка правил.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="8e2e9-161">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8e2e9-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e2e9-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="8e2e9-162">Tcp</span></span>
- <span data-ttu-id="8e2e9-163">Udp</span><span class="sxs-lookup"><span data-stu-id="8e2e9-163">Udp</span></span>
- <span data-ttu-id="8e2e9-164">Поддиавный знак (\*), который соответствует обоим</span><span class="sxs-lookup"><span data-stu-id="8e2e9-164">Wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8e2e9-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="8e2e9-166">Указывает префикс для исходных адресов.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="8e2e9-167">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="8e2e9-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e2e9-168">A CIDR</span><span class="sxs-lookup"><span data-stu-id="8e2e9-168">A CIDR</span></span>
- <span data-ttu-id="8e2e9-169">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="8e2e9-169">A source IP range</span></span>
- <span data-ttu-id="8e2e9-170">Поддиавный знак (\*), который соответствует любому IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="8e2e9-171">Вы также можете использовать такие теги, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e2e9-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="8e2e9-173">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="8e2e9-174">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8e2e9-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="8e2e9-176">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="8e2e9-177">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="8e2e9-178">-SourcePortRange</span></span>
<span data-ttu-id="8e2e9-179">Определяет исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-179">Specifies a source port or range.</span></span>
<span data-ttu-id="8e2e9-180">Это значение выражается как integer, в диапазоне от 0 до 65 5535 или в качестве поддеревного знака (\*), совпадают с любым исходным портом.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2e9-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2e9-181">CommonParameters</span></span>
<span data-ttu-id="8e2e9-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2e9-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2e9-183">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2e9-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2e9-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2e9-184">INPUTS</span></span>

### <span data-ttu-id="8e2e9-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e2e9-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8e2e9-186">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2e9-186">OUTPUTS</span></span>

### <span data-ttu-id="8e2e9-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8e2e9-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8e2e9-188">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e2e9-188">NOTES</span></span>

## <span data-ttu-id="8e2e9-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e2e9-189">RELATED LINKS</span></span>

[<span data-ttu-id="8e2e9-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e2e9-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8e2e9-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e2e9-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8e2e9-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e2e9-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8e2e9-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e2e9-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


