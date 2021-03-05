---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 832fd96f34e18413bfd72e1a05826954f3ae58e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005891"
---
# <span data-ttu-id="f128e-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f128e-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f128e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f128e-102">SYNOPSIS</span></span>
<span data-ttu-id="f128e-103">Изменяет правило маршрутики запроса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f128e-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f128e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f128e-104">SYNTAX</span></span>

### <span data-ttu-id="f128e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f128e-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f128e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f128e-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f128e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f128e-107">DESCRIPTION</span></span>
<span data-ttu-id="f128e-108">**Cmdlet Set-AzApplicationGatewayRequestRoutingRule** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="f128e-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f128e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f128e-109">EXAMPLES</span></span>

### <span data-ttu-id="f128e-110">Пример 1. Обновление правила маршрутки запросов</span><span class="sxs-lookup"><span data-stu-id="f128e-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="f128e-111">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f128e-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f128e-112">Вторая команда изменяет правило маршрутики запроса шлюза приложения на использование back-end HTTP-параметров, задающихся в переменной $Setting, http-прослушивания, указанного в переменной $Listener, и пула адресов с конечными адресами, заданными в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="f128e-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="f128e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f128e-113">PARAMETERS</span></span>

### <span data-ttu-id="f128e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f128e-114">-ApplicationGateway</span></span>
<span data-ttu-id="f128e-115">Определяет объект шлюза приложения, с которым этот cmdlet связывает правило маршрутки запросов.</span><span class="sxs-lookup"><span data-stu-id="f128e-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="f128e-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f128e-116">-BackendAddressPool</span></span>
<span data-ttu-id="f128e-117">Определяет пул адресов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f128e-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="f128e-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f128e-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f128e-119">Определяет ИД пула адресов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f128e-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="f128e-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f128e-120">-BackendHttpSettings</span></span>
<span data-ttu-id="f128e-121">Определяет параметры HTTP шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f128e-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="f128e-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f128e-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f128e-123">Определяет back-end HTTP-параметры шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f128e-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="f128e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f128e-124">-DefaultProfile</span></span>
<span data-ttu-id="f128e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f128e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f128e-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f128e-126">-HttpListener</span></span>
<span data-ttu-id="f128e-127">Указывает шлюз приложения HTTP-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="f128e-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f128e-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="f128e-128">-HttpListenerId</span></span>
<span data-ttu-id="f128e-129">Указывает ИД HTTP-приложения шлюза HTTP.</span><span class="sxs-lookup"><span data-stu-id="f128e-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="f128e-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f128e-130">-Name</span></span>
<span data-ttu-id="f128e-131">Указывает имя правила маршрутики запроса, которое изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f128e-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f128e-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="f128e-132">-Priority</span></span>
<span data-ttu-id="f128e-133">Приоритет правила</span><span class="sxs-lookup"><span data-stu-id="f128e-133">The priority of the rule</span></span>

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

### <span data-ttu-id="f128e-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f128e-134">-RedirectConfiguration</span></span>
<span data-ttu-id="f128e-135">RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="f128e-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f128e-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f128e-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="f128e-137">ID of the application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f128e-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f128e-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f128e-138">-RewriteRuleSet</span></span>
<span data-ttu-id="f128e-139">RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="f128e-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f128e-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="f128e-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="f128e-141">ИД шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f128e-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="f128e-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="f128e-142">-RuleType</span></span>
<span data-ttu-id="f128e-143">Определяет тип правила маршрутинга запросов.</span><span class="sxs-lookup"><span data-stu-id="f128e-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="f128e-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f128e-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="f128e-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="f128e-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="f128e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f128e-146">CommonParameters</span></span>
<span data-ttu-id="f128e-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f128e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f128e-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f128e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f128e-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f128e-149">INPUTS</span></span>

### <span data-ttu-id="f128e-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f128e-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f128e-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f128e-151">OUTPUTS</span></span>

### <span data-ttu-id="f128e-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f128e-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f128e-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f128e-153">NOTES</span></span>

## <span data-ttu-id="f128e-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f128e-154">RELATED LINKS</span></span>

[<span data-ttu-id="f128e-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f128e-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f128e-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f128e-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f128e-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f128e-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f128e-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f128e-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


