---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248321"
---
# <span data-ttu-id="67e01-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="67e01-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="67e01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67e01-102">SYNOPSIS</span></span>
<span data-ttu-id="67e01-103">Создание правила NAT в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="67e01-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="67e01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67e01-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67e01-105">DESCRIPTION</span></span>
<span data-ttu-id="67e01-106">Командлет **New-AzFirewallNatRule** создает правило NAT для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="67e01-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="67e01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67e01-107">EXAMPLES</span></span>

### <span data-ttu-id="67e01-108">Пример 1: Создание правила для DNAT всего TCP-трафика из 10.0.0.0/24 с конечной 10.1.2.3:80 на конечный адрес 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="67e01-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="67e01-109">В этом примере создается правило, которое будет DNAT весь трафик, исходящий из 10.0.0.0/24 с конечной 10.1.2.3:80 на 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="67e01-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="67e01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67e01-110">PARAMETERS</span></span>

### <span data-ttu-id="67e01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e01-111">-DefaultProfile</span></span>
<span data-ttu-id="67e01-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67e01-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e01-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="67e01-113">-Description</span></span>
<span data-ttu-id="67e01-114">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="67e01-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="67e01-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="67e01-115">-DestinationAddress</span></span>
<span data-ttu-id="67e01-116">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="67e01-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="67e01-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="67e01-117">-DestinationPort</span></span>
<span data-ttu-id="67e01-118">Порты назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="67e01-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="67e01-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="67e01-119">-Name</span></span>
<span data-ttu-id="67e01-120">Указывает имя этого правила NAT.</span><span class="sxs-lookup"><span data-stu-id="67e01-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="67e01-121">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="67e01-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="67e01-122">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="67e01-122">-Protocol</span></span>
<span data-ttu-id="67e01-123">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="67e01-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="67e01-124">Поддерживаются протоколы TCP и UDP.</span><span class="sxs-lookup"><span data-stu-id="67e01-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="67e01-125">Разрешено специальное значение Any, означающее соответствие протоколов TCP и UDP, но не других протоколов.</span><span class="sxs-lookup"><span data-stu-id="67e01-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e01-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="67e01-126">-SourceAddress</span></span>
<span data-ttu-id="67e01-127">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="67e01-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="67e01-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="67e01-128">-SourceIpGroup</span></span>
<span data-ttu-id="67e01-129">Исходная IPGroup правила</span><span class="sxs-lookup"><span data-stu-id="67e01-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="67e01-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="67e01-130">-TranslatedAddress</span></span>
<span data-ttu-id="67e01-131">Указывает желаемый результат перевода адреса.</span><span class="sxs-lookup"><span data-stu-id="67e01-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="67e01-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="67e01-132">-TranslatedFqdn</span></span>
<span data-ttu-id="67e01-133">Преобразованное полное доменное имя для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="67e01-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="67e01-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="67e01-134">-TranslatedPort</span></span>
<span data-ttu-id="67e01-135">Указывает желаемый результат перевода порта</span><span class="sxs-lookup"><span data-stu-id="67e01-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="67e01-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67e01-136">-Confirm</span></span>
<span data-ttu-id="67e01-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67e01-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e01-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e01-138">-WhatIf</span></span>
<span data-ttu-id="67e01-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67e01-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e01-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67e01-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e01-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e01-141">CommonParameters</span></span>
<span data-ttu-id="67e01-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67e01-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e01-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e01-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e01-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67e01-144">INPUTS</span></span>

### <span data-ttu-id="67e01-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="67e01-145">None</span></span>

## <span data-ttu-id="67e01-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67e01-146">OUTPUTS</span></span>

### <span data-ttu-id="67e01-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="67e01-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="67e01-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="67e01-148">NOTES</span></span>

## <span data-ttu-id="67e01-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67e01-149">RELATED LINKS</span></span>

[<span data-ttu-id="67e01-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="67e01-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="67e01-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="67e01-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="67e01-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="67e01-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
