---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079432"
---
# <span data-ttu-id="2b503-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b503-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="2b503-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b503-102">SYNOPSIS</span></span>
<span data-ttu-id="2b503-103">Обновление конфигурации правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="2b503-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="2b503-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b503-104">SYNTAX</span></span>

### <span data-ttu-id="2b503-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b503-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b503-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b503-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b503-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b503-107">DESCRIPTION</span></span>
<span data-ttu-id="2b503-108">Командлет **Set-AzNetworkSecurityRuleConfig** обновляет конфигурацию правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="2b503-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="2b503-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b503-109">EXAMPLES</span></span>

### <span data-ttu-id="2b503-110">Пример 1: изменение конфигурации доступа в правиле сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="2b503-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="2b503-111">Первая команда получает сетевую группу безопасности с именем NSG-интерфейс и сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="2b503-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="2b503-112">Вторая команда использует оператор Pipeline для передачи группы безопасности в $nsg на Get-AzNetworkSecurityRuleConfig, который получает конфигурацию правила безопасности с именем RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="2b503-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="2b503-113">Третья команда изменяет конфигурацию доступа RDP-правила на "запретить".</span><span class="sxs-lookup"><span data-stu-id="2b503-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="2b503-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b503-114">Example 2</span></span>

<span data-ttu-id="2b503-115">Обновление конфигурации правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="2b503-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="2b503-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="2b503-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="2b503-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b503-117">PARAMETERS</span></span>

### <span data-ttu-id="2b503-118">-Доступ</span><span class="sxs-lookup"><span data-stu-id="2b503-118">-Access</span></span>
<span data-ttu-id="2b503-119">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="2b503-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="2b503-120">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="2b503-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="2b503-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b503-121">-DefaultProfile</span></span>
<span data-ttu-id="2b503-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b503-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b503-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="2b503-123">-Description</span></span>
<span data-ttu-id="2b503-124">Задает описание конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="2b503-125">Максимальный размер — 140 символов.</span><span class="sxs-lookup"><span data-stu-id="2b503-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="2b503-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2b503-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="2b503-127">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="2b503-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="2b503-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2b503-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b503-129">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="2b503-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="2b503-130">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="2b503-130">A destination IP address range</span></span> 
- <span data-ttu-id="2b503-131">Подстановочный знак (\*) для поиска соответствия любому IP-адресу, в котором можно использовать теги, такие как VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="2b503-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="2b503-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="2b503-133">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="2b503-134">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="2b503-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2b503-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2b503-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="2b503-136">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="2b503-137">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="2b503-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2b503-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="2b503-138">-DestinationPortRange</span></span>
<span data-ttu-id="2b503-139">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="2b503-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="2b503-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2b503-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b503-141">Целое число</span><span class="sxs-lookup"><span data-stu-id="2b503-141">An integer</span></span> 
- <span data-ttu-id="2b503-142">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="2b503-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="2b503-143">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="2b503-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="2b503-144">-Направление</span><span class="sxs-lookup"><span data-stu-id="2b503-144">-Direction</span></span>
<span data-ttu-id="2b503-145">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="2b503-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="2b503-146">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="2b503-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="2b503-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b503-147">-Name</span></span>
<span data-ttu-id="2b503-148">Указывает имя конфигурации правила сетевой безопасности, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b503-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="2b503-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2b503-150">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="2b503-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="2b503-151">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="2b503-151">-Priority</span></span>
<span data-ttu-id="2b503-152">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="2b503-153">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="2b503-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="2b503-154">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="2b503-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="2b503-155">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="2b503-156">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="2b503-156">-Protocol</span></span>
<span data-ttu-id="2b503-157">Указывает сетевой протокол, к которому применяется конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="2b503-158">Допустимые значения этого параметра:--TCP</span><span class="sxs-lookup"><span data-stu-id="2b503-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="2b503-159">Трафика</span><span class="sxs-lookup"><span data-stu-id="2b503-159">Udp</span></span>
- <span data-ttu-id="2b503-160">Подстановочный знак (\*) для поиска соответствия обоим</span><span class="sxs-lookup"><span data-stu-id="2b503-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="2b503-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2b503-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="2b503-162">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="2b503-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="2b503-163">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2b503-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b503-164">CIDR</span><span class="sxs-lookup"><span data-stu-id="2b503-164">A CIDR</span></span>
- <span data-ttu-id="2b503-165">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="2b503-165">A source IP range</span></span>
- <span data-ttu-id="2b503-166">Подстановочный знак (\*) для поиска соответствия любому IP-адресу вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="2b503-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="2b503-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="2b503-168">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="2b503-169">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="2b503-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2b503-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="2b503-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="2b503-171">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="2b503-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="2b503-172">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="2b503-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="2b503-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="2b503-173">-SourcePortRange</span></span>
<span data-ttu-id="2b503-174">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="2b503-174">Specifies the source port or range.</span></span>
<span data-ttu-id="2b503-175">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2b503-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b503-176">Целое число</span><span class="sxs-lookup"><span data-stu-id="2b503-176">An integer</span></span>
- <span data-ttu-id="2b503-177">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="2b503-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="2b503-178">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="2b503-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="2b503-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b503-179">CommonParameters</span></span>
<span data-ttu-id="2b503-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b503-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b503-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b503-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b503-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b503-182">INPUTS</span></span>

### <span data-ttu-id="2b503-183">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="2b503-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b503-184">OUTPUTS</span></span>

### <span data-ttu-id="2b503-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b503-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="2b503-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b503-186">NOTES</span></span>

## <span data-ttu-id="2b503-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b503-187">RELATED LINKS</span></span>

[<span data-ttu-id="2b503-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b503-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2b503-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b503-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2b503-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b503-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="2b503-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2b503-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


