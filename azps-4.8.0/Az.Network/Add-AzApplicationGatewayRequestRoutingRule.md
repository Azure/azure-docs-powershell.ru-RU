---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: b0335fd0700b256650809c4548efe4d1e620442b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078956"
---
# <span data-ttu-id="160d8-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="160d8-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="160d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="160d8-102">SYNOPSIS</span></span>
<span data-ttu-id="160d8-103">Добавляет правило маршрутизации запросов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="160d8-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="160d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="160d8-104">SYNTAX</span></span>

### <span data-ttu-id="160d8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="160d8-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="160d8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="160d8-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="160d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="160d8-107">DESCRIPTION</span></span>
<span data-ttu-id="160d8-108">Командлет **Add-AzApplicationGatewayRequestRoutingRule** добавляет правило маршрутизации запросов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="160d8-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="160d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="160d8-109">EXAMPLES</span></span>

### <span data-ttu-id="160d8-110">Пример 1: Добавление правила маршрутизации запросов к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="160d8-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="160d8-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="160d8-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="160d8-112">Вторая команда добавляет правило маршрутизации запросов к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="160d8-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="160d8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="160d8-113">PARAMETERS</span></span>

### <span data-ttu-id="160d8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="160d8-114">-ApplicationGateway</span></span>
<span data-ttu-id="160d8-115">Указывает шлюз приложений, к которому этот командлет добавляет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="160d8-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="160d8-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="160d8-116">-BackendAddressPool</span></span>
<span data-ttu-id="160d8-117">Указывает объект пула для серверного конечного адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="160d8-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="160d8-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="160d8-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="160d8-119">Задает серверный идентификатор пула конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="160d8-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="160d8-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="160d8-120">-BackendHttpSettings</span></span>
<span data-ttu-id="160d8-121">Указывает объект параметров HTTP для веб-части для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="160d8-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="160d8-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="160d8-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="160d8-123">Указывает идентификатор HTTP-параметров для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="160d8-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="160d8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160d8-124">-DefaultProfile</span></span>
<span data-ttu-id="160d8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="160d8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="160d8-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="160d8-126">-HttpListener</span></span>
<span data-ttu-id="160d8-127">Указывает объект прослушивателя HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="160d8-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="160d8-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="160d8-128">-HttpListenerId</span></span>
<span data-ttu-id="160d8-129">Указывает идентификатор прослушивателя HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="160d8-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="160d8-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="160d8-130">-Name</span></span>
<span data-ttu-id="160d8-131">Указывает имя правила маршрутизации запросов, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="160d8-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="160d8-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="160d8-132">-RedirectConfiguration</span></span>
<span data-ttu-id="160d8-133">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="160d8-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="160d8-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="160d8-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="160d8-135">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="160d8-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="160d8-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="160d8-136">-RewriteRuleSet</span></span>
<span data-ttu-id="160d8-137">RewriteRuleSet шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="160d8-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="160d8-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="160d8-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="160d8-139">Идентификатор RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="160d8-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="160d8-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="160d8-140">-RuleType</span></span>
<span data-ttu-id="160d8-141">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="160d8-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="160d8-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="160d8-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="160d8-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="160d8-143">-UrlPathMapId</span></span>
<span data-ttu-id="160d8-144">Указывает идентификатор URL-пути для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="160d8-144">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="160d8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160d8-145">CommonParameters</span></span>
<span data-ttu-id="160d8-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="160d8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160d8-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="160d8-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160d8-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="160d8-148">INPUTS</span></span>

### <span data-ttu-id="160d8-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="160d8-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="160d8-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="160d8-150">OUTPUTS</span></span>

### <span data-ttu-id="160d8-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="160d8-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="160d8-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="160d8-152">NOTES</span></span>

## <span data-ttu-id="160d8-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="160d8-153">RELATED LINKS</span></span>

[<span data-ttu-id="160d8-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="160d8-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="160d8-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="160d8-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="160d8-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="160d8-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="160d8-157">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="160d8-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

