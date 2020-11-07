---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: cb66bda25d1353fcfaac732588817ce515fef746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902709"
---
# <span data-ttu-id="c2a66-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2a66-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="c2a66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2a66-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a66-103">Создает конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c2a66-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="c2a66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2a66-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a66-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2a66-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a66-106">Командлет **New-AzApplicationGatewayWebApplicationFirewallConfiguration** создает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a66-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="c2a66-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2a66-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a66-108">Пример 1: создание конфигурации брандмауэра для веб-приложения для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="c2a66-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="c2a66-109">Первая команда создает новую конфигурацию отключенной группы правил для группы правил с именем "запрос-942-приложение-АТАКа-SQLI" с правилом 942130 и отключением правила 942140.</span><span class="sxs-lookup"><span data-stu-id="c2a66-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="c2a66-110">Вторая команда создает другую отключенную конфигурацию группы правил для группы правил с именем "запрос-921-протокол-АТАКа".</span><span class="sxs-lookup"><span data-stu-id="c2a66-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="c2a66-111">Правила не продавались явным образом, поэтому все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="c2a66-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="c2a66-112">Последняя команда затем создает конфигурацию WAF с правилами брандмауэра, которые отключены в соответствии с настройками $disabledRuleGroup 1 и $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="c2a66-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="c2a66-113">Новая конфигурация WAF хранится в переменной $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="c2a66-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="c2a66-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2a66-114">PARAMETERS</span></span>

### <span data-ttu-id="c2a66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a66-115">-DefaultProfile</span></span>
<span data-ttu-id="c2a66-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2a66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2a66-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="c2a66-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="c2a66-118">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="c2a66-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a66-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="c2a66-119">-Enabled</span></span>
<span data-ttu-id="c2a66-120">Указывает, включена ли WAF.</span><span class="sxs-lookup"><span data-stu-id="c2a66-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="c2a66-121">-Исключение</span><span class="sxs-lookup"><span data-stu-id="c2a66-121">-Exclusion</span></span>
<span data-ttu-id="c2a66-122">Списки исключений.</span><span class="sxs-lookup"><span data-stu-id="c2a66-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a66-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="c2a66-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="c2a66-124">Максимальный предел отправки файлов (МБ).</span><span class="sxs-lookup"><span data-stu-id="c2a66-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a66-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="c2a66-125">-FirewallMode</span></span>
<span data-ttu-id="c2a66-126">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c2a66-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="c2a66-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2a66-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2a66-128">Случай</span><span class="sxs-lookup"><span data-stu-id="c2a66-128">Detection</span></span>
- <span data-ttu-id="c2a66-129">Диагностик</span><span class="sxs-lookup"><span data-stu-id="c2a66-129">Prevention</span></span>

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

### <span data-ttu-id="c2a66-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="c2a66-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="c2a66-131">Максимальный размер тела запроса в КБ.</span><span class="sxs-lookup"><span data-stu-id="c2a66-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a66-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="c2a66-132">-RequestBodyCheck</span></span>
<span data-ttu-id="c2a66-133">Установлен ли флажок "текст запроса".</span><span class="sxs-lookup"><span data-stu-id="c2a66-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a66-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="c2a66-134">-RuleSetType</span></span>
<span data-ttu-id="c2a66-135">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c2a66-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="c2a66-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c2a66-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="c2a66-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="c2a66-137">OWASP</span></span>

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

### <span data-ttu-id="c2a66-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="c2a66-138">-RuleSetVersion</span></span>
<span data-ttu-id="c2a66-139">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="c2a66-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a66-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2a66-140">-Confirm</span></span>
<span data-ttu-id="c2a66-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2a66-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a66-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a66-142">-WhatIf</span></span>
<span data-ttu-id="c2a66-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2a66-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2a66-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2a66-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a66-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a66-145">CommonParameters</span></span>
<span data-ttu-id="c2a66-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2a66-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a66-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a66-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a66-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2a66-148">INPUTS</span></span>

### <span data-ttu-id="c2a66-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="c2a66-149">None</span></span>

## <span data-ttu-id="c2a66-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2a66-150">OUTPUTS</span></span>

### <span data-ttu-id="c2a66-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2a66-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="c2a66-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2a66-152">NOTES</span></span>

## <span data-ttu-id="c2a66-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2a66-153">RELATED LINKS</span></span>

[<span data-ttu-id="c2a66-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2a66-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="c2a66-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2a66-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


