---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565858"
---
# <span data-ttu-id="01c01-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="01c01-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="01c01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01c01-102">SYNOPSIS</span></span>
<span data-ttu-id="01c01-103">Создание правила NAT в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="01c01-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01c01-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01c01-105">DESCRIPTION</span></span>
<span data-ttu-id="01c01-106">Командлет **New-AzureRmFirewallNatRule** создает правило NAT для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="01c01-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="01c01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01c01-107">EXAMPLES</span></span>

### <span data-ttu-id="01c01-108">1: Создание правила для DNAT всего TCP-трафика из 10.0.0.0/24 с конечной 10.1.2.3:80 на конечный адрес 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="01c01-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="01c01-109">В этом примере создается правило, которое будет DNAT весь трафик, исходящий из 10.0.0.0/24 с конечной 10.1.2.3:80 на 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="01c01-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="01c01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01c01-110">PARAMETERS</span></span>

### <span data-ttu-id="01c01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c01-111">-DefaultProfile</span></span>
<span data-ttu-id="01c01-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01c01-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c01-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="01c01-113">-Description</span></span>
<span data-ttu-id="01c01-114">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="01c01-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="01c01-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="01c01-115">-DestinationAddress</span></span>
<span data-ttu-id="01c01-116">Конечные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="01c01-116">The destination addresses of the rule.</span></span>

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

### <span data-ttu-id="01c01-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="01c01-117">-DestinationPort</span></span>
<span data-ttu-id="01c01-118">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="01c01-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="01c01-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01c01-119">-Name</span></span>
<span data-ttu-id="01c01-120">Указывает имя этого правила NAT.</span><span class="sxs-lookup"><span data-stu-id="01c01-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="01c01-121">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="01c01-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="01c01-122">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="01c01-122">-Protocol</span></span>
<span data-ttu-id="01c01-123">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="01c01-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="01c01-124">Поддерживаются протоколы TCP и UDP.</span><span class="sxs-lookup"><span data-stu-id="01c01-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="01c01-125">Разрешено специальное значение Any, означающее соответствие протоколов TCP и UDP, но не других протоколов.</span><span class="sxs-lookup"><span data-stu-id="01c01-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01c01-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="01c01-126">-SourceAddress</span></span>
<span data-ttu-id="01c01-127">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="01c01-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="01c01-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="01c01-128">-TranslatedAddress</span></span>
<span data-ttu-id="01c01-129">Указывает желаемый результат перевода адреса.</span><span class="sxs-lookup"><span data-stu-id="01c01-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="01c01-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="01c01-130">-TranslatedPort</span></span>
<span data-ttu-id="01c01-131">Указывает желаемый результат перевода порта</span><span class="sxs-lookup"><span data-stu-id="01c01-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="01c01-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01c01-132">-Confirm</span></span>
<span data-ttu-id="01c01-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01c01-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c01-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c01-134">-WhatIf</span></span>
<span data-ttu-id="01c01-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01c01-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c01-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01c01-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c01-137">CommonParameters</span></span>
<span data-ttu-id="01c01-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01c01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c01-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c01-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c01-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01c01-140">INPUTS</span></span>

### <span data-ttu-id="01c01-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="01c01-141">None</span></span>
<span data-ttu-id="01c01-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="01c01-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01c01-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01c01-143">OUTPUTS</span></span>

### <span data-ttu-id="01c01-144">Microsoft. Azure. Commands. Network. Models. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="01c01-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="01c01-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="01c01-145">NOTES</span></span>

## <span data-ttu-id="01c01-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01c01-146">RELATED LINKS</span></span>

[<span data-ttu-id="01c01-147">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="01c01-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="01c01-148">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="01c01-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="01c01-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="01c01-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
