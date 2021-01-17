---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f815994a6f60490bd930a17748cd00167c2b52ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421423"
---
# <span data-ttu-id="4e268-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4e268-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4e268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e268-102">SYNOPSIS</span></span>
<span data-ttu-id="4e268-103">Изменяет правило маршрутики запроса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4e268-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="4e268-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e268-104">SYNTAX</span></span>

### <span data-ttu-id="4e268-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e268-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e268-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4e268-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e268-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e268-107">DESCRIPTION</span></span>
<span data-ttu-id="4e268-108">**Cmdlet Set-AzApplicationGatewayRequestRoutingRule** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="4e268-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="4e268-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e268-109">EXAMPLES</span></span>

### <span data-ttu-id="4e268-110">Пример 1. Обновление правила маршрутки запросов</span><span class="sxs-lookup"><span data-stu-id="4e268-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="4e268-111">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4e268-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4e268-112">Вторая команда изменяет правило маршрутики запроса шлюза приложения, чтобы использовать back-end HTTP-параметры, указанные в переменной $Setting, http-прослушивание, указанное в переменной $Listener, и пул конечных адресов, заданный в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="4e268-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="4e268-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e268-113">PARAMETERS</span></span>

### <span data-ttu-id="4e268-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e268-114">-ApplicationGateway</span></span>
<span data-ttu-id="4e268-115">Определяет объект шлюза приложения, с которым этот cmdlet связывает правило маршрутки запросов.</span><span class="sxs-lookup"><span data-stu-id="4e268-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="4e268-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e268-116">-BackendAddressPool</span></span>
<span data-ttu-id="4e268-117">Определяет пул адресов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4e268-117">Specifies the application gateway back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4e268-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="4e268-119">Определяет ИД пула адресов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4e268-119">Specifies the application gateway back-end address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4e268-120">-BackendHttpSettings</span></span>
<span data-ttu-id="4e268-121">Определяет параметры HTTP шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4e268-121">Specifies the application gateway backend HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4e268-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="4e268-123">Определяет back-end HTTP-параметры шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4e268-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e268-124">-DefaultProfile</span></span>
<span data-ttu-id="4e268-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e268-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e268-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="4e268-126">-HttpListener</span></span>
<span data-ttu-id="4e268-127">Указывает шлюз приложения HTTP-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="4e268-127">Specifies the application gateway HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="4e268-128">-HttpListenerId</span></span>
<span data-ttu-id="4e268-129">Определяет ИД HTTP-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4e268-129">Specifies the application gateway HTTP listener ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-130">-Name</span><span class="sxs-lookup"><span data-stu-id="4e268-130">-Name</span></span>
<span data-ttu-id="4e268-131">Указывает имя правила маршрутики запроса, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e268-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4e268-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="4e268-132">-Priority</span></span>
<span data-ttu-id="4e268-133">Приоритет правила</span><span class="sxs-lookup"><span data-stu-id="4e268-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e268-134">-RedirectConfiguration</span></span>
<span data-ttu-id="4e268-135">RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="4e268-135">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4e268-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="4e268-137">ID of the application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e268-137">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e268-138">-RewriteRuleSet</span></span>
<span data-ttu-id="4e268-139">RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="4e268-139">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="4e268-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="4e268-141">ИД шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e268-141">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="4e268-142">-RuleType</span></span>
<span data-ttu-id="4e268-143">Определяет тип правила маршрутки запросов.</span><span class="sxs-lookup"><span data-stu-id="4e268-143">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="4e268-144">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="4e268-145">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e268-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e268-146">CommonParameters</span></span>
<span data-ttu-id="4e268-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e268-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e268-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e268-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e268-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e268-149">INPUTS</span></span>

### <span data-ttu-id="4e268-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e268-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e268-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e268-151">OUTPUTS</span></span>

### <span data-ttu-id="4e268-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e268-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4e268-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e268-153">NOTES</span></span>

## <span data-ttu-id="4e268-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e268-154">RELATED LINKS</span></span>

[<span data-ttu-id="4e268-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4e268-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4e268-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4e268-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4e268-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4e268-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4e268-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4e268-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


