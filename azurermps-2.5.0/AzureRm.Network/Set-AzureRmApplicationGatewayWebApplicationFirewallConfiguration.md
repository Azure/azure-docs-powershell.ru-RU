---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: fd925829248c7f11f047de90ddc2bc0b57f51b71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914018"
---
# <span data-ttu-id="93d9c-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="93d9c-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="93d9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="93d9c-103">Изменяет конфигурацию WAF для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="93d9c-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93d9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93d9c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93d9c-105">DESCRIPTION</span></span>
<span data-ttu-id="93d9c-106">Командлет **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="93d9c-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="93d9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93d9c-107">EXAMPLES</span></span>

### <span data-ttu-id="93d9c-108">Пример 1: Обновление конфигурации брандмауэра для веб-приложения "шлюз приложений"</span><span class="sxs-lookup"><span data-stu-id="93d9c-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="93d9c-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="93d9c-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="93d9c-110">Вторая команда включает конфигурацию брандмауэра для шлюза приложения, хранящуюся в $AppGw, и задает для режима брандмауэра значение "Обнаружение", RuleSetType на "OWASP", а RuleSetVersion — "3,0".</span><span class="sxs-lookup"><span data-stu-id="93d9c-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="93d9c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93d9c-111">PARAMETERS</span></span>

### <span data-ttu-id="93d9c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93d9c-112">-ApplicationGateway</span></span>
<span data-ttu-id="93d9c-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="93d9c-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="93d9c-114">Вы можете использовать командлет Get-AzureRmApplicationGateway, чтобы получить объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="93d9c-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93d9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d9c-115">-DefaultProfile</span></span>
<span data-ttu-id="93d9c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93d9c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93d9c-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="93d9c-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="93d9c-118">Группы отключенных правил.</span><span class="sxs-lookup"><span data-stu-id="93d9c-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="93d9c-119">-Включено</span><span class="sxs-lookup"><span data-stu-id="93d9c-119">-Enabled</span></span>
<span data-ttu-id="93d9c-120">Указывает, включен ли брандмауэр веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="93d9c-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="93d9c-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="93d9c-121">-FirewallMode</span></span>
<span data-ttu-id="93d9c-122">Задает режим брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="93d9c-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="93d9c-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="93d9c-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93d9c-124">Случай</span><span class="sxs-lookup"><span data-stu-id="93d9c-124">Detection</span></span>
- <span data-ttu-id="93d9c-125">Диагностик</span><span class="sxs-lookup"><span data-stu-id="93d9c-125">Prevention</span></span>

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

### <span data-ttu-id="93d9c-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="93d9c-126">-RuleSetType</span></span>
<span data-ttu-id="93d9c-127">Тип набора правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="93d9c-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="93d9c-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="93d9c-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="93d9c-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="93d9c-129">OWASP</span></span>

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

### <span data-ttu-id="93d9c-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="93d9c-130">-RuleSetVersion</span></span>
<span data-ttu-id="93d9c-131">Версия типа набора правил.</span><span class="sxs-lookup"><span data-stu-id="93d9c-131">The version of the rule set type.</span></span>
<span data-ttu-id="93d9c-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="93d9c-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="93d9c-133">3,0</span><span class="sxs-lookup"><span data-stu-id="93d9c-133">3.0</span></span>
- <span data-ttu-id="93d9c-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="93d9c-134">2.2.9</span></span>

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

### <span data-ttu-id="93d9c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93d9c-135">-Confirm</span></span>
<span data-ttu-id="93d9c-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93d9c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93d9c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d9c-137">-WhatIf</span></span>
<span data-ttu-id="93d9c-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93d9c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93d9c-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93d9c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93d9c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d9c-140">CommonParameters</span></span>
<span data-ttu-id="93d9c-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93d9c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d9c-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d9c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d9c-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93d9c-143">INPUTS</span></span>

### <span data-ttu-id="93d9c-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93d9c-144">PSApplicationGateway</span></span>
<span data-ttu-id="93d9c-145">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="93d9c-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="93d9c-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93d9c-146">OUTPUTS</span></span>

### <span data-ttu-id="93d9c-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93d9c-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93d9c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="93d9c-148">NOTES</span></span>

## <span data-ttu-id="93d9c-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93d9c-149">RELATED LINKS</span></span>

[<span data-ttu-id="93d9c-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93d9c-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="93d9c-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="93d9c-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="93d9c-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="93d9c-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


