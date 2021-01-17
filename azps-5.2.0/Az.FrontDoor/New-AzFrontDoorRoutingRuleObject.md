---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405756"
---
# <span data-ttu-id="4c064-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="4c064-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="4c064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c064-102">SYNOPSIS</span></span>
<span data-ttu-id="4c064-103">Создание psRoutingRuleObject для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="4c064-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="4c064-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c064-104">SYNTAX</span></span>

### <span data-ttu-id="4c064-105">ByFieldsWithForwardingParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c064-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c064-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c064-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c064-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c064-107">DESCRIPTION</span></span>
<span data-ttu-id="4c064-108">Создание psRoutingRuleObject для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="4c064-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="4c064-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c064-109">EXAMPLES</span></span>

### <span data-ttu-id="4c064-110">Пример 1. Создание psRoutingRuleObject для создания передней двери с помощью правила переадружения</span><span class="sxs-lookup"><span data-stu-id="4c064-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="4c064-111">Пример 2. Создание psRoutingRuleObject для создания передней двери с помощью правила перенаправления</span><span class="sxs-lookup"><span data-stu-id="4c064-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="4c064-112">Создание psRoutingRuleObject для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="4c064-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="4c064-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c064-113">PARAMETERS</span></span>

### <span data-ttu-id="4c064-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="4c064-114">-AcceptedProtocol</span></span>
<span data-ttu-id="4c064-115">Схемы протокола, которые соответствуют этому правилу.</span><span class="sxs-lookup"><span data-stu-id="4c064-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="4c064-116">Значение по умолчанию: {Https, Http}</span><span class="sxs-lookup"><span data-stu-id="4c064-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="4c064-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="4c064-117">-BackendPoolName</span></span>
<span data-ttu-id="4c064-118">ИД ресурса backendPool, на который это правило перенаправить</span><span class="sxs-lookup"><span data-stu-id="4c064-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="4c064-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="4c064-119">-CustomForwardingPath</span></span>
<span data-ttu-id="4c064-120">Настраиваемый путь, используемый для переописи путей ресурсов, которые соответствуют этому правилу.</span><span class="sxs-lookup"><span data-stu-id="4c064-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="4c064-121">Оставьте пустым, чтобы использовать входящие пути.</span><span class="sxs-lookup"><span data-stu-id="4c064-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="4c064-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="4c064-122">-CustomFragment</span></span>
<span data-ttu-id="4c064-123">Фрагмент для добавления в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4c064-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="4c064-124">Фрагмент — это часть URL-адреса, которая появляется после #.</span><span class="sxs-lookup"><span data-stu-id="4c064-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="4c064-125">Не включаем</span><span class="sxs-lookup"><span data-stu-id="4c064-125">Do not include the #.</span></span>

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

