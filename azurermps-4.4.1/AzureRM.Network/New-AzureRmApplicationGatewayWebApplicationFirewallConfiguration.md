---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 281a4a0d935d73777f7fdd693f3d32982b2da47a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563880"
---
# <span data-ttu-id="e1c09-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1c09-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e1c09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1c09-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c09-103">Создает конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e1c09-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1c09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1c09-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c09-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c09-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c09-106">Командлет **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** создает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c09-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="e1c09-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1c09-107">EXAMPLES</span></span>

### <span data-ttu-id="e1c09-108">Пример 1: создание конфигурации брандмауэра для веб-приложения для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="e1c09-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="e1c09-109">Первая команда создает новую конфигурацию отключенной группы правил для группы правил с именем "запрос-942-приложение-АТАКа-SQLI" с правилом 942130 и отключением правила 942140.</span><span class="sxs-lookup"><span data-stu-id="e1c09-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="e1c09-110">Вторая команда создает другую отключенную конфигурацию группы правил для группы правил с именем "запрос-921-протокол-АТАКа".</span><span class="sxs-lookup"><span data-stu-id="e1c09-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="e1c09-111">Правила не продавались явным образом, поэтому все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="e1c09-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="e1c09-112">Последняя команда затем создает конфигурацию WAF с правилами брандмауэра, которые отключены в соответствии с настройками $disabledRuleGroup 1 и $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="e1c09-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="e1c09-113">Новая конфигурация WAF хранится в переменной $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="e1c09-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="e1c09-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1c09-114">PARAMETERS</span></span>

### <span data-ttu-id="e1c09-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="e1c09-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="e1c09-116">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="e1c09-116">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c09-117">-Включено</span><span class="sxs-lookup"><span data-stu-id="e1c09-117">-Enabled</span></span>
<span data-ttu-id="e1c09-118">Указывает, включена ли WAF.</span><span class="sxs-lookup"><span data-stu-id="e1c09-118">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c09-119">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="e1c09-119">-FirewallMode</span></span>
<span data-ttu-id="e1c09-120">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="e1c09-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="e1c09-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1c09-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1c09-122">Случай</span><span class="sxs-lookup"><span data-stu-id="e1c09-122">Detection</span></span>
- <span data-ttu-id="e1c09-123">Диагностик</span><span class="sxs-lookup"><span data-stu-id="e1c09-123">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c09-124">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="e1c09-124">-RuleSetType</span></span>
<span data-ttu-id="e1c09-125">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="e1c09-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="e1c09-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1c09-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="e1c09-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="e1c09-127">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c09-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="e1c09-128">-RuleSetVersion</span></span>
<span data-ttu-id="e1c09-129">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="e1c09-129">The version of the rule set type.</span></span>
<span data-ttu-id="e1c09-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e1c09-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="e1c09-131">3,0</span><span class="sxs-lookup"><span data-stu-id="e1c09-131">3.0</span></span>
- <span data-ttu-id="e1c09-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="e1c09-132">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c09-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1c09-133">-Confirm</span></span>
<span data-ttu-id="e1c09-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1c09-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1c09-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c09-135">-WhatIf</span></span>
<span data-ttu-id="e1c09-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1c09-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1c09-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1c09-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1c09-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c09-138">-DefaultProfile</span></span>
<span data-ttu-id="e1c09-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c09-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1c09-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c09-140">CommonParameters</span></span>
<span data-ttu-id="e1c09-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1c09-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c09-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1c09-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c09-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1c09-143">INPUTS</span></span>

## <span data-ttu-id="e1c09-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1c09-144">OUTPUTS</span></span>

### <span data-ttu-id="e1c09-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1c09-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e1c09-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1c09-146">NOTES</span></span>

## <span data-ttu-id="e1c09-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1c09-147">RELATED LINKS</span></span>

[<span data-ttu-id="e1c09-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1c09-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e1c09-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1c09-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


