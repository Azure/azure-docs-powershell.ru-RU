---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95f3e4b11d9253a232fc119faf39a4fa51fab60a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421852"
---
# <span data-ttu-id="957c7-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="957c7-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="957c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957c7-102">SYNOPSIS</span></span>
<span data-ttu-id="957c7-103">Создает правило маршрутки запросов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="957c7-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="957c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="957c7-104">SYNTAX</span></span>

### <span data-ttu-id="957c7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="957c7-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="957c7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="957c7-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-Priority <Int32>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="957c7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="957c7-107">DESCRIPTION</span></span>
<span data-ttu-id="957c7-108">**Cmdlet Add-AzApplicationGatewayRequestRoutingRule** создает правило маршрутизации запросов для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="957c7-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="957c7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="957c7-109">EXAMPLES</span></span>

### <span data-ttu-id="957c7-110">Пример 1. Создание правила маршрутки запроса для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="957c7-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="957c7-111">Эта команда создает базовое правило маршрутизов запросов с именем "Правило01" и сохраняет результат в переменной с $Rule.</span><span class="sxs-lookup"><span data-stu-id="957c7-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="957c7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="957c7-112">PARAMETERS</span></span>

### <span data-ttu-id="957c7-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="957c7-113">-BackendAddressPool</span></span>
<span data-ttu-id="957c7-114">Определяет пул конечных адресов в качестве объекта, который создает правило маршрутинга запросов.</span><span class="sxs-lookup"><span data-stu-id="957c7-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="957c7-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="957c7-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="957c7-116">Определяет конечный ИД пула адресов, который создается правило маршрутинга запросов.</span><span class="sxs-lookup"><span data-stu-id="957c7-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="957c7-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="957c7-117">-BackendHttpSettings</span></span>
<span data-ttu-id="957c7-118">Определяет конечные параметры HTTP в качестве объекта, которые создает правило маршрутинга запросов.</span><span class="sxs-lookup"><span data-stu-id="957c7-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="957c7-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="957c7-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="957c7-120">Определяет конечный http-параметры ИД правила маршрутки запросов, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="957c7-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="957c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957c7-121">-DefaultProfile</span></span>
<span data-ttu-id="957c7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="957c7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="957c7-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="957c7-123">-HttpListener</span></span>
<span data-ttu-id="957c7-124">Указывает прослушаку HTTP для правила маршрутки запросов, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="957c7-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="957c7-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="957c7-125">-HttpListenerId</span></span>
<span data-ttu-id="957c7-126">Определяет дополнительный ИД HTTP-прослушки для правила маршрутки запросов, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="957c7-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="957c7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="957c7-127">-Name</span></span>
<span data-ttu-id="957c7-128">Указывает имя правила маршрутки запроса, которое создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="957c7-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="957c7-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="957c7-129">-Priority</span></span>
<span data-ttu-id="957c7-130">Приоритет правила</span><span class="sxs-lookup"><span data-stu-id="957c7-130">The priority of the rule</span></span>

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

### <span data-ttu-id="957c7-131">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="957c7-131">-RedirectConfiguration</span></span>
<span data-ttu-id="957c7-132">RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="957c7-132">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="957c7-133">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="957c7-133">-RedirectConfigurationId</span></span>
<span data-ttu-id="957c7-134">ID of the application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="957c7-134">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="957c7-135">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="957c7-135">-RewriteRuleSet</span></span>
<span data-ttu-id="957c7-136">RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="957c7-136">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="957c7-137">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="957c7-137">-RewriteRuleSetId</span></span>
<span data-ttu-id="957c7-138">ИД шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="957c7-138">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="957c7-139">-RuleType</span><span class="sxs-lookup"><span data-stu-id="957c7-139">-RuleType</span></span>
<span data-ttu-id="957c7-140">Определяет тип правила маршрутки запроса.</span><span class="sxs-lookup"><span data-stu-id="957c7-140">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="957c7-141">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="957c7-141">-UrlPathMap</span></span>
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

### <span data-ttu-id="957c7-142">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="957c7-142">-UrlPathMapId</span></span>
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

### <span data-ttu-id="957c7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957c7-143">CommonParameters</span></span>
<span data-ttu-id="957c7-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="957c7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957c7-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="957c7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957c7-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="957c7-146">INPUTS</span></span>

### <span data-ttu-id="957c7-147">Нет</span><span class="sxs-lookup"><span data-stu-id="957c7-147">None</span></span>

## <span data-ttu-id="957c7-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="957c7-148">OUTPUTS</span></span>

### <span data-ttu-id="957c7-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="957c7-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="957c7-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="957c7-150">NOTES</span></span>

## <span data-ttu-id="957c7-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="957c7-151">RELATED LINKS</span></span>

[<span data-ttu-id="957c7-152">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="957c7-152">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="957c7-153">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="957c7-153">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="957c7-154">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="957c7-154">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="957c7-155">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="957c7-155">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


