---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: b2b1667a9326a9c25d78639e397146c0dd85dc5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910127"
---
# <span data-ttu-id="9900b-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9900b-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9900b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9900b-102">SYNOPSIS</span></span>
<span data-ttu-id="9900b-103">Добавляет конфигурацию правила сетевой безопасности в сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="9900b-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="9900b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9900b-104">SYNTAX</span></span>

### <span data-ttu-id="9900b-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9900b-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9900b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9900b-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9900b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9900b-107">DESCRIPTION</span></span>
<span data-ttu-id="9900b-108">Командлет **Add-AzNetworkSecurityRuleConfig** добавляет конфигурацию правила сетевой безопасности в группу безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9900b-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="9900b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9900b-109">EXAMPLES</span></span>

### <span data-ttu-id="9900b-110">1: Добавление группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="9900b-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="9900b-111">В первой команде извлекается Сетевая группа безопасности Azure с именем "nsg1" из группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="9900b-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="9900b-112">Вторая команда добавляет правило сетевой безопасности с именем "RDP-правило", разрешающее трафик из Интернета на порт 3389 в полученный объект группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9900b-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="9900b-113">Сохранение измененной группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9900b-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="9900b-114">1: Добавление нового правила безопасности с группами безопасности приложений</span><span class="sxs-lookup"><span data-stu-id="9900b-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="9900b-115">Для начала мы создаем две новые группы безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="9900b-115">First, we create two new application security groups.</span></span> <span data-ttu-id="9900b-116">Затем извлекается Сетевая группа безопасности Azure с именем "nsg1" из группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="9900b-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="9900b-117">и добавьте правило сетевой безопасности с именем "RDP-правило".</span><span class="sxs-lookup"><span data-stu-id="9900b-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="9900b-118">Правило разрешает трафик из всех IP-конфигураций в группе безопасности приложения "srcAsg" ко всем настройкам IP в разделе "destAsg" для порта 3389.</span><span class="sxs-lookup"><span data-stu-id="9900b-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="9900b-119">После того как вы добавите правило, мы сохраняем измененную сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="9900b-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="9900b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9900b-120">PARAMETERS</span></span>

### <span data-ttu-id="9900b-121">-Доступ</span><span class="sxs-lookup"><span data-stu-id="9900b-121">-Access</span></span>
<span data-ttu-id="9900b-122">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="9900b-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="9900b-123">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="9900b-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9900b-124">-DefaultProfile</span></span>
<span data-ttu-id="9900b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9900b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9900b-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="9900b-126">-Description</span></span>
<span data-ttu-id="9900b-127">Задает описание конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="9900b-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9900b-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="9900b-129">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="9900b-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="9900b-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9900b-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9900b-131">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="9900b-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="9900b-132">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="9900b-132">A destination IP address range</span></span>
- <span data-ttu-id="9900b-133">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="9900b-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="9900b-134">Вы можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="9900b-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9900b-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="9900b-136">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9900b-137">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9900b-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9900b-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="9900b-139">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9900b-140">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9900b-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="9900b-141">-DestinationPortRange</span></span>
<span data-ttu-id="9900b-142">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="9900b-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="9900b-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9900b-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9900b-144">Целое число</span><span class="sxs-lookup"><span data-stu-id="9900b-144">An integer</span></span>
- <span data-ttu-id="9900b-145">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="9900b-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9900b-146">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="9900b-146">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-147">-Направление</span><span class="sxs-lookup"><span data-stu-id="9900b-147">-Direction</span></span>
<span data-ttu-id="9900b-148">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="9900b-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="9900b-149">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="9900b-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9900b-150">-Name</span></span>
<span data-ttu-id="9900b-151">Указывает имя конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="9900b-151">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="9900b-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9900b-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9900b-153">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="9900b-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="9900b-154">Этот командлет добавляет конфигурацию правила сетевой безопасности к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="9900b-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-155">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="9900b-155">-Priority</span></span>
<span data-ttu-id="9900b-156">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="9900b-157">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="9900b-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="9900b-158">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9900b-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="9900b-159">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-159">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="9900b-160">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9900b-160">-Protocol</span></span>
<span data-ttu-id="9900b-161">Указывает сетевой протокол, к которому применяется конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="9900b-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9900b-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9900b-163">Номера</span><span class="sxs-lookup"><span data-stu-id="9900b-163">Tcp</span></span>
- <span data-ttu-id="9900b-164">Трафика</span><span class="sxs-lookup"><span data-stu-id="9900b-164">Udp</span></span>
- <span data-ttu-id="9900b-165">Подстановочный знак (\*) для поиска соответствия обоим</span><span class="sxs-lookup"><span data-stu-id="9900b-165">Wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9900b-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="9900b-167">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="9900b-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="9900b-168">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9900b-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9900b-169">CIDR</span><span class="sxs-lookup"><span data-stu-id="9900b-169">A CIDR</span></span>
- <span data-ttu-id="9900b-170">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="9900b-170">A source IP range</span></span>
- <span data-ttu-id="9900b-171">Подстановочный знак (\*) для соответствия любому IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="9900b-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="9900b-172">Вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="9900b-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9900b-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="9900b-174">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="9900b-175">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9900b-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9900b-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="9900b-177">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="9900b-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="9900b-178">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9900b-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="9900b-179">-SourcePortRange</span></span>
<span data-ttu-id="9900b-180">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="9900b-180">Specifies a source port or range.</span></span>
<span data-ttu-id="9900b-181">Это значение выражается как целое число в диапазоне от 0 до 65535 или как подстановочный знак (\*) для соответствия любому порту источника.</span><span class="sxs-lookup"><span data-stu-id="9900b-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9900b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9900b-182">CommonParameters</span></span>
<span data-ttu-id="9900b-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9900b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9900b-184">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9900b-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9900b-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9900b-185">INPUTS</span></span>

### <span data-ttu-id="9900b-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9900b-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="9900b-187">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9900b-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="9900b-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9900b-188">OUTPUTS</span></span>

### <span data-ttu-id="9900b-189">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9900b-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9900b-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="9900b-190">NOTES</span></span>

## <span data-ttu-id="9900b-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9900b-191">RELATED LINKS</span></span>

[<span data-ttu-id="9900b-192">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9900b-192">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9900b-193">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9900b-193">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9900b-194">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9900b-194">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9900b-195">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9900b-195">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


