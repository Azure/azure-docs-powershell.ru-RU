---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517938"
---
# <span data-ttu-id="8b1f5-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b1f5-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8b1f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="8b1f5-103">Обновляет конфигурацию правила безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8b1f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b1f5-104">SYNTAX</span></span>

### <span data-ttu-id="8b1f5-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b1f5-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b1f5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b1f5-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b1f5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b1f5-107">DESCRIPTION</span></span>
<span data-ttu-id="8b1f5-108">Командлет **Set-AzNetworkSecurityRuleConfig** обновляет конфигурацию правил безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8b1f5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b1f5-109">EXAMPLES</span></span>

### <span data-ttu-id="8b1f5-110">Пример 1. Изменение конфигурации доступа в правиле безопасности сети</span><span class="sxs-lookup"><span data-stu-id="8b1f5-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="8b1f5-111">Первая команда получает группу безопасности сети с именем NSG-FrontEnd, а затем сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="8b1f5-112">Вторая команда передает группу безопасности в $nsg команде Get-AzNetworkSecurityRuleConfig, которая получает конфигурацию правил безопасности с именем rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="8b1f5-113">Третья команда изменяет конфигурацию RDP-правила на "Запретить".</span><span class="sxs-lookup"><span data-stu-id="8b1f5-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="8b1f5-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b1f5-114">Example 2</span></span>

<span data-ttu-id="8b1f5-115">Обновляет конфигурацию правила безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="8b1f5-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="8b1f5-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="8b1f5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b1f5-117">PARAMETERS</span></span>

### <span data-ttu-id="8b1f5-118">-Access</span><span class="sxs-lookup"><span data-stu-id="8b1f5-118">-Access</span></span>
<span data-ttu-id="8b1f5-119">Указывает, разрешен или запрещен сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="8b1f5-120">Для этого параметра можно использовать допустимые значения: Allow (Разрешить) и Deny (Запретить).</span><span class="sxs-lookup"><span data-stu-id="8b1f5-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="8b1f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b1f5-121">-DefaultProfile</span></span>
<span data-ttu-id="8b1f5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b1f5-123">-Description</span><span class="sxs-lookup"><span data-stu-id="8b1f5-123">-Description</span></span>
<span data-ttu-id="8b1f5-124">Описание конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="8b1f5-125">Максимальный размер — 140 знаков.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="8b1f5-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b1f5-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="8b1f5-127">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="8b1f5-128">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="8b1f5-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b1f5-129">Адрес CIDR CIDR</span><span class="sxs-lookup"><span data-stu-id="8b1f5-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="8b1f5-130">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="8b1f5-130">A destination IP address range</span></span> 
- <span data-ttu-id="8b1f5-131">Подстановка (\*) для совпадения с ЛЮБЫМ IP-адресом, который можно использовать с такими тегами, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="8b1f5-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b1f5-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="8b1f5-133">Группа безопасности приложений, заемная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8b1f5-134">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8b1f5-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8b1f5-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="8b1f5-136">Группа безопасности приложений, заемная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="8b1f5-137">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8b1f5-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="8b1f5-138">-DestinationPortRange</span></span>
<span data-ttu-id="8b1f5-139">Указывает порт назначения или диапазон.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="8b1f5-140">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="8b1f5-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b1f5-141">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="8b1f5-141">An integer</span></span> 
- <span data-ttu-id="8b1f5-142">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="8b1f5-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8b1f5-143">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="8b1f5-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="8b1f5-144">-Direction</span><span class="sxs-lookup"><span data-stu-id="8b1f5-144">-Direction</span></span>
<span data-ttu-id="8b1f5-145">Указывает, следует ли оценивать правило для входящих и исходяющих трафика.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="8b1f5-146">Допустимыми значениями для этого параметра являются входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="8b1f5-147">-Name</span><span class="sxs-lookup"><span data-stu-id="8b1f5-147">-Name</span></span>
<span data-ttu-id="8b1f5-148">Задает имя конфигурации правила безопасности сети, заданной этим набором cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="8b1f5-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b1f5-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8b1f5-150">Объект **NetworkSecurityGroup,** содержащий заданную конфигурацию правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="8b1f5-151">-Priority</span><span class="sxs-lookup"><span data-stu-id="8b1f5-151">-Priority</span></span>
<span data-ttu-id="8b1f5-152">Определяет приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="8b1f5-153">Допустимыми значениями для этого параметра являются:integer between 100–4096.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="8b1f5-154">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="8b1f5-155">Чем ниже номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="8b1f5-156">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8b1f5-156">-Protocol</span></span>
<span data-ttu-id="8b1f5-157">Определяет сетевой протокол, к который применяется настройка правил.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="8b1f5-158">Допустимые значения для этого параметра: --Tcp</span><span class="sxs-lookup"><span data-stu-id="8b1f5-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="8b1f5-159">Udp</span><span class="sxs-lookup"><span data-stu-id="8b1f5-159">Udp</span></span>
- <span data-ttu-id="8b1f5-160">Поддиавный знак (\*), который соответствует обоим</span><span class="sxs-lookup"><span data-stu-id="8b1f5-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="8b1f5-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b1f5-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="8b1f5-162">Указывает префикс для исходных адресов.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="8b1f5-163">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="8b1f5-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b1f5-164">A CIDR</span><span class="sxs-lookup"><span data-stu-id="8b1f5-164">A CIDR</span></span>
- <span data-ttu-id="8b1f5-165">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="8b1f5-165">A source IP range</span></span>
- <span data-ttu-id="8b1f5-166">Подстановка (\*) для совпадения с ЛЮБЫМ IP-адресом Также можно использовать такие теги, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="8b1f5-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b1f5-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="8b1f5-168">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="8b1f5-169">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8b1f5-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="8b1f5-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="8b1f5-171">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="8b1f5-172">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="8b1f5-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="8b1f5-173">-SourcePortRange</span></span>
<span data-ttu-id="8b1f5-174">Определяет исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-174">Specifies the source port or range.</span></span>
<span data-ttu-id="8b1f5-175">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="8b1f5-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b1f5-176">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="8b1f5-176">An integer</span></span>
- <span data-ttu-id="8b1f5-177">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="8b1f5-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="8b1f5-178">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="8b1f5-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="8b1f5-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b1f5-179">CommonParameters</span></span>
<span data-ttu-id="8b1f5-180">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b1f5-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b1f5-181">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b1f5-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b1f5-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b1f5-182">INPUTS</span></span>

### <span data-ttu-id="8b1f5-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b1f5-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8b1f5-184">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b1f5-184">OUTPUTS</span></span>

### <span data-ttu-id="8b1f5-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8b1f5-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8b1f5-186">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b1f5-186">NOTES</span></span>

## <span data-ttu-id="8b1f5-187">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b1f5-187">RELATED LINKS</span></span>

[<span data-ttu-id="8b1f5-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b1f5-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8b1f5-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b1f5-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8b1f5-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b1f5-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8b1f5-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8b1f5-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


