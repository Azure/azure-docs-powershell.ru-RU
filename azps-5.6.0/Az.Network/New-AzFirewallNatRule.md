---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: 2bbac9bebd79f1ca51a7defd4c57589764b2c34e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985799"
---
# <span data-ttu-id="adb12-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="adb12-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="adb12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb12-102">SYNOPSIS</span></span>
<span data-ttu-id="adb12-103">Создает правило NAT брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="adb12-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="adb12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="adb12-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-TranslatedAddress <String>] [-TranslatedFqdn <String>] -TranslatedPort <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb12-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adb12-105">DESCRIPTION</span></span>
<span data-ttu-id="adb12-106">Для **брандмауэра Azure** создается правило NAT.</span><span class="sxs-lookup"><span data-stu-id="adb12-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="adb12-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="adb12-107">EXAMPLES</span></span>

### <span data-ttu-id="adb12-108">Пример 1. Создание правила для всего TCP-трафика TCP с 10.0.0.0/24 с назначением 10.1.2.3:80 до 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="adb12-108">Example 1: Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```powershell
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="adb12-109">В этом примере создается правило, которое будет соотнося с 10.0.0.0.24 и назначением 10.1.2.3:80 по 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="adb12-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="adb12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adb12-110">PARAMETERS</span></span>

### <span data-ttu-id="adb12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb12-111">-DefaultProfile</span></span>
<span data-ttu-id="adb12-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adb12-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adb12-113">-Description</span><span class="sxs-lookup"><span data-stu-id="adb12-113">-Description</span></span>
<span data-ttu-id="adb12-114">Указывает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="adb12-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="adb12-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="adb12-115">-DestinationAddress</span></span>
<span data-ttu-id="adb12-116">Адреса назначения правила</span><span class="sxs-lookup"><span data-stu-id="adb12-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="adb12-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="adb12-117">-DestinationPort</span></span>
<span data-ttu-id="adb12-118">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="adb12-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="adb12-119">-Name</span><span class="sxs-lookup"><span data-stu-id="adb12-119">-Name</span></span>
<span data-ttu-id="adb12-120">Указывает имя правила NAT.</span><span class="sxs-lookup"><span data-stu-id="adb12-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="adb12-121">Имя должно быть уникальным в наборе правил.</span><span class="sxs-lookup"><span data-stu-id="adb12-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="adb12-122">-Protocol</span><span class="sxs-lookup"><span data-stu-id="adb12-122">-Protocol</span></span>
<span data-ttu-id="adb12-123">Определяет тип трафика, который нужно отфильтровать по этому правилу.</span><span class="sxs-lookup"><span data-stu-id="adb12-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="adb12-124">Поддерживаются протоколы TCP и UDP.</span><span class="sxs-lookup"><span data-stu-id="adb12-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="adb12-125">Допускается специальное значение "Any", то есть оно будет соответствовать TCP и UDP, но не другим протоколам.</span><span class="sxs-lookup"><span data-stu-id="adb12-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

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

### <span data-ttu-id="adb12-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="adb12-126">-SourceAddress</span></span>
<span data-ttu-id="adb12-127">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="adb12-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="adb12-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="adb12-128">-SourceIpGroup</span></span>
<span data-ttu-id="adb12-129">Ipgroup-источник правила</span><span class="sxs-lookup"><span data-stu-id="adb12-129">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="adb12-130">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="adb12-130">-TranslatedAddress</span></span>
<span data-ttu-id="adb12-131">Определяет желаемый результат перевода адреса.</span><span class="sxs-lookup"><span data-stu-id="adb12-131">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="adb12-132">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="adb12-132">-TranslatedFqdn</span></span>
<span data-ttu-id="adb12-133">Переведенное FQDN для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="adb12-133">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="adb12-134">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="adb12-134">-TranslatedPort</span></span>
<span data-ttu-id="adb12-135">Определяет желаемый результат перевода порта.</span><span class="sxs-lookup"><span data-stu-id="adb12-135">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="adb12-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adb12-136">-Confirm</span></span>
<span data-ttu-id="adb12-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb12-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb12-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb12-138">-WhatIf</span></span>
<span data-ttu-id="adb12-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adb12-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb12-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="adb12-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb12-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb12-141">CommonParameters</span></span>
<span data-ttu-id="adb12-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb12-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb12-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adb12-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb12-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adb12-144">INPUTS</span></span>

### <span data-ttu-id="adb12-145">Нет</span><span class="sxs-lookup"><span data-stu-id="adb12-145">None</span></span>

## <span data-ttu-id="adb12-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="adb12-146">OUTPUTS</span></span>

### <span data-ttu-id="adb12-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="adb12-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="adb12-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="adb12-148">NOTES</span></span>

## <span data-ttu-id="adb12-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adb12-149">RELATED LINKS</span></span>

[<span data-ttu-id="adb12-150">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="adb12-150">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="adb12-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="adb12-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="adb12-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="adb12-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
