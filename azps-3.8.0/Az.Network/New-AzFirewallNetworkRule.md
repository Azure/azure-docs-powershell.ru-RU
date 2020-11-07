---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 31c066ce97502c43c9e93bdaf532ee63e701a18f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911794"
---
# <span data-ttu-id="4e45b-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4e45b-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="4e45b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e45b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e45b-103">Создание сетевого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4e45b-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="4e45b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e45b-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e45b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e45b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e45b-106">Командлет **New-AzFirewallNetworkRule** создает сетевое правило для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4e45b-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="4e45b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e45b-107">EXAMPLES</span></span>

### <span data-ttu-id="4e45b-108">1: Создание правила для всего трафика TCP</span><span class="sxs-lookup"><span data-stu-id="4e45b-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="4e45b-109">В этом примере создается правило для всего трафика TCP.</span><span class="sxs-lookup"><span data-stu-id="4e45b-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="4e45b-110">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4e45b-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4e45b-111">2. Создайте правило для всего TCP-трафика с 10.0.0.0 на 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="4e45b-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="4e45b-112">В этом примере создается правило для всего трафика TCP из 10.0.0.0 в 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4e45b-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4e45b-113">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4e45b-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4e45b-114">3. Создайте правило для всего трафика TCP и ICMP из любого источника в 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="4e45b-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="4e45b-115">В этом примере создается правило для всего трафика TCP из 10.0.0.0 в 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4e45b-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4e45b-116">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4e45b-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="4e45b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e45b-117">PARAMETERS</span></span>

### <span data-ttu-id="4e45b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e45b-118">-DefaultProfile</span></span>
<span data-ttu-id="4e45b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e45b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e45b-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="4e45b-120">-Description</span></span>
<span data-ttu-id="4e45b-121">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="4e45b-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4e45b-122">-DestinationAddress</span></span>
<span data-ttu-id="4e45b-123">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="4e45b-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="4e45b-124">-DestinationFqdn</span></span>
<span data-ttu-id="4e45b-125">Полное доменное имя назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="4e45b-126">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="4e45b-126">-DestinationIpGroup</span></span>
<span data-ttu-id="4e45b-127">Конечная IPGroup правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="4e45b-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4e45b-128">-DestinationPort</span></span>
<span data-ttu-id="4e45b-129">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-129">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e45b-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e45b-130">-Name</span></span>
<span data-ttu-id="4e45b-131">Указывает имя сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="4e45b-132">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4e45b-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4e45b-133">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="4e45b-133">-Protocol</span></span>
<span data-ttu-id="4e45b-134">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="4e45b-135">Возможные значения: TCP, UDP, ICMP и ANY.</span><span class="sxs-lookup"><span data-stu-id="4e45b-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e45b-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4e45b-136">-SourceAddress</span></span>
<span data-ttu-id="4e45b-137">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="4e45b-137">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e45b-138">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="4e45b-138">-SourceIpGroup</span></span>
<span data-ttu-id="4e45b-139">Исходная IPGroup правила</span><span class="sxs-lookup"><span data-stu-id="4e45b-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="4e45b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e45b-140">-Confirm</span></span>
<span data-ttu-id="4e45b-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e45b-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e45b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e45b-142">-WhatIf</span></span>
<span data-ttu-id="4e45b-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e45b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e45b-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e45b-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e45b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e45b-145">CommonParameters</span></span>
<span data-ttu-id="4e45b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e45b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e45b-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e45b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e45b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e45b-148">INPUTS</span></span>

### <span data-ttu-id="4e45b-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e45b-149">None</span></span>

## <span data-ttu-id="4e45b-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e45b-150">OUTPUTS</span></span>

### <span data-ttu-id="4e45b-151">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4e45b-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="4e45b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e45b-152">NOTES</span></span>

## <span data-ttu-id="4e45b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e45b-153">RELATED LINKS</span></span>

[<span data-ttu-id="4e45b-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4e45b-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="4e45b-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4e45b-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4e45b-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4e45b-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
