---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729988"
---
# <span data-ttu-id="43716-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43716-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="43716-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43716-102">SYNOPSIS</span></span>
<span data-ttu-id="43716-103">Обновление конфигурации правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="43716-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="43716-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43716-104">SYNTAX</span></span>

### <span data-ttu-id="43716-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43716-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43716-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="43716-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43716-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43716-107">DESCRIPTION</span></span>
<span data-ttu-id="43716-108">Командлет **Set-AzNetworkSecurityRuleConfig** обновляет конфигурацию правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="43716-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="43716-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43716-109">EXAMPLES</span></span>

### <span data-ttu-id="43716-110">Пример 1: изменение конфигурации доступа в правиле сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="43716-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="43716-111">Первая команда получает сетевую группу безопасности с именем NSG-интерфейс и сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="43716-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="43716-112">Вторая команда использует оператор Pipeline для передачи группы безопасности в $nsg на Get-AzNetworkSecurityRuleConfig, который получает конфигурацию правила безопасности с именем RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="43716-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="43716-113">Третья команда изменяет конфигурацию доступа RDP-правила на "запретить".</span><span class="sxs-lookup"><span data-stu-id="43716-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="43716-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43716-114">PARAMETERS</span></span>

### <span data-ttu-id="43716-115">-Доступ</span><span class="sxs-lookup"><span data-stu-id="43716-115">-Access</span></span>
<span data-ttu-id="43716-116">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="43716-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="43716-117">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="43716-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="43716-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43716-118">-DefaultProfile</span></span>
<span data-ttu-id="43716-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43716-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43716-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="43716-120">-Description</span></span>
<span data-ttu-id="43716-121">Задает описание конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="43716-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="43716-122">Максимальный размер — 140 символов.</span><span class="sxs-lookup"><span data-stu-id="43716-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="43716-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43716-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="43716-124">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="43716-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="43716-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43716-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43716-126">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="43716-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="43716-127">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="43716-127">A destination IP address range</span></span> 
- <span data-ttu-id="43716-128">Подстановочный знак (\*) для поиска соответствия любому IP-адресу, в котором можно использовать теги, такие как VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="43716-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="43716-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43716-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="43716-130">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="43716-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="43716-131">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="43716-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="43716-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="43716-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="43716-133">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="43716-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="43716-134">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="43716-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="43716-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="43716-135">-DestinationPortRange</span></span>
<span data-ttu-id="43716-136">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="43716-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="43716-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43716-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43716-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="43716-138">An integer</span></span> 
- <span data-ttu-id="43716-139">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="43716-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="43716-140">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="43716-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="43716-141">-Направление</span><span class="sxs-lookup"><span data-stu-id="43716-141">-Direction</span></span>
<span data-ttu-id="43716-142">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="43716-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="43716-143">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="43716-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="43716-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43716-144">-Name</span></span>
<span data-ttu-id="43716-145">Указывает имя конфигурации правила сетевой безопасности, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="43716-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="43716-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43716-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="43716-147">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="43716-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="43716-148">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="43716-148">-Priority</span></span>
<span data-ttu-id="43716-149">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="43716-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="43716-150">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="43716-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="43716-151">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="43716-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="43716-152">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="43716-152">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="43716-153">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="43716-153">-Protocol</span></span>
<span data-ttu-id="43716-154">Указывает сетевой протокол, к которому применяется конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="43716-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="43716-155">Допустимые значения этого параметра:--TCP</span><span class="sxs-lookup"><span data-stu-id="43716-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="43716-156">Трафика</span><span class="sxs-lookup"><span data-stu-id="43716-156">Udp</span></span>
- <span data-ttu-id="43716-157">Подстановочный знак (\*) для поиска соответствия обоим</span><span class="sxs-lookup"><span data-stu-id="43716-157">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="43716-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="43716-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="43716-159">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="43716-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="43716-160">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43716-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43716-161">CIDR</span><span class="sxs-lookup"><span data-stu-id="43716-161">A CIDR</span></span>
- <span data-ttu-id="43716-162">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="43716-162">A source IP range</span></span>
- <span data-ttu-id="43716-163">Подстановочный знак (\*) для поиска соответствия любому IP-адресу вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="43716-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="43716-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43716-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="43716-165">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="43716-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="43716-166">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="43716-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="43716-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="43716-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="43716-168">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="43716-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="43716-169">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="43716-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="43716-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="43716-170">-SourcePortRange</span></span>
<span data-ttu-id="43716-171">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="43716-171">Specifies the source port or range.</span></span>
<span data-ttu-id="43716-172">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43716-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43716-173">Целое число</span><span class="sxs-lookup"><span data-stu-id="43716-173">An integer</span></span>
- <span data-ttu-id="43716-174">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="43716-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="43716-175">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="43716-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="43716-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43716-176">CommonParameters</span></span>
<span data-ttu-id="43716-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43716-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43716-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43716-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43716-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43716-179">INPUTS</span></span>

### <span data-ttu-id="43716-180">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43716-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="43716-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43716-181">OUTPUTS</span></span>

### <span data-ttu-id="43716-182">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43716-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="43716-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="43716-183">NOTES</span></span>

## <span data-ttu-id="43716-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43716-184">RELATED LINKS</span></span>

[<span data-ttu-id="43716-185">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43716-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="43716-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43716-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="43716-187">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43716-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="43716-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="43716-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


