---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 06cac261d368dfafa19b96b42945ed9cda613122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730336"
---
# <span data-ttu-id="4c511-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4c511-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="4c511-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c511-102">SYNOPSIS</span></span>
<span data-ttu-id="4c511-103">Создание сетевого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4c511-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="4c511-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c511-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c511-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c511-105">DESCRIPTION</span></span>
<span data-ttu-id="4c511-106">Командлет **New-AzFirewallNetworkRule** создает сетевое правило для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4c511-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="4c511-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c511-107">EXAMPLES</span></span>

### <span data-ttu-id="4c511-108">1: Создание правила для всего трафика TCP</span><span class="sxs-lookup"><span data-stu-id="4c511-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="4c511-109">В этом примере создается правило для всего трафика TCP.</span><span class="sxs-lookup"><span data-stu-id="4c511-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="4c511-110">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4c511-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4c511-111">2. Создайте правило для всего TCP-трафика с 10.0.0.0 на 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="4c511-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="4c511-112">В этом примере создается правило для всего трафика TCP из 10.0.0.0 в 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4c511-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4c511-113">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4c511-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4c511-114">3. Создайте правило для всего трафика TCP и ICMP из любого источника в 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="4c511-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="4c511-115">В этом примере создается правило для всего трафика TCP из 10.0.0.0 в 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4c511-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4c511-116">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4c511-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="4c511-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c511-117">PARAMETERS</span></span>

### <span data-ttu-id="4c511-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c511-118">-DefaultProfile</span></span>
<span data-ttu-id="4c511-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c511-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c511-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="4c511-120">-Description</span></span>
<span data-ttu-id="4c511-121">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="4c511-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="4c511-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4c511-122">-DestinationAddress</span></span>
<span data-ttu-id="4c511-123">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="4c511-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="4c511-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4c511-124">-DestinationPort</span></span>
<span data-ttu-id="4c511-125">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="4c511-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="4c511-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c511-126">-Name</span></span>
<span data-ttu-id="4c511-127">Указывает имя сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="4c511-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="4c511-128">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4c511-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4c511-129">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="4c511-129">-Protocol</span></span>
<span data-ttu-id="4c511-130">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="4c511-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="4c511-131">Возможные значения: TCP, UDP, ICMP и ANY.</span><span class="sxs-lookup"><span data-stu-id="4c511-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="4c511-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4c511-132">-SourceAddress</span></span>
<span data-ttu-id="4c511-133">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="4c511-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="4c511-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c511-134">-Confirm</span></span>
<span data-ttu-id="4c511-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c511-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c511-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c511-136">-WhatIf</span></span>
<span data-ttu-id="4c511-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c511-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c511-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c511-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c511-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c511-139">CommonParameters</span></span>
<span data-ttu-id="4c511-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c511-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c511-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c511-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c511-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c511-142">INPUTS</span></span>

### <span data-ttu-id="4c511-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c511-143">None</span></span>

## <span data-ttu-id="4c511-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c511-144">OUTPUTS</span></span>

### <span data-ttu-id="4c511-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4c511-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="4c511-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c511-146">NOTES</span></span>

## <span data-ttu-id="4c511-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c511-147">RELATED LINKS</span></span>

[<span data-ttu-id="4c511-148">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4c511-148">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="4c511-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4c511-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4c511-150">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4c511-150">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
