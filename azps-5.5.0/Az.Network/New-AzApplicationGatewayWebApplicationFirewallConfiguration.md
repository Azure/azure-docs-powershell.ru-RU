---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218596"
---
# <span data-ttu-id="3b49c-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b49c-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="3b49c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b49c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b49c-103">Создает конфигурацию WAF для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3b49c-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="3b49c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b49c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b49c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b49c-105">DESCRIPTION</span></span>
<span data-ttu-id="3b49c-106">С помощью **cmdlet New-AzApplicationGatewayWebApplicationFirewallConfiguration** создается конфигурация брандмауэра веб-приложения (WAF) для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3b49c-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="3b49c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b49c-107">EXAMPLES</span></span>

### <span data-ttu-id="3b49c-108">Пример 1. Создание конфигурации брандмауэра веб-приложения для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="3b49c-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="3b49c-109">Первая команда создает конфигурацию отключенной группы правил для группы правил REQUEST-942-APPLICATION-ATTACK-SQLI с отключаемой правилом 942130 и правилом 942140.</span><span class="sxs-lookup"><span data-stu-id="3b49c-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="3b49c-110">Вторая команда создает другую отключенную группу правил для группы правил REQUEST-921-PROTOCOL-ATTACK.</span><span class="sxs-lookup"><span data-stu-id="3b49c-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="3b49c-111">Правила не передаются отдельно, поэтому все правила группы правил будут отключены.</span><span class="sxs-lookup"><span data-stu-id="3b49c-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="3b49c-112">Затем создается конфигурация WAF с отключенными правилами брандмауэра, настроенными в $disabledRuleGroup 1 и $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="3b49c-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="3b49c-113">Новая конфигурация WAF хранится в переменной $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="3b49c-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="3b49c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b49c-114">PARAMETERS</span></span>

### <span data-ttu-id="3b49c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b49c-115">-DefaultProfile</span></span>
<span data-ttu-id="3b49c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b49c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b49c-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="3b49c-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="3b49c-118">Отключенные группы правил.</span><span class="sxs-lookup"><span data-stu-id="3b49c-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="3b49c-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="3b49c-119">-Enabled</span></span>
<span data-ttu-id="3b49c-120">Указывает на то, включено ли WAF.</span><span class="sxs-lookup"><span data-stu-id="3b49c-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="3b49c-121">-Исключение</span><span class="sxs-lookup"><span data-stu-id="3b49c-121">-Exclusion</span></span>
<span data-ttu-id="3b49c-122">Списки исключений.</span><span class="sxs-lookup"><span data-stu-id="3b49c-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="3b49c-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="3b49c-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="3b49c-124">Максимальное количество отложенных файлов в МБ.</span><span class="sxs-lookup"><span data-stu-id="3b49c-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="3b49c-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="3b49c-125">-FirewallMode</span></span>
<span data-ttu-id="3b49c-126">Определяет режим брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3b49c-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="3b49c-127">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="3b49c-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3b49c-128">Обнаружение</span><span class="sxs-lookup"><span data-stu-id="3b49c-128">Detection</span></span>
- <span data-ttu-id="3b49c-129">Предотвращение</span><span class="sxs-lookup"><span data-stu-id="3b49c-129">Prevention</span></span>

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

### <span data-ttu-id="3b49c-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="3b49c-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="3b49c-131">Максимальный размер запроса в КБ.</span><span class="sxs-lookup"><span data-stu-id="3b49c-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="3b49c-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="3b49c-132">-RequestBodyCheck</span></span>
<span data-ttu-id="3b49c-133">Будет ли проверяться тело запроса.</span><span class="sxs-lookup"><span data-stu-id="3b49c-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="3b49c-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="3b49c-134">-RuleSetType</span></span>
<span data-ttu-id="3b49c-135">Тип набора правил брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3b49c-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="3b49c-136">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="3b49c-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="3b49c-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="3b49c-137">OWASP</span></span>

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

### <span data-ttu-id="3b49c-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="3b49c-138">-RuleSetVersion</span></span>
<span data-ttu-id="3b49c-139">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="3b49c-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="3b49c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b49c-140">-Confirm</span></span>
<span data-ttu-id="3b49c-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b49c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b49c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b49c-142">-WhatIf</span></span>
<span data-ttu-id="3b49c-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b49c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b49c-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3b49c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b49c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b49c-145">CommonParameters</span></span>
<span data-ttu-id="3b49c-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b49c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b49c-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b49c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b49c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b49c-148">INPUTS</span></span>

### <span data-ttu-id="3b49c-149">Нет</span><span class="sxs-lookup"><span data-stu-id="3b49c-149">None</span></span>

## <span data-ttu-id="3b49c-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b49c-150">OUTPUTS</span></span>

### <span data-ttu-id="3b49c-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b49c-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="3b49c-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b49c-152">NOTES</span></span>

## <span data-ttu-id="3b49c-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b49c-153">RELATED LINKS</span></span>

[<span data-ttu-id="3b49c-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b49c-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="3b49c-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b49c-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


