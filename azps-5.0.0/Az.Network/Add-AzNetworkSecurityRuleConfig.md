---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247054"
---
# <span data-ttu-id="df3d6-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df3d6-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="df3d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="df3d6-103">Добавляет конфигурацию правила сетевой безопасности в сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="df3d6-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="df3d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df3d6-104">SYNTAX</span></span>

### <span data-ttu-id="df3d6-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df3d6-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df3d6-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="df3d6-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df3d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df3d6-107">DESCRIPTION</span></span>
<span data-ttu-id="df3d6-108">Командлет **Add-AzNetworkSecurityRuleConfig** добавляет конфигурацию правила сетевой безопасности в группу безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="df3d6-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="df3d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df3d6-109">EXAMPLES</span></span>

### <span data-ttu-id="df3d6-110">1: Добавление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="df3d6-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="df3d6-111">В первой команде извлекается Сетевая группа безопасности Azure с именем "nsg1" из группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="df3d6-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="df3d6-112">Вторая команда добавляет правило сетевой безопасности с именем "RDP-правило", разрешающее трафик из Интернета на порт 3389 в полученный объект группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="df3d6-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="df3d6-113">Сохранение измененной группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="df3d6-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="df3d6-114">2. Добавление нового правила безопасности с группами безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="df3d6-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="df3d6-115">Для начала мы создаем две новые группы безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="df3d6-115">First, we create two new application security groups.</span></span> <span data-ttu-id="df3d6-116">Затем извлекается Сетевая группа безопасности Azure с именем "nsg1" из группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="df3d6-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="df3d6-117">и добавьте правило сетевой безопасности с именем "RDP-правило".</span><span class="sxs-lookup"><span data-stu-id="df3d6-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="df3d6-118">Правило разрешает трафик из всех IP-конфигураций в группе безопасности приложения "srcAsg" ко всем настройкам IP в разделе "destAsg" для порта 3389.</span><span class="sxs-lookup"><span data-stu-id="df3d6-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="df3d6-119">После того как вы добавите правило, мы сохраняем измененную сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="df3d6-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="df3d6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df3d6-120">PARAMETERS</span></span>

### <span data-ttu-id="df3d6-121">-Доступ</span><span class="sxs-lookup"><span data-stu-id="df3d6-121">-Access</span></span>
<span data-ttu-id="df3d6-122">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="df3d6-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="df3d6-123">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="df3d6-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="df3d6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3d6-124">-DefaultProfile</span></span>
<span data-ttu-id="df3d6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df3d6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df3d6-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="df3d6-126">-Description</span></span>
<span data-ttu-id="df3d6-127">Задает описание конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="df3d6-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="df3d6-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="df3d6-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="df3d6-129">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="df3d6-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="df3d6-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="df3d6-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df3d6-131">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="df3d6-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="df3d6-132">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="df3d6-132">A destination IP address range</span></span>
- <span data-ttu-id="df3d6-133">Подстановочный знак (\*) для поиска соответствия любому IP-адресу, в котором можно использовать теги, такие как VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="df3d6-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="df3d6-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df3d6-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="df3d6-135">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="df3d6-136">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df3d6-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="df3d6-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="df3d6-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="df3d6-138">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="df3d6-139">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df3d6-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="df3d6-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="df3d6-140">-DestinationPortRange</span></span>
<span data-ttu-id="df3d6-141">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="df3d6-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="df3d6-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="df3d6-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df3d6-143">Целое число</span><span class="sxs-lookup"><span data-stu-id="df3d6-143">An integer</span></span>
- <span data-ttu-id="df3d6-144">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="df3d6-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="df3d6-145">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="df3d6-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="df3d6-146">-Направление</span><span class="sxs-lookup"><span data-stu-id="df3d6-146">-Direction</span></span>
<span data-ttu-id="df3d6-147">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="df3d6-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="df3d6-148">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="df3d6-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="df3d6-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df3d6-149">-Name</span></span>
<span data-ttu-id="df3d6-150">Указывает имя конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="df3d6-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="df3d6-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df3d6-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="df3d6-152">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="df3d6-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="df3d6-153">Этот командлет добавляет конфигурацию правила сетевой безопасности к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="df3d6-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="df3d6-154">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="df3d6-154">-Priority</span></span>
<span data-ttu-id="df3d6-155">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="df3d6-156">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="df3d6-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="df3d6-157">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="df3d6-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="df3d6-158">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="df3d6-159">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="df3d6-159">-Protocol</span></span>
<span data-ttu-id="df3d6-160">Указывает сетевой протокол, к которому применяется конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="df3d6-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="df3d6-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df3d6-162">Номера</span><span class="sxs-lookup"><span data-stu-id="df3d6-162">Tcp</span></span>
- <span data-ttu-id="df3d6-163">Трафика</span><span class="sxs-lookup"><span data-stu-id="df3d6-163">Udp</span></span>
- <span data-ttu-id="df3d6-164">Подстановочный знак (\*) для поиска соответствия обоим</span><span class="sxs-lookup"><span data-stu-id="df3d6-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="df3d6-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="df3d6-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="df3d6-166">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="df3d6-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="df3d6-167">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="df3d6-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df3d6-168">CIDR</span><span class="sxs-lookup"><span data-stu-id="df3d6-168">A CIDR</span></span>
- <span data-ttu-id="df3d6-169">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="df3d6-169">A source IP range</span></span>
- <span data-ttu-id="df3d6-170">Подстановочный знак (\*) для соответствия любому IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="df3d6-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="df3d6-171">Вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="df3d6-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="df3d6-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df3d6-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="df3d6-173">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="df3d6-174">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df3d6-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="df3d6-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="df3d6-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="df3d6-176">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="df3d6-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="df3d6-177">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df3d6-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="df3d6-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="df3d6-178">-SourcePortRange</span></span>
<span data-ttu-id="df3d6-179">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="df3d6-179">Specifies a source port or range.</span></span>
<span data-ttu-id="df3d6-180">Это значение выражается как целое число в диапазоне от 0 до 65535 или как подстановочный знак (\*) для соответствия любому порту источника.</span><span class="sxs-lookup"><span data-stu-id="df3d6-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="df3d6-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3d6-181">CommonParameters</span></span>
<span data-ttu-id="df3d6-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df3d6-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3d6-183">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df3d6-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3d6-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df3d6-184">INPUTS</span></span>

### <span data-ttu-id="df3d6-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df3d6-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="df3d6-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df3d6-186">OUTPUTS</span></span>

### <span data-ttu-id="df3d6-187">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df3d6-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="df3d6-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="df3d6-188">NOTES</span></span>

## <span data-ttu-id="df3d6-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df3d6-189">RELATED LINKS</span></span>

[<span data-ttu-id="df3d6-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df3d6-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df3d6-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df3d6-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df3d6-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df3d6-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df3d6-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df3d6-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

