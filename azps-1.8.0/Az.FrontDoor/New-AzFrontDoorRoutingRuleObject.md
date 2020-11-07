---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900598"
---
# <span data-ttu-id="cba93-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="cba93-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="cba93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cba93-102">SYNOPSIS</span></span>
<span data-ttu-id="cba93-103">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="cba93-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="cba93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cba93-104">SYNTAX</span></span>

### <span data-ttu-id="cba93-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="cba93-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cba93-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cba93-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba93-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba93-107">DESCRIPTION</span></span>
<span data-ttu-id="cba93-108">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="cba93-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="cba93-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cba93-109">EXAMPLES</span></span>

### <span data-ttu-id="cba93-110">Пример 1: создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="cba93-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="cba93-111">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="cba93-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="cba93-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cba93-112">PARAMETERS</span></span>

### <span data-ttu-id="cba93-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="cba93-113">-AcceptedProtocol</span></span>
<span data-ttu-id="cba93-114">Схемы протоколов для сопоставления с этим правилом.</span><span class="sxs-lookup"><span data-stu-id="cba93-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="cba93-115">Значение по умолчанию: {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="cba93-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="cba93-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="cba93-116">-BackendPoolName</span></span>
<span data-ttu-id="cba93-117">Идентификатор ресурса для BackendPool, к которому это правило адресуется</span><span class="sxs-lookup"><span data-stu-id="cba93-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="cba93-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="cba93-118">-CustomForwardingPath</span></span>
<span data-ttu-id="cba93-119">Настраиваемый путь, используемый для перезаписи путей к ресурсам, подходящих для этого правила.</span><span class="sxs-lookup"><span data-stu-id="cba93-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="cba93-120">Оставьте поле пустым, чтобы использовать входящий путь.</span><span class="sxs-lookup"><span data-stu-id="cba93-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="cba93-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="cba93-121">-CustomFragment</span></span>
<span data-ttu-id="cba93-122">Фрагмент, который нужно добавить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="cba93-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="cba93-123">Фрагмент — это часть URL-адреса, который приходится на следующий адрес:</span><span class="sxs-lookup"><span data-stu-id="cba93-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="cba93-124">Не включайте номер #.</span><span class="sxs-lookup"><span data-stu-id="cba93-124">Do not include the #.</span></span>

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

### <span data-ttu-id="cba93-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="cba93-125">-CustomHost</span></span>
<span data-ttu-id="cba93-126">Hosting (перенаправление).</span><span class="sxs-lookup"><span data-stu-id="cba93-126">Host to redirect.</span></span> <span data-ttu-id="cba93-127">Оставьте пустым, чтобы использовать узел входящей почты в качестве узла назначения.</span><span class="sxs-lookup"><span data-stu-id="cba93-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="cba93-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="cba93-128">-CustomPath</span></span>
<span data-ttu-id="cba93-129">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="cba93-129">The full path to redirect.</span></span> <span data-ttu-id="cba93-130">Путь не может быть пустым и должен начинаться с/.</span><span class="sxs-lookup"><span data-stu-id="cba93-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="cba93-131">Оставьте пустым, чтобы использовать входящий путь в качестве конечного пути.</span><span class="sxs-lookup"><span data-stu-id="cba93-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="cba93-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="cba93-132">-CustomQueryString</span></span>
<span data-ttu-id="cba93-133">Набор строк запроса, которые должны быть помещены в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="cba93-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="cba93-134">При задании этого значения все имеющиеся строки запроса будут заменены. Оставьте пустым для сохранения строки входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="cba93-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="cba93-135">Строка запроса должна находиться в <key>=</span><span class="sxs-lookup"><span data-stu-id="cba93-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="cba93-136">формате.</span><span class="sxs-lookup"><span data-stu-id="cba93-136">format.</span></span> <span data-ttu-id="cba93-137">Первый?</span><span class="sxs-lookup"><span data-stu-id="cba93-137">The first ?</span></span> <span data-ttu-id="cba93-138">и & будут автоматически добавляться, поэтому не включайте их на передний план, но разделите строки запросов с помощью &.</span><span class="sxs-lookup"><span data-stu-id="cba93-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="cba93-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba93-139">-DefaultProfile</span></span>
<span data-ttu-id="cba93-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cba93-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cba93-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="cba93-141">-DynamicCompression</span></span>
<span data-ttu-id="cba93-142">Следует ли включить динамическое сжатие для кэшированного содержимого, если включено кэширование.</span><span class="sxs-lookup"><span data-stu-id="cba93-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="cba93-143">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="cba93-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="cba93-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="cba93-144">-EnableCaching</span></span>
<span data-ttu-id="cba93-145">Следует ли включить кэширование для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="cba93-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="cba93-146">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="cba93-146">Default value is false</span></span>

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

