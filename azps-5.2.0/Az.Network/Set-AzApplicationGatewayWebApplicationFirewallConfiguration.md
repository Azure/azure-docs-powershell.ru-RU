---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400156"
---
# <span data-ttu-id="97c73-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c73-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="97c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97c73-102">SYNOPSIS</span></span>
<span data-ttu-id="97c73-103">Изменяет конфигурацию WAF шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="97c73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97c73-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c73-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97c73-105">DESCRIPTION</span></span>
<span data-ttu-id="97c73-106">Cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию брандмауэра веб-приложения (WAF) шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="97c73-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97c73-107">EXAMPLES</span></span>

### <span data-ttu-id="97c73-108">Пример 1. Обновление конфигурации брандмауэра веб-приложения шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="97c73-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="97c73-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="97c73-110">Вторая команда включает конфигурацию брандмауэра для шлюза приложения, храняого в $AppGw, и задает для брандмауэра режим "Обнаружение", RuleSetType — "OWASP", а Для RuleSetVersion — "3.0".</span><span class="sxs-lookup"><span data-stu-id="97c73-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="97c73-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97c73-111">PARAMETERS</span></span>

### <span data-ttu-id="97c73-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97c73-112">-ApplicationGateway</span></span>
<span data-ttu-id="97c73-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="97c73-114">Вы можете использовать Get-AzApplicationGateway для получения объекта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="97c73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c73-115">-DefaultProfile</span></span>
<span data-ttu-id="97c73-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97c73-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c73-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="97c73-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="97c73-118">Отключенные группы правил.</span><span class="sxs-lookup"><span data-stu-id="97c73-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="97c73-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="97c73-119">-Enabled</span></span>
<span data-ttu-id="97c73-120">Указывает на то, включен ли брандмауэр веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="97c73-121">-Исключение</span><span class="sxs-lookup"><span data-stu-id="97c73-121">-Exclusion</span></span>
<span data-ttu-id="97c73-122">Списки исключений.</span><span class="sxs-lookup"><span data-stu-id="97c73-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="97c73-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="97c73-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="97c73-124">Максимальное количество отложенных файлов в МБ.</span><span class="sxs-lookup"><span data-stu-id="97c73-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="97c73-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="97c73-125">-FirewallMode</span></span>
<span data-ttu-id="97c73-126">Определяет режим брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="97c73-127">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="97c73-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="97c73-128">Обнаружение</span><span class="sxs-lookup"><span data-stu-id="97c73-128">Detection</span></span>
- <span data-ttu-id="97c73-129">Предотвращение</span><span class="sxs-lookup"><span data-stu-id="97c73-129">Prevention</span></span>

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

### <span data-ttu-id="97c73-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="97c73-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="97c73-131">Максимальный размер запроса в КБ.</span><span class="sxs-lookup"><span data-stu-id="97c73-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="97c73-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="97c73-132">-RequestBodyCheck</span></span>
<span data-ttu-id="97c73-133">Будет ли проверяться тело запроса.</span><span class="sxs-lookup"><span data-stu-id="97c73-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="97c73-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="97c73-134">-RuleSetType</span></span>
<span data-ttu-id="97c73-135">Тип набора правил брандмауэра веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="97c73-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="97c73-136">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="97c73-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="97c73-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="97c73-137">OWASP</span></span>

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

### <span data-ttu-id="97c73-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="97c73-138">-RuleSetVersion</span></span>
<span data-ttu-id="97c73-139">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="97c73-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="97c73-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97c73-140">-Confirm</span></span>
<span data-ttu-id="97c73-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c73-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c73-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c73-142">-WhatIf</span></span>
<span data-ttu-id="97c73-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c73-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97c73-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97c73-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c73-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c73-145">CommonParameters</span></span>
<span data-ttu-id="97c73-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c73-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c73-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c73-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c73-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97c73-148">INPUTS</span></span>

### <span data-ttu-id="97c73-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97c73-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97c73-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97c73-150">OUTPUTS</span></span>

### <span data-ttu-id="97c73-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97c73-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97c73-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97c73-152">NOTES</span></span>

## <span data-ttu-id="97c73-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97c73-153">RELATED LINKS</span></span>

[<span data-ttu-id="97c73-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97c73-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="97c73-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c73-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="97c73-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="97c73-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


