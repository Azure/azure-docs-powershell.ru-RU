---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 963dc6391ef5f500b26068e2a407eacd64ce6c16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911029"
---
# <span data-ttu-id="78897-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78897-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="78897-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78897-102">SYNOPSIS</span></span>
<span data-ttu-id="78897-103">Задает состояние цели для конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="78897-103">Sets the goal state for a network security rule configuration.</span></span>

## <span data-ttu-id="78897-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78897-104">SYNTAX</span></span>

### <span data-ttu-id="78897-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78897-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="78897-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="78897-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78897-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78897-107">DESCRIPTION</span></span>
<span data-ttu-id="78897-108">Командлет **Set-AzNetworkSecurityRuleConfig** задает состояние цели для конфигурации правила сетевой безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="78897-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="78897-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78897-109">EXAMPLES</span></span>

### <span data-ttu-id="78897-110">Пример 1: изменение конфигурации доступа в правиле сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="78897-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="78897-111">Первая команда получает сетевую группу безопасности с именем NSG-интерфейс и сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="78897-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="78897-112">Вторая команда использует оператор Pipeline для передачи группы безопасности в $nsg на Get-AzNetworkSecurityRuleConfig, который получает конфигурацию правила безопасности с именем RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="78897-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="78897-113">Третья команда изменяет конфигурацию доступа RDP-правила на "запретить".</span><span class="sxs-lookup"><span data-stu-id="78897-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="78897-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78897-114">PARAMETERS</span></span>

### <span data-ttu-id="78897-115">-Доступ</span><span class="sxs-lookup"><span data-stu-id="78897-115">-Access</span></span>
<span data-ttu-id="78897-116">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="78897-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="78897-117">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="78897-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="78897-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78897-118">-DefaultProfile</span></span>
<span data-ttu-id="78897-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78897-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78897-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="78897-120">-Description</span></span>
<span data-ttu-id="78897-121">Задает описание конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="78897-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="78897-122">Максимальный размер — 140 символов.</span><span class="sxs-lookup"><span data-stu-id="78897-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="78897-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="78897-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="78897-124">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="78897-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="78897-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78897-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78897-126">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="78897-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="78897-127">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="78897-127">A destination IP address range</span></span> 
- <span data-ttu-id="78897-128">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="78897-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="78897-129">Вы можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="78897-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="78897-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78897-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="78897-131">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="78897-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="78897-132">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="78897-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="78897-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="78897-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="78897-134">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="78897-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="78897-135">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="78897-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="78897-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="78897-136">-DestinationPortRange</span></span>
<span data-ttu-id="78897-137">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="78897-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="78897-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78897-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78897-139">Целое число</span><span class="sxs-lookup"><span data-stu-id="78897-139">An integer</span></span> 
- <span data-ttu-id="78897-140">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="78897-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="78897-141">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="78897-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="78897-142">-Направление</span><span class="sxs-lookup"><span data-stu-id="78897-142">-Direction</span></span>
<span data-ttu-id="78897-143">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="78897-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="78897-144">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="78897-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="78897-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78897-145">-Name</span></span>
<span data-ttu-id="78897-146">Указывает имя конфигурации правила сетевой безопасности, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="78897-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="78897-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78897-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="78897-148">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="78897-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="78897-149">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="78897-149">-Priority</span></span>
<span data-ttu-id="78897-150">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="78897-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="78897-151">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="78897-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="78897-152">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="78897-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="78897-153">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="78897-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="78897-154">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="78897-154">-Protocol</span></span>
<span data-ttu-id="78897-155">Указывает сетевой протокол, к которому применяется конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="78897-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="78897-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78897-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="78897-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="78897-157">--Tcp</span></span>
- <span data-ttu-id="78897-158">Трафика</span><span class="sxs-lookup"><span data-stu-id="78897-158">Udp</span></span>
- <span data-ttu-id="78897-159">Подстановочный знак (\*) для поиска соответствия обоим</span><span class="sxs-lookup"><span data-stu-id="78897-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="78897-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="78897-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="78897-161">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="78897-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="78897-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78897-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78897-163">CIDR</span><span class="sxs-lookup"><span data-stu-id="78897-163">A CIDR</span></span>
- <span data-ttu-id="78897-164">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="78897-164">A source IP range</span></span>
- <span data-ttu-id="78897-165">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="78897-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="78897-166">Вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="78897-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="78897-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78897-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="78897-168">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="78897-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="78897-169">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="78897-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="78897-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="78897-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="78897-171">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="78897-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="78897-172">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="78897-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="78897-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="78897-173">-SourcePortRange</span></span>
<span data-ttu-id="78897-174">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="78897-174">Specifies the source port or range.</span></span>
<span data-ttu-id="78897-175">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78897-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78897-176">Целое число</span><span class="sxs-lookup"><span data-stu-id="78897-176">An integer</span></span>
- <span data-ttu-id="78897-177">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="78897-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="78897-178">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="78897-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="78897-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78897-179">CommonParameters</span></span>
<span data-ttu-id="78897-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78897-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78897-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78897-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78897-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78897-182">INPUTS</span></span>

### <span data-ttu-id="78897-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78897-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="78897-184">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="78897-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="78897-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78897-185">OUTPUTS</span></span>

### <span data-ttu-id="78897-186">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78897-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="78897-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="78897-187">NOTES</span></span>

## <span data-ttu-id="78897-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78897-188">RELATED LINKS</span></span>

[<span data-ttu-id="78897-189">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78897-189">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78897-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78897-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78897-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78897-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="78897-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="78897-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


