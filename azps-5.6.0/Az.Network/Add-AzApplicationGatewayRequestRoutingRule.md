---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d86810ec15d38ecbe57a7471297b4ac167a2e526
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982504"
---
# <span data-ttu-id="b4067-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4067-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b4067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4067-102">SYNOPSIS</span></span>
<span data-ttu-id="b4067-103">Добавляет правило маршрутки запросов к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="b4067-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4067-104">SYNTAX</span></span>

### <span data-ttu-id="b4067-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4067-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4067-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4067-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4067-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4067-107">DESCRIPTION</span></span>
<span data-ttu-id="b4067-108">Cmdlet **Add-AzApplicationGatewayRequestRoutingRule** добавляет правило маршрутизации запросов к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="b4067-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4067-109">EXAMPLES</span></span>

### <span data-ttu-id="b4067-110">Пример 1. Добавление правила маршрутки запроса к шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="b4067-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="b4067-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b4067-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b4067-112">Вторая команда добавляет правило маршрутки запроса к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="b4067-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4067-113">PARAMETERS</span></span>

### <span data-ttu-id="b4067-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4067-114">-ApplicationGateway</span></span>
<span data-ttu-id="b4067-115">Указывает шлюз приложения, к которому этот cmdlet добавляет правило маршрутки запросов.</span><span class="sxs-lookup"><span data-stu-id="b4067-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="b4067-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4067-116">-BackendAddressPool</span></span>
<span data-ttu-id="b4067-117">Определяет объект пула адресов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="b4067-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b4067-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="b4067-119">Определяет ИД пула адресов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="b4067-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b4067-120">-BackendHttpSettings</span></span>
<span data-ttu-id="b4067-121">Определяет объект параметров HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="b4067-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b4067-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="b4067-123">Определяет дополнительный http-параметры ИД шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="b4067-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4067-124">-DefaultProfile</span></span>
<span data-ttu-id="b4067-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4067-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4067-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b4067-126">-HttpListener</span></span>
<span data-ttu-id="b4067-127">Определяет объект HTTP-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="b4067-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="b4067-128">-HttpListenerId</span></span>
<span data-ttu-id="b4067-129">Определяет ИД HTTP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4067-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="b4067-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b4067-130">-Name</span></span>
<span data-ttu-id="b4067-131">Указывает имя правила маршрутинга запросов, которое добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4067-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="b4067-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="b4067-132">-Priority</span></span>
<span data-ttu-id="b4067-133">Приоритет правила</span><span class="sxs-lookup"><span data-stu-id="b4067-133">The priority of the rule</span></span>

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

### <span data-ttu-id="b4067-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4067-134">-RedirectConfiguration</span></span>
<span data-ttu-id="b4067-135">RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b4067-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b4067-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4067-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="b4067-137">ID of the application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4067-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b4067-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4067-138">-RewriteRuleSet</span></span>
<span data-ttu-id="b4067-139">RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b4067-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b4067-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="b4067-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="b4067-141">ИД шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b4067-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b4067-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b4067-142">-RuleType</span></span>
<span data-ttu-id="b4067-143">Определяет тип правила маршрутинга запросов.</span><span class="sxs-lookup"><span data-stu-id="b4067-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="b4067-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="b4067-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="b4067-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="b4067-145">-UrlPathMapId</span></span>
<span data-ttu-id="b4067-146">Определяет url-адрес карты пути для правила маршрутки.</span><span class="sxs-lookup"><span data-stu-id="b4067-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="b4067-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4067-147">CommonParameters</span></span>
<span data-ttu-id="b4067-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4067-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4067-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4067-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4067-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4067-150">INPUTS</span></span>

### <span data-ttu-id="b4067-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4067-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4067-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4067-152">OUTPUTS</span></span>

### <span data-ttu-id="b4067-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4067-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4067-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4067-154">NOTES</span></span>

## <span data-ttu-id="b4067-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4067-155">RELATED LINKS</span></span>

[<span data-ttu-id="b4067-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4067-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b4067-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4067-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b4067-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4067-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b4067-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b4067-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


