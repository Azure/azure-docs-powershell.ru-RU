---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003272"
---
# <span data-ttu-id="ee125-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee125-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ee125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee125-102">SYNOPSIS</span></span>
<span data-ttu-id="ee125-103">Обновляет конфигурацию правила безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ee125-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="ee125-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee125-104">SYNTAX</span></span>

### <span data-ttu-id="ee125-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee125-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee125-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee125-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee125-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee125-107">DESCRIPTION</span></span>
<span data-ttu-id="ee125-108">Командлет **Set-AzNetworkSecurityRuleConfig** обновляет конфигурацию правил безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ee125-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="ee125-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee125-109">EXAMPLES</span></span>

### <span data-ttu-id="ee125-110">Пример 1. Изменение конфигурации доступа в правиле безопасности сети</span><span class="sxs-lookup"><span data-stu-id="ee125-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="ee125-111">Первая команда получает группу безопасности сети с именем NSG-FrontEnd, а затем сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="ee125-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="ee125-112">Вторая команда передает группу безопасности в $nsg команде Get-AzNetworkSecurityRuleConfig, которая получает конфигурацию правил безопасности с именем rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="ee125-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="ee125-113">Третья команда изменяет конфигурацию RDP-правила на "Запретить".</span><span class="sxs-lookup"><span data-stu-id="ee125-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="ee125-114">Однако при этом правило переопишется и задает только параметры, которые передаются Set-AzNetworkSecurityRuleConfig функции.</span><span class="sxs-lookup"><span data-stu-id="ee125-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="ee125-115">ПРИМЕЧАНИЕ. Изменить один атрибут не существует</span><span class="sxs-lookup"><span data-stu-id="ee125-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="ee125-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee125-116">Example 2</span></span>

<span data-ttu-id="ee125-117">Обновляет конфигурацию правила безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ee125-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="ee125-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="ee125-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="ee125-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee125-119">PARAMETERS</span></span>

### <span data-ttu-id="ee125-120">-Access</span><span class="sxs-lookup"><span data-stu-id="ee125-120">-Access</span></span>
<span data-ttu-id="ee125-121">Указывает, разрешен или запрещен сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="ee125-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="ee125-122">Для этого параметра можно использовать допустимые значения: "Разрешить" и "Запретить".</span><span class="sxs-lookup"><span data-stu-id="ee125-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="ee125-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee125-123">-DefaultProfile</span></span>
<span data-ttu-id="ee125-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee125-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee125-125">-Description</span><span class="sxs-lookup"><span data-stu-id="ee125-125">-Description</span></span>
<span data-ttu-id="ee125-126">Описание конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="ee125-127">Максимальный размер — 140 знаков.</span><span class="sxs-lookup"><span data-stu-id="ee125-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="ee125-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ee125-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="ee125-129">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="ee125-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="ee125-130">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ee125-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee125-131">Адрес CIDR CIDR</span><span class="sxs-lookup"><span data-stu-id="ee125-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="ee125-132">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="ee125-132">A destination IP address range</span></span> 
- <span data-ttu-id="ee125-133">Подстановка (\*) для совпадения с ЛЮБЫМ IP-адресом, который можно использовать с такими тегами, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="ee125-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="ee125-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee125-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="ee125-135">Группа безопасности приложений, за установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ee125-136">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="ee125-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ee125-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ee125-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="ee125-138">Группа безопасности приложений, за установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="ee125-139">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="ee125-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ee125-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="ee125-140">-DestinationPortRange</span></span>
<span data-ttu-id="ee125-141">Определяет порт назначения или диапазон.</span><span class="sxs-lookup"><span data-stu-id="ee125-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="ee125-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ee125-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee125-143">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="ee125-143">An integer</span></span> 
- <span data-ttu-id="ee125-144">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="ee125-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ee125-145">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="ee125-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ee125-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="ee125-146">-Direction</span></span>
<span data-ttu-id="ee125-147">Указывает, следует ли оценивать правило для входящих и исходяющих трафика.</span><span class="sxs-lookup"><span data-stu-id="ee125-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="ee125-148">Допустимыми значениями для этого параметра являются входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="ee125-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="ee125-149">-Name</span><span class="sxs-lookup"><span data-stu-id="ee125-149">-Name</span></span>
<span data-ttu-id="ee125-150">Задает имя конфигурации правила безопасности сети, заданного этим набором cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee125-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="ee125-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee125-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ee125-152">Объект **NetworkSecurityGroup,** содержащий заданную конфигурацию правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="ee125-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="ee125-153">-Priority</span><span class="sxs-lookup"><span data-stu-id="ee125-153">-Priority</span></span>
<span data-ttu-id="ee125-154">Определяет приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="ee125-155">Допустимыми значениями для этого параметра являются:integer between 100–4096.</span><span class="sxs-lookup"><span data-stu-id="ee125-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="ee125-156">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ee125-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="ee125-157">Чем ниже номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="ee125-158">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ee125-158">-Protocol</span></span>
<span data-ttu-id="ee125-159">Определяет сетевой протокол, к который применяется настройка правил.</span><span class="sxs-lookup"><span data-stu-id="ee125-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="ee125-160">Допустимые значения для этого параметра: --Tcp</span><span class="sxs-lookup"><span data-stu-id="ee125-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="ee125-161">Udp</span><span class="sxs-lookup"><span data-stu-id="ee125-161">Udp</span></span>
- <span data-ttu-id="ee125-162">Поддиавный знак (\*), который соответствует обоим</span><span class="sxs-lookup"><span data-stu-id="ee125-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="ee125-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ee125-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="ee125-164">Указывает префикс для исходных адресов.</span><span class="sxs-lookup"><span data-stu-id="ee125-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="ee125-165">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ee125-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee125-166">A CIDR</span><span class="sxs-lookup"><span data-stu-id="ee125-166">A CIDR</span></span>
- <span data-ttu-id="ee125-167">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="ee125-167">A source IP range</span></span>
- <span data-ttu-id="ee125-168">Подстановавный знак (\*), который соответствует любому IP-адресу, можно также использовать такие теги, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="ee125-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="ee125-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee125-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="ee125-170">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="ee125-171">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="ee125-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ee125-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ee125-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="ee125-173">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="ee125-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="ee125-174">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="ee125-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="ee125-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="ee125-175">-SourcePortRange</span></span>
<span data-ttu-id="ee125-176">Определяет исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="ee125-176">Specifies the source port or range.</span></span>
<span data-ttu-id="ee125-177">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ee125-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ee125-178">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="ee125-178">An integer</span></span>
- <span data-ttu-id="ee125-179">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="ee125-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="ee125-180">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="ee125-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="ee125-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee125-181">CommonParameters</span></span>
<span data-ttu-id="ee125-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee125-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee125-183">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee125-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee125-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee125-184">INPUTS</span></span>

### <span data-ttu-id="ee125-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee125-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ee125-186">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee125-186">OUTPUTS</span></span>

### <span data-ttu-id="ee125-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee125-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ee125-188">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee125-188">NOTES</span></span>

## <span data-ttu-id="ee125-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee125-189">RELATED LINKS</span></span>

[<span data-ttu-id="ee125-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee125-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ee125-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee125-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ee125-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee125-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ee125-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ee125-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


