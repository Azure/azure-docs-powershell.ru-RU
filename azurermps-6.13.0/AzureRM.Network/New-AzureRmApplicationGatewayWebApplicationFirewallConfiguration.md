---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 523381f4b8b5b214dc2549f52e3340adec4d9341
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569808"
---
# <span data-ttu-id="378a0-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="378a0-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="378a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="378a0-102">SYNOPSIS</span></span>
<span data-ttu-id="378a0-103">Создает конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="378a0-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="378a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="378a0-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-RequestBodyCheck <Boolean>] [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="378a0-105">DESCRIPTION</span></span>
<span data-ttu-id="378a0-106">Командлет **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** создает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="378a0-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="378a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="378a0-107">EXAMPLES</span></span>

### <span data-ttu-id="378a0-108">Пример 1: создание конфигурации брандмауэра для веб-приложения для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="378a0-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="378a0-109">Первая команда создает новую конфигурацию отключенной группы правил для группы правил с именем "запрос-942-приложение-АТАКа-SQLI" с правилом 942130 и отключением правила 942140.</span><span class="sxs-lookup"><span data-stu-id="378a0-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="378a0-110">Вторая команда создает другую отключенную конфигурацию группы правил для группы правил с именем "запрос-921-протокол-АТАКа".</span><span class="sxs-lookup"><span data-stu-id="378a0-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="378a0-111">Правила не продавались явным образом, поэтому все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="378a0-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="378a0-112">Последняя команда затем создает конфигурацию WAF с правилами брандмауэра, которые отключены в соответствии с настройками $disabledRuleGroup 1 и $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="378a0-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="378a0-113">Новая конфигурация WAF хранится в переменной $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="378a0-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="378a0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="378a0-114">PARAMETERS</span></span>

### <span data-ttu-id="378a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378a0-115">-DefaultProfile</span></span>
<span data-ttu-id="378a0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="378a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="378a0-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="378a0-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="378a0-118">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="378a0-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378a0-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="378a0-119">-Enabled</span></span>
<span data-ttu-id="378a0-120">Указывает, включена ли WAF.</span><span class="sxs-lookup"><span data-stu-id="378a0-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="378a0-121">-Исключение</span><span class="sxs-lookup"><span data-stu-id="378a0-121">-Exclusion</span></span>
<span data-ttu-id="378a0-122">Списки исключений.</span><span class="sxs-lookup"><span data-stu-id="378a0-122">The exclusion lists.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378a0-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="378a0-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="378a0-124">Максимальный предел отправки файлов (МБ).</span><span class="sxs-lookup"><span data-stu-id="378a0-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="378a0-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="378a0-125">-FirewallMode</span></span>
<span data-ttu-id="378a0-126">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="378a0-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="378a0-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="378a0-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="378a0-128">Случай</span><span class="sxs-lookup"><span data-stu-id="378a0-128">Detection</span></span>
- <span data-ttu-id="378a0-129">Диагностик</span><span class="sxs-lookup"><span data-stu-id="378a0-129">Prevention</span></span>

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

### <span data-ttu-id="378a0-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="378a0-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="378a0-131">Максимальный размер тела запроса в КБ.</span><span class="sxs-lookup"><span data-stu-id="378a0-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="378a0-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="378a0-132">-RequestBodyCheck</span></span>
<span data-ttu-id="378a0-133">Установлен ли флажок "текст запроса".</span><span class="sxs-lookup"><span data-stu-id="378a0-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="378a0-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="378a0-134">-RuleSetType</span></span>
<span data-ttu-id="378a0-135">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="378a0-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="378a0-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="378a0-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="378a0-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="378a0-137">OWASP</span></span>

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

### <span data-ttu-id="378a0-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="378a0-138">-RuleSetVersion</span></span>
<span data-ttu-id="378a0-139">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="378a0-139">The version of the rule set type.</span></span>
<span data-ttu-id="378a0-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="378a0-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="378a0-141">3,0</span><span class="sxs-lookup"><span data-stu-id="378a0-141">3.0</span></span>
- <span data-ttu-id="378a0-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="378a0-142">2.2.9</span></span>

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

### <span data-ttu-id="378a0-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="378a0-143">-Confirm</span></span>
<span data-ttu-id="378a0-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="378a0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="378a0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378a0-145">-WhatIf</span></span>
<span data-ttu-id="378a0-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="378a0-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="378a0-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="378a0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="378a0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378a0-148">CommonParameters</span></span>
<span data-ttu-id="378a0-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="378a0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378a0-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378a0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378a0-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="378a0-151">INPUTS</span></span>

### <span data-ttu-id="378a0-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="378a0-152">None</span></span>

## <span data-ttu-id="378a0-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="378a0-153">OUTPUTS</span></span>

### <span data-ttu-id="378a0-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="378a0-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="378a0-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="378a0-155">NOTES</span></span>

## <span data-ttu-id="378a0-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="378a0-156">RELATED LINKS</span></span>

[<span data-ttu-id="378a0-157">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="378a0-157">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="378a0-158">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="378a0-158">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


