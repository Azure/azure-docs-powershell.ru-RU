---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: a5f60588a0db848d0b96aa0611b8647142db2b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730028"
---
# <span data-ttu-id="36ab0-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36ab0-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="36ab0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="36ab0-103">Изменяет конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="36ab0-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="36ab0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36ab0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ab0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="36ab0-106">Командлет **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="36ab0-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="36ab0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36ab0-107">EXAMPLES</span></span>

### <span data-ttu-id="36ab0-108">Пример 1: Обновление конфигурации брандмауэра для веб-приложения "шлюз приложений"</span><span class="sxs-lookup"><span data-stu-id="36ab0-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="36ab0-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="36ab0-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="36ab0-110">Вторая команда включает конфигурацию брандмауэра для шлюза приложения, хранящуюся в $AppGw, и задает для режима брандмауэра значение "Обнаружение", RuleSetType на "OWASP", а RuleSetVersion — "3,0".</span><span class="sxs-lookup"><span data-stu-id="36ab0-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="36ab0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36ab0-111">PARAMETERS</span></span>

### <span data-ttu-id="36ab0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36ab0-112">-ApplicationGateway</span></span>
<span data-ttu-id="36ab0-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="36ab0-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="36ab0-114">Вы можете использовать командлет Get-AzApplicationGateway, чтобы получить объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="36ab0-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36ab0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ab0-115">-DefaultProfile</span></span>
<span data-ttu-id="36ab0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36ab0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ab0-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="36ab0-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="36ab0-118">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="36ab0-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="36ab0-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="36ab0-119">-Enabled</span></span>
<span data-ttu-id="36ab0-120">Указывает, включен ли брандмауэр веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="36ab0-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="36ab0-121">-Исключение</span><span class="sxs-lookup"><span data-stu-id="36ab0-121">-Exclusion</span></span>
<span data-ttu-id="36ab0-122">Списки исключений.</span><span class="sxs-lookup"><span data-stu-id="36ab0-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="36ab0-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="36ab0-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="36ab0-124">Максимальный предел отправки файлов (МБ).</span><span class="sxs-lookup"><span data-stu-id="36ab0-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="36ab0-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="36ab0-125">-FirewallMode</span></span>
<span data-ttu-id="36ab0-126">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="36ab0-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="36ab0-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="36ab0-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36ab0-128">Случай</span><span class="sxs-lookup"><span data-stu-id="36ab0-128">Detection</span></span>
- <span data-ttu-id="36ab0-129">Диагностик</span><span class="sxs-lookup"><span data-stu-id="36ab0-129">Prevention</span></span>

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

### <span data-ttu-id="36ab0-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="36ab0-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="36ab0-131">Максимальный размер тела запроса в КБ.</span><span class="sxs-lookup"><span data-stu-id="36ab0-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="36ab0-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="36ab0-132">-RequestBodyCheck</span></span>
<span data-ttu-id="36ab0-133">Установлен ли флажок "текст запроса".</span><span class="sxs-lookup"><span data-stu-id="36ab0-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="36ab0-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="36ab0-134">-RuleSetType</span></span>
<span data-ttu-id="36ab0-135">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="36ab0-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="36ab0-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="36ab0-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="36ab0-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="36ab0-137">OWASP</span></span>

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

### <span data-ttu-id="36ab0-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="36ab0-138">-RuleSetVersion</span></span>
<span data-ttu-id="36ab0-139">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="36ab0-139">The version of the rule set type.</span></span>
<span data-ttu-id="36ab0-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="36ab0-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="36ab0-141">3,0</span><span class="sxs-lookup"><span data-stu-id="36ab0-141">3.0</span></span>
- <span data-ttu-id="36ab0-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="36ab0-142">2.2.9</span></span>

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

### <span data-ttu-id="36ab0-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36ab0-143">-Confirm</span></span>
<span data-ttu-id="36ab0-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36ab0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ab0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ab0-145">-WhatIf</span></span>
<span data-ttu-id="36ab0-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36ab0-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36ab0-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36ab0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ab0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ab0-148">CommonParameters</span></span>
<span data-ttu-id="36ab0-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36ab0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ab0-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ab0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ab0-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36ab0-151">INPUTS</span></span>

### <span data-ttu-id="36ab0-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36ab0-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36ab0-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36ab0-153">OUTPUTS</span></span>

### <span data-ttu-id="36ab0-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36ab0-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36ab0-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="36ab0-155">NOTES</span></span>

## <span data-ttu-id="36ab0-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36ab0-156">RELATED LINKS</span></span>

[<span data-ttu-id="36ab0-157">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36ab0-157">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="36ab0-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36ab0-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="36ab0-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36ab0-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


