---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242776"
---
# <span data-ttu-id="e439e-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="e439e-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="e439e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e439e-102">SYNOPSIS</span></span>
<span data-ttu-id="e439e-103">Создайте объект PSRulesEngineAction для создания правила обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="e439e-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="e439e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e439e-104">SYNTAX</span></span>

### <span data-ttu-id="e439e-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="e439e-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e439e-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e439e-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e439e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e439e-107">DESCRIPTION</span></span>
<span data-ttu-id="e439e-108">Создайте объект PSRulesEngineAction для создания правила обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="e439e-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="e439e-109">Используйте командлет "New-AzFrontDoorHeaderActionObject" для создания PSHeaderObjects, чтобы передать параметры "-RequestHeaderActions" и "-ResponseHeaderActions". "</span><span class="sxs-lookup"><span data-stu-id="e439e-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="e439e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e439e-110">EXAMPLES</span></span>

### <span data-ttu-id="e439e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e439e-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="e439e-112">Создание действия обработчика правил и демонстрация просмотра свойств созданного действия обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="e439e-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="e439e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e439e-113">PARAMETERS</span></span>

### <span data-ttu-id="e439e-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="e439e-114">-BackendPoolName</span></span>
<span data-ttu-id="e439e-115">Имя BackendPool, к которому это правило адресуется</span><span class="sxs-lookup"><span data-stu-id="e439e-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="e439e-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="e439e-116">-CustomForwardingPath</span></span>
<span data-ttu-id="e439e-117">Настраиваемый путь, используемый для перезаписи путей к ресурсам, подходящих для этого правила.</span><span class="sxs-lookup"><span data-stu-id="e439e-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="e439e-118">Оставьте поле пустым, чтобы использовать входящий путь.</span><span class="sxs-lookup"><span data-stu-id="e439e-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="e439e-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="e439e-119">-CustomFragment</span></span>
<span data-ttu-id="e439e-120">Фрагмент, который нужно добавить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e439e-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="e439e-121">Фрагмент — это часть URL-адреса, который приходится на следующий адрес:</span><span class="sxs-lookup"><span data-stu-id="e439e-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="e439e-122">Не включайте номер #.</span><span class="sxs-lookup"><span data-stu-id="e439e-122">Do not include the #.</span></span>

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

### <span data-ttu-id="e439e-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="e439e-123">-CustomHost</span></span>
<span data-ttu-id="e439e-124">Hosting (перенаправление).</span><span class="sxs-lookup"><span data-stu-id="e439e-124">Host to redirect.</span></span>
<span data-ttu-id="e439e-125">Оставьте пустым, чтобы использовать узел входящей почты в качестве узла назначения.</span><span class="sxs-lookup"><span data-stu-id="e439e-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="e439e-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="e439e-126">-CustomPath</span></span>
<span data-ttu-id="e439e-127">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e439e-127">The full path to redirect.</span></span>
<span data-ttu-id="e439e-128">Путь не может быть пустым и должен начинаться с/.</span><span class="sxs-lookup"><span data-stu-id="e439e-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="e439e-129">Оставьте пустым, чтобы использовать входящий путь в качестве конечного пути.</span><span class="sxs-lookup"><span data-stu-id="e439e-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="e439e-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="e439e-130">-CustomQueryString</span></span>
<span data-ttu-id="e439e-131">Набор строк запроса, которые должны быть помещены в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e439e-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="e439e-132">При задании этого значения все имеющиеся строки запроса будут заменены. Оставьте пустым для сохранения строки входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="e439e-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="e439e-133">Строка запроса должна иметь \<key\> = \<value\> Формат.</span><span class="sxs-lookup"><span data-stu-id="e439e-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="e439e-134">Первый?</span><span class="sxs-lookup"><span data-stu-id="e439e-134">The first ?</span></span>
<span data-ttu-id="e439e-135">и & будут автоматически добавляться, поэтому не включайте их на передний план, но разделите строки запросов с помощью &.</span><span class="sxs-lookup"><span data-stu-id="e439e-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="e439e-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e439e-136">-DefaultProfile</span></span>
<span data-ttu-id="e439e-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e439e-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e439e-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="e439e-138">-DynamicCompression</span></span>
<span data-ttu-id="e439e-139">Следует ли включить динамическое сжатие для кэшированного содержимого.</span><span class="sxs-lookup"><span data-stu-id="e439e-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="e439e-140">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="e439e-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="e439e-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="e439e-141">-EnableCaching</span></span>
<span data-ttu-id="e439e-142">Следует ли включить кэширование для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="e439e-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="e439e-143">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="e439e-143">Default value is false</span></span>

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

### <span data-ttu-id="e439e-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="e439e-144">-ForwardingProtocol</span></span>
<span data-ttu-id="e439e-145">Протокол, который будет использоваться этим правилом при пересылке трафика в "незавершенные".</span><span class="sxs-lookup"><span data-stu-id="e439e-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="e439e-146">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="e439e-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="e439e-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e439e-147">-FrontDoorName</span></span>
<span data-ttu-id="e439e-148">Имя передней дверцы, к которой относится данное правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e439e-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="e439e-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="e439e-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="e439e-150">Обработка терминов запроса URL-адреса при создании ключа кэша.</span><span class="sxs-lookup"><span data-stu-id="e439e-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="e439e-151">Значение по умолчанию — StripAll</span><span class="sxs-lookup"><span data-stu-id="e439e-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="e439e-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="e439e-152">-RedirectProtocol</span></span>
<span data-ttu-id="e439e-153">Протокол назначения, на который перенаправляется трафик.</span><span class="sxs-lookup"><span data-stu-id="e439e-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="e439e-154">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="e439e-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="e439e-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="e439e-155">-RedirectType</span></span>
<span data-ttu-id="e439e-156">Тип перенаправления, который будет использоваться правилом для перенаправления трафика.</span><span class="sxs-lookup"><span data-stu-id="e439e-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="e439e-157">Значение по умолчанию перемещается</span><span class="sxs-lookup"><span data-stu-id="e439e-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="e439e-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="e439e-158">-RequestHeaderAction</span></span>
<span data-ttu-id="e439e-159">Список макрокоманд-заголовков, применяемых к запросу из AFD к источнику.</span><span class="sxs-lookup"><span data-stu-id="e439e-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439e-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e439e-160">-ResourceGroupName</span></span>
<span data-ttu-id="e439e-161">Имя группы ресурсов, в которой будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="e439e-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="e439e-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="e439e-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="e439e-163">Список действий заголовков, применяемых к ответу от AFD на клиент.</span><span class="sxs-lookup"><span data-stu-id="e439e-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e439e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e439e-164">CommonParameters</span></span>
<span data-ttu-id="e439e-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e439e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e439e-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e439e-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e439e-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e439e-167">INPUTS</span></span>

### <span data-ttu-id="e439e-168">Ничего</span><span class="sxs-lookup"><span data-stu-id="e439e-168">None</span></span>

## <span data-ttu-id="e439e-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e439e-169">OUTPUTS</span></span>

### <span data-ttu-id="e439e-170">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="e439e-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="e439e-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="e439e-171">NOTES</span></span>

## <span data-ttu-id="e439e-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e439e-172">RELATED LINKS</span></span>
