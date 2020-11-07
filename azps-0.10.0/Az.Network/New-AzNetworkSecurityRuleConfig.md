---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 17e73f28595a0b99c8209634a6dee6838fa4599d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909657"
---
# <span data-ttu-id="c2199-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2199-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c2199-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2199-102">SYNOPSIS</span></span>
<span data-ttu-id="c2199-103">Создание конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="c2199-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="c2199-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2199-104">SYNTAX</span></span>

### <span data-ttu-id="c2199-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2199-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2199-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2199-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2199-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2199-107">DESCRIPTION</span></span>
<span data-ttu-id="c2199-108">Командлет **New-AzNetworkSecurityRuleConfig** создает конфигурацию правила сетевой безопасности Azure для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="c2199-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="c2199-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2199-109">EXAMPLES</span></span>

### <span data-ttu-id="c2199-110">1: Создание правила сетевой безопасности, разрешающее RDP</span><span class="sxs-lookup"><span data-stu-id="c2199-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="c2199-111">Эта команда создает правило безопасности, позволяющее доступ из Интернета к порту 3389</span><span class="sxs-lookup"><span data-stu-id="c2199-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="c2199-112">2. Создание правила сетевой безопасности, разрешающего HTTP</span><span class="sxs-lookup"><span data-stu-id="c2199-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="c2199-113">Эта команда создает правило безопасности, позволяющее доступ из Интернета к порту 80</span><span class="sxs-lookup"><span data-stu-id="c2199-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="c2199-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2199-114">PARAMETERS</span></span>

### <span data-ttu-id="c2199-115">-Доступ</span><span class="sxs-lookup"><span data-stu-id="c2199-115">-Access</span></span>
<span data-ttu-id="c2199-116">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="c2199-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="c2199-117">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="c2199-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="c2199-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2199-118">-DefaultProfile</span></span>
<span data-ttu-id="c2199-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2199-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2199-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="c2199-120">-Description</span></span>
<span data-ttu-id="c2199-121">Задает описание конфигурации правила сетевой безопасности для создания.</span><span class="sxs-lookup"><span data-stu-id="c2199-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="c2199-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c2199-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="c2199-123">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="c2199-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="c2199-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2199-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2199-125">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="c2199-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="c2199-126">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="c2199-126">A destination IP address range</span></span> 
- <span data-ttu-id="c2199-127">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="c2199-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="c2199-128">Вы можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="c2199-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="c2199-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2199-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="c2199-130">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c2199-131">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c2199-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c2199-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c2199-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="c2199-133">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c2199-134">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c2199-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c2199-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="c2199-135">-DestinationPortRange</span></span>
<span data-ttu-id="c2199-136">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="c2199-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="c2199-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2199-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2199-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="c2199-138">An integer</span></span>
- <span data-ttu-id="c2199-139">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="c2199-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c2199-140">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="c2199-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="c2199-141">-Направление</span><span class="sxs-lookup"><span data-stu-id="c2199-141">-Direction</span></span>
<span data-ttu-id="c2199-142">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="c2199-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="c2199-143">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="c2199-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="c2199-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2199-144">-Name</span></span>
<span data-ttu-id="c2199-145">Указывает имя конфигурации правила сетевой безопасности, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="c2199-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c2199-146">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="c2199-146">-Priority</span></span>
<span data-ttu-id="c2199-147">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="c2199-148">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="c2199-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="c2199-149">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2199-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="c2199-150">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="c2199-151">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c2199-151">-Protocol</span></span>
<span data-ttu-id="c2199-152">Указывает сетевой протокол, к которому применяется новая конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="c2199-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2199-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2199-154">Номера</span><span class="sxs-lookup"><span data-stu-id="c2199-154">Tcp</span></span>
- <span data-ttu-id="c2199-155">Трафика</span><span class="sxs-lookup"><span data-stu-id="c2199-155">Udp</span></span>
- <span data-ttu-id="c2199-156">подстановочный знак (\*) для поиска соответствия обоим.</span><span class="sxs-lookup"><span data-stu-id="c2199-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="c2199-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c2199-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="c2199-158">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="c2199-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="c2199-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2199-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2199-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="c2199-160">A CIDR</span></span>
- <span data-ttu-id="c2199-161">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="c2199-161">A source IP range</span></span>
- <span data-ttu-id="c2199-162">Подстановочный знак (\*) для соответствия любому IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="c2199-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="c2199-163">Вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="c2199-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="c2199-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c2199-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="c2199-165">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="c2199-166">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c2199-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c2199-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c2199-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="c2199-168">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="c2199-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="c2199-169">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c2199-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c2199-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="c2199-170">-SourcePortRange</span></span>
<span data-ttu-id="c2199-171">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="c2199-171">Specifies the source port or range.</span></span>
<span data-ttu-id="c2199-172">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2199-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2199-173">Целое число</span><span class="sxs-lookup"><span data-stu-id="c2199-173">An integer</span></span>
- <span data-ttu-id="c2199-174">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="c2199-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c2199-175">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="c2199-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="c2199-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2199-176">CommonParameters</span></span>
<span data-ttu-id="c2199-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2199-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2199-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2199-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2199-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2199-179">INPUTS</span></span>

## <span data-ttu-id="c2199-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2199-180">OUTPUTS</span></span>

### <span data-ttu-id="c2199-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="c2199-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="c2199-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2199-182">NOTES</span></span>

## <span data-ttu-id="c2199-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2199-183">RELATED LINKS</span></span>

[<span data-ttu-id="c2199-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2199-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c2199-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2199-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c2199-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2199-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c2199-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c2199-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