### <span data-ttu-id="4c064-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="4c064-126">-CustomHost</span></span>
<span data-ttu-id="4c064-127">Host to redirect (Перенаправление) host (Перена</span><span class="sxs-lookup"><span data-stu-id="4c064-127">Host to redirect.</span></span> <span data-ttu-id="4c064-128">Оставьте пустым, чтобы использовать входящие хост в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="4c064-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="4c064-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="4c064-129">-CustomPath</span></span>
<span data-ttu-id="4c064-130">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4c064-130">The full path to redirect.</span></span> <span data-ttu-id="4c064-131">Путь не может быть пустым и должен начинаться с /.</span><span class="sxs-lookup"><span data-stu-id="4c064-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="4c064-132">Оставьте пустым, чтобы использовать входящий путь в качестве пути назначения.</span><span class="sxs-lookup"><span data-stu-id="4c064-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="4c064-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="4c064-133">-CustomQueryString</span></span>
<span data-ttu-id="4c064-134">Набор строк запроса, которые нужно поместить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="4c064-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="4c064-135">Если это значение заместит любую существующую строку запроса; оставьте пустым, чтобы сохранить строку входящих запросов.</span><span class="sxs-lookup"><span data-stu-id="4c064-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="4c064-136">Строка запроса должна быть в <key>=</span><span class="sxs-lookup"><span data-stu-id="4c064-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="4c064-137">формат.</span><span class="sxs-lookup"><span data-stu-id="4c064-137">format.</span></span> <span data-ttu-id="4c064-138">Первый ?</span><span class="sxs-lookup"><span data-stu-id="4c064-138">The first ?</span></span> <span data-ttu-id="4c064-139">и & будут добавлены автоматически, поэтому не включайте их в запрос, но разделяйте несколько строк запроса &.</span><span class="sxs-lookup"><span data-stu-id="4c064-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="4c064-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c064-140">-DefaultProfile</span></span>
<span data-ttu-id="4c064-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c064-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c064-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="4c064-142">-DynamicCompression</span></span>
<span data-ttu-id="4c064-143">Включить ли динамическое сжатие для кэшного содержимого при включенной кэшации.</span><span class="sxs-lookup"><span data-stu-id="4c064-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="4c064-144">Значение по умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="4c064-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="4c064-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="4c064-145">-EnableCaching</span></span>
<span data-ttu-id="4c064-146">Следует ли включить кэшинг для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="4c064-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="4c064-147">Значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="4c064-147">Default value is false</span></span>

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

### <span data-ttu-id="4c064-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="4c064-148">-EnabledState</span></span>
<span data-ttu-id="4c064-149">Следует ли включить это правило.</span><span class="sxs-lookup"><span data-stu-id="4c064-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="4c064-150">Значение по умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="4c064-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="4c064-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="4c064-151">-ForwardingProtocol</span></span>
<span data-ttu-id="4c064-152">Протокол, который будет применяться этим правилом при перенаправить трафик на backends Default ( значение По умолчанию — MatchRequest).</span><span class="sxs-lookup"><span data-stu-id="4c064-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="4c064-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4c064-153">-FrontDoorName</span></span>
<span data-ttu-id="4c064-154">Название переднего входа, к которому относится это правило маршрутинга.</span><span class="sxs-lookup"><span data-stu-id="4c064-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="4c064-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="4c064-155">-FrontendEndpointName</span></span>
<span data-ttu-id="4c064-156">Имена конечных точек frontend, связанных с этим правилом</span><span class="sxs-lookup"><span data-stu-id="4c064-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="4c064-157">-Name</span><span class="sxs-lookup"><span data-stu-id="4c064-157">-Name</span></span>
<span data-ttu-id="4c064-158">RoutingRule name.</span><span class="sxs-lookup"><span data-stu-id="4c064-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="4c064-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="4c064-159">-PatternToMatch</span></span>
<span data-ttu-id="4c064-160">Шаблоны маршрутов правила не должны иметь \*, кроме, возможно, после последнего /в конце пути.</span><span class="sxs-lookup"><span data-stu-id="4c064-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="4c064-161">Значение по умолчанию: /\*</span><span class="sxs-lookup"><span data-stu-id="4c064-161">Default value is /\*</span></span>

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

### <span data-ttu-id="4c064-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="4c064-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="4c064-163">Обработка условий URL-запроса при формировании ключа кэша.</span><span class="sxs-lookup"><span data-stu-id="4c064-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="4c064-164">Значение по умолчанию — StripAll</span><span class="sxs-lookup"><span data-stu-id="4c064-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="4c064-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="4c064-165">-RedirectProtocol</span></span>
<span data-ttu-id="4c064-166">Протокол назначения, в который перенаправляется трафик.</span><span class="sxs-lookup"><span data-stu-id="4c064-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="4c064-167">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="4c064-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="4c064-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="4c064-168">-RedirectType</span></span>
<span data-ttu-id="4c064-169">Тип перенаправления, который будет применяться правилом при перенаправлении трафика.</span><span class="sxs-lookup"><span data-stu-id="4c064-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="4c064-170">Значение по умолчанию перемещено</span><span class="sxs-lookup"><span data-stu-id="4c064-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="4c064-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c064-171">-ResourceGroupName</span></span>
<span data-ttu-id="4c064-172">Имя группы ресурсов, в которую будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="4c064-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="4c064-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="4c064-173">-RulesEngineName</span></span>
<span data-ttu-id="4c064-174">Ссылка на конкретную конфигурацию обулка правил, применяемую к этому маршруту.</span><span class="sxs-lookup"><span data-stu-id="4c064-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="4c064-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c064-175">CommonParameters</span></span>
<span data-ttu-id="4c064-176">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c064-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c064-177">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c064-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c064-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c064-178">INPUTS</span></span>

### <span data-ttu-id="4c064-179">Нет</span><span class="sxs-lookup"><span data-stu-id="4c064-179">None</span></span>

## <span data-ttu-id="4c064-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c064-180">OUTPUTS</span></span>

### <span data-ttu-id="4c064-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4c064-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="4c064-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c064-182">NOTES</span></span>

## <span data-ttu-id="4c064-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c064-183">RELATED LINKS</span></span>

<span data-ttu-id="4c064-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="4c064-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
