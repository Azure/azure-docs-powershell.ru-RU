---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bdfd9cb100b43f58326b9b94c4e15bb24561eadd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909722"
---
# <span data-ttu-id="0cef9-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cef9-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="0cef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0cef9-102">SYNOPSIS</span></span>
<span data-ttu-id="0cef9-103">Создает конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0cef9-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="0cef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0cef9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cef9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cef9-105">DESCRIPTION</span></span>
<span data-ttu-id="0cef9-106">Командлет **New-AzApplicationGatewayWebApplicationFirewallConfiguration** создает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="0cef9-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="0cef9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0cef9-107">EXAMPLES</span></span>

### <span data-ttu-id="0cef9-108">Пример 1: создание конфигурации брандмауэра для веб-приложения для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0cef9-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="0cef9-109">Первая команда создает новую конфигурацию отключенной группы правил для группы правил с именем "запрос-942-приложение-АТАКа-SQLI" с правилом 942130 и отключением правила 942140.</span><span class="sxs-lookup"><span data-stu-id="0cef9-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="0cef9-110">Вторая команда создает другую отключенную конфигурацию группы правил для группы правил с именем "запрос-921-протокол-АТАКа".</span><span class="sxs-lookup"><span data-stu-id="0cef9-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="0cef9-111">Правила не продавались явным образом, поэтому все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="0cef9-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="0cef9-112">Последняя команда затем создает конфигурацию WAF с правилами брандмауэра, которые отключены в соответствии с настройками $disabledRuleGroup 1 и $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="0cef9-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="0cef9-113">Новая конфигурация WAF хранится в переменной $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="0cef9-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="0cef9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0cef9-114">PARAMETERS</span></span>

### <span data-ttu-id="0cef9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cef9-115">-DefaultProfile</span></span>
<span data-ttu-id="0cef9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0cef9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cef9-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="0cef9-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="0cef9-118">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="0cef9-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="0cef9-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="0cef9-119">-Enabled</span></span>
<span data-ttu-id="0cef9-120">Указывает, включена ли WAF.</span><span class="sxs-lookup"><span data-stu-id="0cef9-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cef9-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="0cef9-121">-FirewallMode</span></span>
<span data-ttu-id="0cef9-122">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0cef9-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="0cef9-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cef9-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cef9-124">Случай</span><span class="sxs-lookup"><span data-stu-id="0cef9-124">Detection</span></span>
- <span data-ttu-id="0cef9-125">Диагностик</span><span class="sxs-lookup"><span data-stu-id="0cef9-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cef9-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="0cef9-126">-RuleSetType</span></span>
<span data-ttu-id="0cef9-127">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0cef9-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="0cef9-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cef9-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="0cef9-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="0cef9-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cef9-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="0cef9-130">-RuleSetVersion</span></span>
<span data-ttu-id="0cef9-131">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="0cef9-131">The version of the rule set type.</span></span>
<span data-ttu-id="0cef9-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0cef9-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="0cef9-133">3,0</span><span class="sxs-lookup"><span data-stu-id="0cef9-133">3.0</span></span>
- <span data-ttu-id="0cef9-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="0cef9-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cef9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cef9-135">-Confirm</span></span>
<span data-ttu-id="0cef9-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0cef9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cef9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cef9-137">-WhatIf</span></span>
<span data-ttu-id="0cef9-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0cef9-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cef9-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0cef9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cef9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cef9-140">CommonParameters</span></span>
<span data-ttu-id="0cef9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0cef9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cef9-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cef9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cef9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0cef9-143">INPUTS</span></span>

## <span data-ttu-id="0cef9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cef9-144">OUTPUTS</span></span>

### <span data-ttu-id="0cef9-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cef9-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="0cef9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0cef9-146">NOTES</span></span>

## <span data-ttu-id="0cef9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cef9-147">RELATED LINKS</span></span>

[<span data-ttu-id="0cef9-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cef9-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="0cef9-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="0cef9-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


