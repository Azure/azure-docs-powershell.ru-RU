---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243570"
---
# <span data-ttu-id="ed46c-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="ed46c-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="ed46c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed46c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed46c-103">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ed46c-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="ed46c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed46c-104">SYNTAX</span></span>

### <span data-ttu-id="ed46c-105">ByFieldsWithForwardingParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed46c-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed46c-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed46c-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed46c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed46c-107">DESCRIPTION</span></span>
<span data-ttu-id="ed46c-108">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ed46c-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="ed46c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed46c-109">EXAMPLES</span></span>

### <span data-ttu-id="ed46c-110">Пример 1: создание PSRoutingRuleObject для создания передней дверцы с помощью правила переадресации</span><span class="sxs-lookup"><span data-stu-id="ed46c-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="ed46c-111">Пример 2: создание PSRoutingRuleObject для создания передней дверцы с помощью правила перенаправления</span><span class="sxs-lookup"><span data-stu-id="ed46c-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="ed46c-112">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="ed46c-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="ed46c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed46c-113">PARAMETERS</span></span>

### <span data-ttu-id="ed46c-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="ed46c-114">-AcceptedProtocol</span></span>
<span data-ttu-id="ed46c-115">Схемы протоколов для сопоставления с этим правилом.</span><span class="sxs-lookup"><span data-stu-id="ed46c-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="ed46c-116">Значение по умолчанию: {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="ed46c-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="ed46c-117">-BackendPoolName</span></span>
<span data-ttu-id="ed46c-118">Идентификатор ресурса для BackendPool, к которому это правило адресуется</span><span class="sxs-lookup"><span data-stu-id="ed46c-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="ed46c-119">-CustomForwardingPath</span></span>
<span data-ttu-id="ed46c-120">Настраиваемый путь, используемый для перезаписи путей к ресурсам, подходящих для этого правила.</span><span class="sxs-lookup"><span data-stu-id="ed46c-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="ed46c-121">Оставьте поле пустым, чтобы использовать входящий путь.</span><span class="sxs-lookup"><span data-stu-id="ed46c-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="ed46c-122">-CustomFragment</span></span>
<span data-ttu-id="ed46c-123">Фрагмент, который нужно добавить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="ed46c-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="ed46c-124">Фрагмент — это часть URL-адреса, который приходится на следующий адрес:</span><span class="sxs-lookup"><span data-stu-id="ed46c-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="ed46c-125">Не включайте номер #.</span><span class="sxs-lookup"><span data-stu-id="ed46c-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="ed46c-126">-CustomHost</span></span>
<span data-ttu-id="ed46c-127">Hosting (перенаправление).</span><span class="sxs-lookup"><span data-stu-id="ed46c-127">Host to redirect.</span></span> <span data-ttu-id="ed46c-128">Оставьте пустым, чтобы использовать узел входящей почты в качестве узла назначения.</span><span class="sxs-lookup"><span data-stu-id="ed46c-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="ed46c-129">-CustomPath</span></span>
<span data-ttu-id="ed46c-130">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="ed46c-130">The full path to redirect.</span></span> <span data-ttu-id="ed46c-131">Путь не может быть пустым и должен начинаться с/.</span><span class="sxs-lookup"><span data-stu-id="ed46c-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="ed46c-132">Оставьте пустым, чтобы использовать входящий путь в качестве конечного пути.</span><span class="sxs-lookup"><span data-stu-id="ed46c-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="ed46c-133">-CustomQueryString</span></span>
<span data-ttu-id="ed46c-134">Набор строк запроса, которые должны быть помещены в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="ed46c-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="ed46c-135">При задании этого значения все имеющиеся строки запроса будут заменены. Оставьте пустым для сохранения строки входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="ed46c-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="ed46c-136">Строка запроса должна находиться в <key>=</span><span class="sxs-lookup"><span data-stu-id="ed46c-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="ed46c-137">формате.</span><span class="sxs-lookup"><span data-stu-id="ed46c-137">format.</span></span> <span data-ttu-id="ed46c-138">Первый?</span><span class="sxs-lookup"><span data-stu-id="ed46c-138">The first ?</span></span> <span data-ttu-id="ed46c-139">и & будут автоматически добавляться, поэтому не включайте их на передний план, но разделите строки запросов с помощью &.</span><span class="sxs-lookup"><span data-stu-id="ed46c-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed46c-140">-DefaultProfile</span></span>
<span data-ttu-id="ed46c-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed46c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed46c-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="ed46c-142">-DynamicCompression</span></span>
<span data-ttu-id="ed46c-143">Следует ли включить динамическое сжатие для кэшированного содержимого, если включено кэширование.</span><span class="sxs-lookup"><span data-stu-id="ed46c-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="ed46c-144">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="ed46c-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="ed46c-145">-EnableCaching</span></span>
<span data-ttu-id="ed46c-146">Следует ли включить кэширование для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="ed46c-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="ed46c-147">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="ed46c-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ed46c-148">-EnabledState</span></span>
<span data-ttu-id="ed46c-149">Следует ли включить использование этого правила.</span><span class="sxs-lookup"><span data-stu-id="ed46c-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="ed46c-150">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="ed46c-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="ed46c-151">-ForwardingProtocol</span></span>
<span data-ttu-id="ed46c-152">Протокол, который будет использоваться этим правилом при пересылке трафика по умолчанию, имеет значение MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="ed46c-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ed46c-153">-FrontDoorName</span></span>
<span data-ttu-id="ed46c-154">Имя передней дверцы, к которой относится данное правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ed46c-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="ed46c-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="ed46c-155">-FrontendEndpointName</span></span>
<span data-ttu-id="ed46c-156">Имена конечных точек с интерфейсом, связанных с этим правилом</span><span class="sxs-lookup"><span data-stu-id="ed46c-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-157">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed46c-157">-Name</span></span>
<span data-ttu-id="ed46c-158">RoutingRule имя.</span><span class="sxs-lookup"><span data-stu-id="ed46c-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="ed46c-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="ed46c-159">-PatternToMatch</span></span>
<span data-ttu-id="ed46c-160">В шаблонах маршрутов правила не должно быть каких-либо знаков \* за исключением случаев, когда это возможно после конечной точки или в конце пути.</span><span class="sxs-lookup"><span data-stu-id="ed46c-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="ed46c-161">Значение по умолчанию —/\*</span><span class="sxs-lookup"><span data-stu-id="ed46c-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="ed46c-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="ed46c-163">Обработка терминов запроса URL-адреса при создании ключа кэша.</span><span class="sxs-lookup"><span data-stu-id="ed46c-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="ed46c-164">Значение по умолчанию — StripAll</span><span class="sxs-lookup"><span data-stu-id="ed46c-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="ed46c-165">-RedirectProtocol</span></span>
<span data-ttu-id="ed46c-166">Протокол назначения, на который перенаправляется трафик.</span><span class="sxs-lookup"><span data-stu-id="ed46c-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="ed46c-167">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="ed46c-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="ed46c-168">-RedirectType</span></span>
<span data-ttu-id="ed46c-169">Тип перенаправления, который будет использоваться правилом для перенаправления трафика.</span><span class="sxs-lookup"><span data-stu-id="ed46c-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="ed46c-170">Значение по умолчанию перемещается</span><span class="sxs-lookup"><span data-stu-id="ed46c-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed46c-171">-ResourceGroupName</span></span>
<span data-ttu-id="ed46c-172">Имя группы ресурсов, в которой будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="ed46c-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="ed46c-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="ed46c-173">-RulesEngineName</span></span>
<span data-ttu-id="ed46c-174">Ссылка на определенную конфигурацию обработчика правил, которую нужно применить к этому маршруту.</span><span class="sxs-lookup"><span data-stu-id="ed46c-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed46c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed46c-175">CommonParameters</span></span>
<span data-ttu-id="ed46c-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed46c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed46c-177">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed46c-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed46c-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed46c-178">INPUTS</span></span>

### <span data-ttu-id="ed46c-179">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed46c-179">None</span></span>

## <span data-ttu-id="ed46c-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed46c-180">OUTPUTS</span></span>

### <span data-ttu-id="ed46c-181">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ed46c-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="ed46c-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed46c-182">NOTES</span></span>

## <span data-ttu-id="ed46c-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed46c-183">RELATED LINKS</span></span>

<span data-ttu-id="ed46c-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ed46c-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
