---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504876"
---
# <span data-ttu-id="964b1-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="964b1-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="964b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964b1-102">SYNOPSIS</span></span>
<span data-ttu-id="964b1-103">Создайте объект PSRulesEngineAction для создания правила обн. правил.</span><span class="sxs-lookup"><span data-stu-id="964b1-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="964b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="964b1-104">SYNTAX</span></span>

### <span data-ttu-id="964b1-105">ByFieldsWithForwardingParameterSet</span><span class="sxs-lookup"><span data-stu-id="964b1-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="964b1-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="964b1-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="964b1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="964b1-107">DESCRIPTION</span></span>
<span data-ttu-id="964b1-108">Создайте объект PSRulesEngineAction для создания правила обн. правил.</span><span class="sxs-lookup"><span data-stu-id="964b1-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="964b1-109">Используйте cmdlet "New-AzFrontDoorHeaderActionObject" для создания PSHeaderObjects, которые должны передаваться в параметры "-RequestHeaderActions" и "-ResponseHeaderActions".</span><span class="sxs-lookup"><span data-stu-id="964b1-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="964b1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="964b1-110">EXAMPLES</span></span>

### <span data-ttu-id="964b1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="964b1-111">Example 1</span></span>
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

<span data-ttu-id="964b1-112">Создайте действие обдвижки правил и покажите, как просмотреть свойства созданного действия.</span><span class="sxs-lookup"><span data-stu-id="964b1-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="964b1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="964b1-113">PARAMETERS</span></span>

### <span data-ttu-id="964b1-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="964b1-114">-BackendPoolName</span></span>
<span data-ttu-id="964b1-115">Имя backendPool, к которому это правило перенаправить</span><span class="sxs-lookup"><span data-stu-id="964b1-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="964b1-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="964b1-116">-CustomForwardingPath</span></span>
<span data-ttu-id="964b1-117">Настраиваемый путь, используемый для переописи путей ресурсов, которые соответствуют этому правилу.</span><span class="sxs-lookup"><span data-stu-id="964b1-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="964b1-118">Оставьте пустым, чтобы использовать входящие пути.</span><span class="sxs-lookup"><span data-stu-id="964b1-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="964b1-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="964b1-119">-CustomFragment</span></span>
<span data-ttu-id="964b1-120">Фрагмент для добавления в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="964b1-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="964b1-121">Фрагмент — это часть URL-адреса, которая появляется после #.</span><span class="sxs-lookup"><span data-stu-id="964b1-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="964b1-122">Не включаем</span><span class="sxs-lookup"><span data-stu-id="964b1-122">Do not include the #.</span></span>

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

