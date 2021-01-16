---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: efe8821ee1ec0978c42aa59fc856b4d6e07fa7dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394396"
---
# <span data-ttu-id="d1a56-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d1a56-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="d1a56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1a56-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a56-103">Создает правило NAT брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d1a56-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="d1a56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1a56-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a56-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1a56-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a56-106">С **помощью cmdlet New-AzFirewallNatRule** создается правило NAT для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a56-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="d1a56-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1a56-107">EXAMPLES</span></span>

### <span data-ttu-id="d1a56-108">Пример 1. Создание правила для всего TCP-трафика TCP с 10.0.0.0/24 с назначением 10.1.2.3:80 до 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="d1a56-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="d1a56-109">В этом примере создается правило, которое будет соотнося с 10.0.0.0.24 и назначением 10.1.2.3:80 по 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="d1a56-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="d1a56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1a56-110">PARAMETERS</span></span>

### <span data-ttu-id="d1a56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a56-111">-DefaultProfile</span></span>
<span data-ttu-id="d1a56-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a56-113">-Description</span><span class="sxs-lookup"><span data-stu-id="d1a56-113">-Description</span></span>
<span data-ttu-id="d1a56-114">Указывает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="d1a56-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="d1a56-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d1a56-115">-DestinationAddress</span></span>
<span data-ttu-id="d1a56-116">Адреса назначения правила</span><span class="sxs-lookup"><span data-stu-id="d1a56-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="d1a56-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d1a56-117">-DestinationPort</span></span>
<span data-ttu-id="d1a56-118">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="d1a56-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="d1a56-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d1a56-119">-Name</span></span>
<span data-ttu-id="d1a56-120">Указывает имя правила NAT.</span><span class="sxs-lookup"><span data-stu-id="d1a56-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="d1a56-121">Имя должно быть уникальным в наборе правил.</span><span class="sxs-lookup"><span data-stu-id="d1a56-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d1a56-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d1a56-122">-Protocol</span></span>
<span data-ttu-id="d1a56-123">Определяет тип трафика, отфильтрованного этим правилом.</span><span class="sxs-lookup"><span data-stu-id="d1a56-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="d1a56-124">Поддерживаются протоколы TCP и UDP.</span><span class="sxs-lookup"><span data-stu-id="d1a56-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="d1a56-125">Допускается специальное значение "Любое", то есть оно будет соответствовать как TCP, так и UDP, но не другим протоколам.</span><span class="sxs-lookup"><span data-stu-id="d1a56-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="d1a56-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d1a56-126">-SourceAddress</span></span>
<span data-ttu-id="d1a56-127">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="d1a56-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d1a56-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="d1a56-128">-SourceIpGroup</span></span>
<span data-ttu-id="d1a56-129">Ipgroup-источник правила</span><span class="sxs-lookup"><span data-stu-id="d1a56-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="d1a56-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="d1a56-130">-TranslatedAddress</span></span>
<span data-ttu-id="d1a56-131">Определяет желаемый результат перевода адреса.</span><span class="sxs-lookup"><span data-stu-id="d1a56-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="d1a56-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="d1a56-132">-TranslatedFqdn</span></span>
<span data-ttu-id="d1a56-133">Переведенное FQDN для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="d1a56-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="d1a56-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="d1a56-134">-TranslatedPort</span></span>
<span data-ttu-id="d1a56-135">Определяет желаемый результат перевода порта.</span><span class="sxs-lookup"><span data-stu-id="d1a56-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="d1a56-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1a56-136">-Confirm</span></span>
<span data-ttu-id="d1a56-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d1a56-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a56-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a56-138">-WhatIf</span></span>
<span data-ttu-id="d1a56-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a56-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a56-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1a56-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a56-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a56-141">CommonParameters</span></span>
<span data-ttu-id="d1a56-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a56-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a56-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a56-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a56-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1a56-144">INPUTS</span></span>

### <span data-ttu-id="d1a56-145">Нет</span><span class="sxs-lookup"><span data-stu-id="d1a56-145">None</span></span>

## <span data-ttu-id="d1a56-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1a56-146">OUTPUTS</span></span>

### <span data-ttu-id="d1a56-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d1a56-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="d1a56-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1a56-148">NOTES</span></span>

## <span data-ttu-id="d1a56-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1a56-149">RELATED LINKS</span></span>

[<span data-ttu-id="d1a56-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d1a56-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="d1a56-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d1a56-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d1a56-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d1a56-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
