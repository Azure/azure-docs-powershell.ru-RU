---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 3b2de5d139c8addb448ac76609e13becf2e0153c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731961"
---
# <span data-ttu-id="cf880-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf880-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="cf880-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf880-102">SYNOPSIS</span></span>
<span data-ttu-id="cf880-103">Изменяет конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cf880-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf880-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf880-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-RequestBodyCheck <Boolean>] [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf880-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf880-105">DESCRIPTION</span></span>
<span data-ttu-id="cf880-106">Командлет **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cf880-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="cf880-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf880-107">EXAMPLES</span></span>

### <span data-ttu-id="cf880-108">Пример 1: Обновление конфигурации брандмауэра для веб-приложения "шлюз приложений"</span><span class="sxs-lookup"><span data-stu-id="cf880-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="cf880-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cf880-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cf880-110">Вторая команда включает конфигурацию брандмауэра для шлюза приложения, хранящуюся в $AppGw, и задает для режима брандмауэра значение "Обнаружение", RuleSetType на "OWASP", а RuleSetVersion — "3,0".</span><span class="sxs-lookup"><span data-stu-id="cf880-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="cf880-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf880-111">PARAMETERS</span></span>

### <span data-ttu-id="cf880-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf880-112">-ApplicationGateway</span></span>
<span data-ttu-id="cf880-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="cf880-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="cf880-114">Вы можете использовать командлет Get-AzureRmApplicationGateway, чтобы получить объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="cf880-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="cf880-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf880-115">-DefaultProfile</span></span>
<span data-ttu-id="cf880-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf880-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf880-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="cf880-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="cf880-118">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="cf880-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="cf880-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="cf880-119">-Enabled</span></span>
<span data-ttu-id="cf880-120">Указывает, включен ли брандмауэр веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cf880-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="cf880-121">-Исключение</span><span class="sxs-lookup"><span data-stu-id="cf880-121">-Exclusion</span></span>
<span data-ttu-id="cf880-122">Списки исключений.</span><span class="sxs-lookup"><span data-stu-id="cf880-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="cf880-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="cf880-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="cf880-124">Максимальный предел отправки файлов (МБ).</span><span class="sxs-lookup"><span data-stu-id="cf880-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="cf880-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="cf880-125">-FirewallMode</span></span>
<span data-ttu-id="cf880-126">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cf880-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="cf880-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cf880-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cf880-128">Случай</span><span class="sxs-lookup"><span data-stu-id="cf880-128">Detection</span></span>
- <span data-ttu-id="cf880-129">Диагностик</span><span class="sxs-lookup"><span data-stu-id="cf880-129">Prevention</span></span>

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

### <span data-ttu-id="cf880-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="cf880-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="cf880-131">Максимальный размер тела запроса в КБ.</span><span class="sxs-lookup"><span data-stu-id="cf880-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="cf880-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="cf880-132">-RequestBodyCheck</span></span>
<span data-ttu-id="cf880-133">Установлен ли флажок "текст запроса".</span><span class="sxs-lookup"><span data-stu-id="cf880-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="cf880-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="cf880-134">-RuleSetType</span></span>
<span data-ttu-id="cf880-135">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cf880-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="cf880-136">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cf880-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="cf880-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="cf880-137">OWASP</span></span>

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

### <span data-ttu-id="cf880-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="cf880-138">-RuleSetVersion</span></span>
<span data-ttu-id="cf880-139">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="cf880-139">The version of the rule set type.</span></span>
<span data-ttu-id="cf880-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cf880-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="cf880-141">3,0</span><span class="sxs-lookup"><span data-stu-id="cf880-141">3.0</span></span>
- <span data-ttu-id="cf880-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="cf880-142">2.2.9</span></span>

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

### <span data-ttu-id="cf880-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf880-143">-Confirm</span></span>
<span data-ttu-id="cf880-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf880-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf880-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf880-145">-WhatIf</span></span>
<span data-ttu-id="cf880-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf880-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf880-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf880-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf880-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf880-148">CommonParameters</span></span>
<span data-ttu-id="cf880-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf880-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf880-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf880-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf880-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf880-151">INPUTS</span></span>

### <span data-ttu-id="cf880-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf880-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="cf880-153">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cf880-153">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="cf880-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf880-154">OUTPUTS</span></span>

### <span data-ttu-id="cf880-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf880-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cf880-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf880-156">NOTES</span></span>

## <span data-ttu-id="cf880-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf880-157">RELATED LINKS</span></span>

[<span data-ttu-id="cf880-158">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cf880-158">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="cf880-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf880-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="cf880-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf880-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