### <span data-ttu-id="964b1-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="964b1-123">-CustomHost</span></span>
<span data-ttu-id="964b1-124">Host to redirect (Перенаправление) host (Перена</span><span class="sxs-lookup"><span data-stu-id="964b1-124">Host to redirect.</span></span>
<span data-ttu-id="964b1-125">Оставьте пустым, чтобы использовать входящие хост в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="964b1-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="964b1-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="964b1-126">-CustomPath</span></span>
<span data-ttu-id="964b1-127">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="964b1-127">The full path to redirect.</span></span>
<span data-ttu-id="964b1-128">Путь не может быть пустым и должен начинаться с /.</span><span class="sxs-lookup"><span data-stu-id="964b1-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="964b1-129">Оставьте пустым, чтобы использовать входящий путь в качестве пути назначения.</span><span class="sxs-lookup"><span data-stu-id="964b1-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="964b1-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="964b1-130">-CustomQueryString</span></span>
<span data-ttu-id="964b1-131">Набор строк запроса, которые нужно поместить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="964b1-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="964b1-132">Если это значение заместит любую существующую строку запроса; оставьте пустым, чтобы сохранить строку входящих запросов.</span><span class="sxs-lookup"><span data-stu-id="964b1-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="964b1-133">Строка запроса должна быть в \<key\> = \<value\> формате.</span><span class="sxs-lookup"><span data-stu-id="964b1-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="964b1-134">Первый ?</span><span class="sxs-lookup"><span data-stu-id="964b1-134">The first ?</span></span>
<span data-ttu-id="964b1-135">и & будут добавлены автоматически, поэтому не включайте их в запрос, но разделяйте несколько строк запроса &.</span><span class="sxs-lookup"><span data-stu-id="964b1-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="964b1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964b1-136">-DefaultProfile</span></span>
<span data-ttu-id="964b1-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="964b1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964b1-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="964b1-138">-DynamicCompression</span></span>
<span data-ttu-id="964b1-139">Следует ли включить динамическое сжатие кэшного содержимого.</span><span class="sxs-lookup"><span data-stu-id="964b1-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="964b1-140">Значение по умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="964b1-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="964b1-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="964b1-141">-EnableCaching</span></span>
<span data-ttu-id="964b1-142">Следует ли включить кэшинг для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="964b1-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="964b1-143">Значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="964b1-143">Default value is false</span></span>

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

### <span data-ttu-id="964b1-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="964b1-144">-ForwardingProtocol</span></span>
<span data-ttu-id="964b1-145">Протокол, который будет применяться этим правилом при перенаправить трафик на backends.</span><span class="sxs-lookup"><span data-stu-id="964b1-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="964b1-146">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="964b1-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="964b1-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="964b1-147">-FrontDoorName</span></span>
<span data-ttu-id="964b1-148">Название переднего входа, к которому относится это правило маршрутинга.</span><span class="sxs-lookup"><span data-stu-id="964b1-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="964b1-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="964b1-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="964b1-150">Обработка условий URL-запроса при формировании ключа кэша.</span><span class="sxs-lookup"><span data-stu-id="964b1-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="964b1-151">Значение по умолчанию — StripAll</span><span class="sxs-lookup"><span data-stu-id="964b1-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="964b1-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="964b1-152">-RedirectProtocol</span></span>
<span data-ttu-id="964b1-153">Протокол назначения, в который перенаправляется трафик.</span><span class="sxs-lookup"><span data-stu-id="964b1-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="964b1-154">Значение по умолчанию — MatchRequest</span><span class="sxs-lookup"><span data-stu-id="964b1-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="964b1-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="964b1-155">-RedirectType</span></span>
<span data-ttu-id="964b1-156">Тип перенаправления, который будет применяться правилом при перенаправлении трафика.</span><span class="sxs-lookup"><span data-stu-id="964b1-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="964b1-157">Значение по умолчанию перемещено</span><span class="sxs-lookup"><span data-stu-id="964b1-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="964b1-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="964b1-158">-RequestHeaderAction</span></span>
<span data-ttu-id="964b1-159">Список действий с заглавным началом из запроса от AFD.</span><span class="sxs-lookup"><span data-stu-id="964b1-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

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

### <span data-ttu-id="964b1-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964b1-160">-ResourceGroupName</span></span>
<span data-ttu-id="964b1-161">Имя группы ресурсов, в которую будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="964b1-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="964b1-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="964b1-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="964b1-163">Список действий с загонами, которые должны применяться в ответе AFD для клиента.</span><span class="sxs-lookup"><span data-stu-id="964b1-163">A list of header actions to apply from the response from AFD to the client.</span></span>

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

### <span data-ttu-id="964b1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964b1-164">CommonParameters</span></span>
<span data-ttu-id="964b1-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="964b1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964b1-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="964b1-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964b1-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="964b1-167">INPUTS</span></span>

### <span data-ttu-id="964b1-168">Нет</span><span class="sxs-lookup"><span data-stu-id="964b1-168">None</span></span>

## <span data-ttu-id="964b1-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="964b1-169">OUTPUTS</span></span>

### <span data-ttu-id="964b1-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="964b1-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="964b1-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="964b1-171">NOTES</span></span>

## <span data-ttu-id="964b1-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="964b1-172">RELATED LINKS</span></span>
