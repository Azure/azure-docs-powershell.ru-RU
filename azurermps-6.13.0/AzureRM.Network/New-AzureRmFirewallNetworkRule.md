---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560883"
---
# <span data-ttu-id="4c78f-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4c78f-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="4c78f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c78f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c78f-103">Создание сетевого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4c78f-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c78f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c78f-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c78f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c78f-105">DESCRIPTION</span></span>
<span data-ttu-id="4c78f-106">Командлет **New-AzureRmFirewallNetworkRule** создает сетевое правило для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4c78f-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="4c78f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c78f-107">EXAMPLES</span></span>

### <span data-ttu-id="4c78f-108">1: Создание правила для всего трафика TCP</span><span class="sxs-lookup"><span data-stu-id="4c78f-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="4c78f-109">В этом примере создается правило для всего трафика TCP.</span><span class="sxs-lookup"><span data-stu-id="4c78f-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="4c78f-110">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4c78f-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4c78f-111">2. Создайте правило для всего TCP-трафика с 10.0.0.0 на 60.1.5.0:4040</span><span class="sxs-lookup"><span data-stu-id="4c78f-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="4c78f-112">В этом примере создается правило для всего трафика TCP из 10.0.0.0 в 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4c78f-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4c78f-113">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4c78f-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="4c78f-114">3. Создайте правило для всего трафика TCP и ICMP из любого источника в 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="4c78f-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="4c78f-115">В этом примере создается правило для всего трафика TCP из 10.0.0.0 в 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4c78f-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="4c78f-116">Пользователь следит за тем, что трафик будет разрешен или отвергнут для правила на основе коллекции правил, с которой он связан.</span><span class="sxs-lookup"><span data-stu-id="4c78f-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="4c78f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c78f-117">PARAMETERS</span></span>

### <span data-ttu-id="4c78f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c78f-118">-DefaultProfile</span></span>
<span data-ttu-id="4c78f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c78f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c78f-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="4c78f-120">-Description</span></span>
<span data-ttu-id="4c78f-121">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="4c78f-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="4c78f-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="4c78f-122">-DestinationAddress</span></span>
<span data-ttu-id="4c78f-123">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="4c78f-123">The destination addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c78f-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="4c78f-124">-DestinationPort</span></span>
<span data-ttu-id="4c78f-125">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="4c78f-125">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c78f-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c78f-126">-Name</span></span>
<span data-ttu-id="4c78f-127">Указывает имя сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="4c78f-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="4c78f-128">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4c78f-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4c78f-129">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="4c78f-129">-Protocol</span></span>
<span data-ttu-id="4c78f-130">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="4c78f-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="4c78f-131">Возможные значения: TCP, UDP, ICMP и ANY.</span><span class="sxs-lookup"><span data-stu-id="4c78f-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c78f-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="4c78f-132">-SourceAddress</span></span>
<span data-ttu-id="4c78f-133">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="4c78f-133">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c78f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c78f-134">-Confirm</span></span>
<span data-ttu-id="4c78f-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c78f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c78f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c78f-136">-WhatIf</span></span>
<span data-ttu-id="4c78f-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c78f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c78f-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c78f-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c78f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c78f-139">CommonParameters</span></span>
<span data-ttu-id="4c78f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c78f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c78f-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c78f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c78f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c78f-142">INPUTS</span></span>

### <span data-ttu-id="4c78f-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c78f-143">None</span></span>
<span data-ttu-id="4c78f-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4c78f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c78f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c78f-145">OUTPUTS</span></span>

### <span data-ttu-id="4c78f-146">Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4c78f-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="4c78f-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c78f-147">NOTES</span></span>

## <span data-ttu-id="4c78f-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c78f-148">RELATED LINKS</span></span>

[<span data-ttu-id="4c78f-149">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4c78f-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="4c78f-150">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4c78f-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="4c78f-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4c78f-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