### <span data-ttu-id="cba93-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cba93-147">-EnabledState</span></span>
<span data-ttu-id="cba93-148">Следует ли включить использование этого правила.</span><span class="sxs-lookup"><span data-stu-id="cba93-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="cba93-149">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="cba93-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="cba93-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="cba93-150">-ForwardingProtocol</span></span>
<span data-ttu-id="cba93-151">Протокол, который будет использоваться этим правилом при пересылке трафика по умолчанию, имеет значение MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="cba93-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba93-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cba93-152">-FrontDoorName</span></span>
<span data-ttu-id="cba93-153">Имя передней дверцы, к которой относится данное правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="cba93-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="cba93-154">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="cba93-154">-FrontendEndpointName</span></span>
<span data-ttu-id="cba93-155">Имена конечных точек с интерфейсом, связанных с этим правилом</span><span class="sxs-lookup"><span data-stu-id="cba93-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="cba93-156">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cba93-156">-Name</span></span>
<span data-ttu-id="cba93-157">RoutingRule имя.</span><span class="sxs-lookup"><span data-stu-id="cba93-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="cba93-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="cba93-158">-PatternToMatch</span></span>
<span data-ttu-id="cba93-159">В шаблонах маршрутов правила не должно быть каких-либо знаков \* за исключением случаев, когда это возможно после конечной точки или в конце пути.</span><span class="sxs-lookup"><span data-stu-id="cba93-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="cba93-160">Значение по умолчанию —/\*</span><span class="sxs-lookup"><span data-stu-id="cba93-160">Default value is /\*</span></span>

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

### <span data-ttu-id="cba93-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="cba93-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="cba93-162">Обработка терминов запроса URL-адреса при создании ключа кэша.</span><span class="sxs-lookup"><span data-stu-id="cba93-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="cba93-163">Значение по умолчанию — StripAll</span><span class="sxs-lookup"><span data-stu-id="cba93-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba93-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="cba93-164">-RedirectProtocol</span></span>
<span data-ttu-id="cba93-165">Протокол назначения, на который перенаправляется трафик.</span><span class="sxs-lookup"><span data-stu-id="cba93-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="cba93-166">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="cba93-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba93-167">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="cba93-167">-RedirectType</span></span>
<span data-ttu-id="cba93-168">Тип перенаправления, который будет использоваться правилом для перенаправления трафика.</span><span class="sxs-lookup"><span data-stu-id="cba93-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="cba93-169">Значение по умолчанию перемещается</span><span class="sxs-lookup"><span data-stu-id="cba93-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba93-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba93-170">-ResourceGroupName</span></span>
<span data-ttu-id="cba93-171">Имя группы ресурсов, в которой будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="cba93-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="cba93-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba93-172">CommonParameters</span></span>
<span data-ttu-id="cba93-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cba93-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba93-174">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cba93-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba93-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cba93-175">INPUTS</span></span>

### <span data-ttu-id="cba93-176">Ничего</span><span class="sxs-lookup"><span data-stu-id="cba93-176">None</span></span>

## <span data-ttu-id="cba93-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba93-177">OUTPUTS</span></span>

### <span data-ttu-id="cba93-178">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cba93-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="cba93-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="cba93-179">NOTES</span></span>

## <span data-ttu-id="cba93-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cba93-180">RELATED LINKS</span></span>

<span data-ttu-id="cba93-181">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="cba93-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
