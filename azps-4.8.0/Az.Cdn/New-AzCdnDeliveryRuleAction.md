---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079822"
---
# <span data-ttu-id="342c5-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="342c5-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="342c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="342c5-102">SYNOPSIS</span></span>
<span data-ttu-id="342c5-103">Создание действия доставки.</span><span class="sxs-lookup"><span data-stu-id="342c5-103">Creates a delivery action.</span></span>

## <span data-ttu-id="342c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="342c5-104">SYNTAX</span></span>

### <span data-ttu-id="342c5-105">CacheExpirationActionParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="342c5-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342c5-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="342c5-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342c5-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="342c5-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342c5-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="342c5-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342c5-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="342c5-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342c5-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="342c5-110">DESCRIPTION</span></span>
<span data-ttu-id="342c5-111">Командлет **New-AzCdnDeliveryRule** создает правило доставки для создания КОНЕЧНОЙ точки CDN.</span><span class="sxs-lookup"><span data-stu-id="342c5-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="342c5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="342c5-112">EXAMPLES</span></span>

### <span data-ttu-id="342c5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="342c5-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="342c5-114">Создание простого правила доставки.</span><span class="sxs-lookup"><span data-stu-id="342c5-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="342c5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="342c5-115">PARAMETERS</span></span>

### <span data-ttu-id="342c5-116">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="342c5-116">-Action</span></span>
<span data-ttu-id="342c5-117">Действие, которое нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="342c5-117">Action to perform.</span></span>

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

### <span data-ttu-id="342c5-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="342c5-118">-CacheBehavior</span></span>
<span data-ttu-id="342c5-119">Кэширование поведения для действия</span><span class="sxs-lookup"><span data-stu-id="342c5-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="342c5-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="342c5-120">-CacheDuration</span></span>
<span data-ttu-id="342c5-121">Продолжительность кэширования содержимого.</span><span class="sxs-lookup"><span data-stu-id="342c5-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="342c5-122">Разрешенный формат — \[ d. \] чч: мм: СС</span><span class="sxs-lookup"><span data-stu-id="342c5-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="342c5-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="342c5-123">-CustomFragment</span></span>
<span data-ttu-id="342c5-124">Фрагмент, который нужно добавить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="342c5-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="342c5-125">Фрагмент — это часть URL-адреса, который приходится на следующий адрес:</span><span class="sxs-lookup"><span data-stu-id="342c5-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="342c5-126">Не включайте номер #.</span><span class="sxs-lookup"><span data-stu-id="342c5-126">Do not include the #.</span></span>

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

### <span data-ttu-id="342c5-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="342c5-127">-CustomHostname</span></span>
<span data-ttu-id="342c5-128">Hosting (перенаправление).</span><span class="sxs-lookup"><span data-stu-id="342c5-128">Host to redirect.</span></span>
<span data-ttu-id="342c5-129">Оставьте пустым, чтобы использовать узел входящей почты в качестве узла назначения.</span><span class="sxs-lookup"><span data-stu-id="342c5-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="342c5-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="342c5-130">-CustomPath</span></span>
<span data-ttu-id="342c5-131">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="342c5-131">The full path to redirect.</span></span>
<span data-ttu-id="342c5-132">Путь не может быть пустым и должен начинаться с/.</span><span class="sxs-lookup"><span data-stu-id="342c5-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="342c5-133">Оставьте пустым, чтобы использовать входящий путь в качестве конечного пути.</span><span class="sxs-lookup"><span data-stu-id="342c5-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="342c5-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="342c5-134">-CustomQueryString</span></span>
<span data-ttu-id="342c5-135">Набор строк запроса, которые должны быть помещены в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="342c5-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="342c5-136">При задании этого значения все имеющиеся строки запроса будут заменены. Оставьте пустым для сохранения строки входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="342c5-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="342c5-137">Строка запроса должна иметь \<key\> = \<value\> Формат.</span><span class="sxs-lookup"><span data-stu-id="342c5-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="342c5-138">?</span><span class="sxs-lookup"><span data-stu-id="342c5-138">?</span></span> <span data-ttu-id="342c5-139">и & будут добавлены автоматически, поэтому их не нужно включать.</span><span class="sxs-lookup"><span data-stu-id="342c5-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="342c5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342c5-140">-DefaultProfile</span></span>
<span data-ttu-id="342c5-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="342c5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="342c5-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="342c5-142">-Destination</span></span>
<span data-ttu-id="342c5-143">Определите относительный URL-адрес, на который будут переписываться указанные выше запросы.</span><span class="sxs-lookup"><span data-stu-id="342c5-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="342c5-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="342c5-144">-DestinationProtocol</span></span>
<span data-ttu-id="342c5-145">Протокол, используемый для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="342c5-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="342c5-146">Значением по умолчанию является MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="342c5-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="342c5-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="342c5-147">-HeaderActionType</span></span>
<span data-ttu-id="342c5-148">Необходимость изменения заголовка запроса или ответа</span><span class="sxs-lookup"><span data-stu-id="342c5-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="342c5-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="342c5-149">-HeaderName</span></span>
<span data-ttu-id="342c5-150">Имя заголовка, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="342c5-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="342c5-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="342c5-151">-PreservePath</span></span>
<span data-ttu-id="342c5-152">Следует ли сохранять несовпадающие пути.</span><span class="sxs-lookup"><span data-stu-id="342c5-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="342c5-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="342c5-153">-QueryParameter</span></span>
<span data-ttu-id="342c5-154">Параметры запроса, которые нужно включить или исключить (с разделителями-запятыми).</span><span class="sxs-lookup"><span data-stu-id="342c5-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="342c5-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="342c5-155">-QueryStringBehavior</span></span>
<span data-ttu-id="342c5-156">Поведение запроса QueryString для запросов</span><span class="sxs-lookup"><span data-stu-id="342c5-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="342c5-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="342c5-157">-RedirectType</span></span>
<span data-ttu-id="342c5-158">Тип перенаправления, который будет использоваться правилом для перенаправления трафика</span><span class="sxs-lookup"><span data-stu-id="342c5-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="342c5-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="342c5-159">-SourcePattern</span></span>
<span data-ttu-id="342c5-160">Определите шаблон URI запроса, указывающий тип запросов, которые можно переписать.</span><span class="sxs-lookup"><span data-stu-id="342c5-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="342c5-161">Если значение пусто, все строки совпадают.</span><span class="sxs-lookup"><span data-stu-id="342c5-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="342c5-162">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="342c5-162">-Value</span></span>
<span data-ttu-id="342c5-163">Значение для указанного действия.</span><span class="sxs-lookup"><span data-stu-id="342c5-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="342c5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342c5-164">CommonParameters</span></span>
<span data-ttu-id="342c5-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="342c5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342c5-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="342c5-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342c5-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="342c5-167">INPUTS</span></span>

### <span data-ttu-id="342c5-168">Ничего</span><span class="sxs-lookup"><span data-stu-id="342c5-168">None</span></span>

## <span data-ttu-id="342c5-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="342c5-169">OUTPUTS</span></span>

### <span data-ttu-id="342c5-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="342c5-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="342c5-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="342c5-171">NOTES</span></span>

## <span data-ttu-id="342c5-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="342c5-172">RELATED LINKS</span></span>
