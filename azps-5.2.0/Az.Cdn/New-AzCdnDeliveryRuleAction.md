---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396439"
---
# <span data-ttu-id="527e0-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="527e0-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="527e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="527e0-102">SYNOPSIS</span></span>
<span data-ttu-id="527e0-103">Создает действие доставки.</span><span class="sxs-lookup"><span data-stu-id="527e0-103">Creates a delivery action.</span></span>

## <span data-ttu-id="527e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="527e0-104">SYNTAX</span></span>

### <span data-ttu-id="527e0-105">CacheExpirationActionParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="527e0-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527e0-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="527e0-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527e0-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="527e0-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527e0-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="527e0-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527e0-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="527e0-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="527e0-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="527e0-110">DESCRIPTION</span></span>
<span data-ttu-id="527e0-111">Для создания конечной точки CDN создается правило доставки для **new-AzCdnDeliveryRule.**</span><span class="sxs-lookup"><span data-stu-id="527e0-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="527e0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="527e0-112">EXAMPLES</span></span>

### <span data-ttu-id="527e0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="527e0-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="527e0-114">Создайте простое правило доставки.</span><span class="sxs-lookup"><span data-stu-id="527e0-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="527e0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="527e0-115">PARAMETERS</span></span>

### <span data-ttu-id="527e0-116">-Action</span><span class="sxs-lookup"><span data-stu-id="527e0-116">-Action</span></span>
<span data-ttu-id="527e0-117">Необходимое действие.</span><span class="sxs-lookup"><span data-stu-id="527e0-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="527e0-118">-CacheBehavior</span></span>
<span data-ttu-id="527e0-119">Кэшинг действия</span><span class="sxs-lookup"><span data-stu-id="527e0-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="527e0-120">-CacheDuration</span></span>
<span data-ttu-id="527e0-121">Длительность, в течение которой содержимое должно быть в кэше.</span><span class="sxs-lookup"><span data-stu-id="527e0-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="527e0-122">Допустимый формат \[ d. \] чч:мм:сс</span><span class="sxs-lookup"><span data-stu-id="527e0-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="527e0-123">-CustomFragment</span></span>
<span data-ttu-id="527e0-124">Фрагмент для добавления в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="527e0-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="527e0-125">Фрагмент — это часть URL-адреса, которая появляется после #.</span><span class="sxs-lookup"><span data-stu-id="527e0-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="527e0-126">Не включаем</span><span class="sxs-lookup"><span data-stu-id="527e0-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="527e0-127">-CustomHostname</span></span>
<span data-ttu-id="527e0-128">Host to redirect (Перенаправление) host (Перена</span><span class="sxs-lookup"><span data-stu-id="527e0-128">Host to redirect.</span></span>
<span data-ttu-id="527e0-129">Оставьте пустым, чтобы использовать входящие хост в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="527e0-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="527e0-130">-CustomPath</span></span>
<span data-ttu-id="527e0-131">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="527e0-131">The full path to redirect.</span></span>
<span data-ttu-id="527e0-132">Путь не может быть пустым и должен начинаться с /.</span><span class="sxs-lookup"><span data-stu-id="527e0-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="527e0-133">Оставьте пустым, чтобы использовать входящий путь в качестве пути назначения.</span><span class="sxs-lookup"><span data-stu-id="527e0-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="527e0-134">-CustomQueryString</span></span>
<span data-ttu-id="527e0-135">Набор строк запроса, которые нужно поместить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="527e0-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="527e0-136">Если это значение заместит любую существующую строку запроса; оставьте пустым, чтобы сохранить строку входящих запросов.</span><span class="sxs-lookup"><span data-stu-id="527e0-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="527e0-137">Строка запроса должна быть в \<key\> = \<value\> формате.</span><span class="sxs-lookup"><span data-stu-id="527e0-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="527e0-138">?</span><span class="sxs-lookup"><span data-stu-id="527e0-138">?</span></span> <span data-ttu-id="527e0-139">и & будут добавлены автоматически, поэтому не включайте их.</span><span class="sxs-lookup"><span data-stu-id="527e0-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="527e0-140">-DefaultProfile</span></span>
<span data-ttu-id="527e0-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="527e0-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="527e0-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="527e0-142">-Destination</span></span>
<span data-ttu-id="527e0-143">Определите относительный URL-адрес, на который будут перезаписаны выше запросы.</span><span class="sxs-lookup"><span data-stu-id="527e0-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="527e0-144">-DestinationProtocol</span></span>
<span data-ttu-id="527e0-145">Протокол для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="527e0-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="527e0-146">Значение по умолчанию — MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="527e0-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="527e0-147">-HeaderActionType</span></span>
<span data-ttu-id="527e0-148">Изменение загона запроса или ответа</span><span class="sxs-lookup"><span data-stu-id="527e0-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="527e0-149">-HeaderName</span></span>
<span data-ttu-id="527e0-150">Имя изменяемого загона.</span><span class="sxs-lookup"><span data-stu-id="527e0-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="527e0-151">-PreservePath</span></span>
<span data-ttu-id="527e0-152">Нужно ли сохранять путь, не относячий к важному.</span><span class="sxs-lookup"><span data-stu-id="527e0-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="527e0-153">-QueryParameter</span></span>
<span data-ttu-id="527e0-154">Параметры запроса, которые нужно включить или исключить (разделив запятую).</span><span class="sxs-lookup"><span data-stu-id="527e0-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="527e0-155">-QueryStringBehavior</span></span>
<span data-ttu-id="527e0-156">Поведение QueryString для запросов</span><span class="sxs-lookup"><span data-stu-id="527e0-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="527e0-157">-RedirectType</span></span>
<span data-ttu-id="527e0-158">Тип перенаправления, который будет применяться правилом при перенаправлении трафика</span><span class="sxs-lookup"><span data-stu-id="527e0-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="527e0-159">-SourcePattern</span></span>
<span data-ttu-id="527e0-160">Определите шаблон URI запроса, определяя тип запросов, которые могут быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="527e0-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="527e0-161">Если значение пустое, со всеми строками будут совметивы все строки.</span><span class="sxs-lookup"><span data-stu-id="527e0-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-162">-Value</span><span class="sxs-lookup"><span data-stu-id="527e0-162">-Value</span></span>
<span data-ttu-id="527e0-163">Значение указанного действия.</span><span class="sxs-lookup"><span data-stu-id="527e0-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527e0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527e0-164">CommonParameters</span></span>
<span data-ttu-id="527e0-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="527e0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527e0-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="527e0-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527e0-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="527e0-167">INPUTS</span></span>

### <span data-ttu-id="527e0-168">Нет</span><span class="sxs-lookup"><span data-stu-id="527e0-168">None</span></span>

## <span data-ttu-id="527e0-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="527e0-169">OUTPUTS</span></span>

### <span data-ttu-id="527e0-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="527e0-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="527e0-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="527e0-171">NOTES</span></span>

## <span data-ttu-id="527e0-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="527e0-172">RELATED LINKS</span></span>