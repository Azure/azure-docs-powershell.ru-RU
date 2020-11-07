---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727587"
---
# <span data-ttu-id="3faaf-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="3faaf-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="3faaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3faaf-102">SYNOPSIS</span></span>
<span data-ttu-id="3faaf-103">Создание действия доставки.</span><span class="sxs-lookup"><span data-stu-id="3faaf-103">Creates a delivery action.</span></span>

## <span data-ttu-id="3faaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3faaf-104">SYNTAX</span></span>

### <span data-ttu-id="3faaf-105">CacheExpirationActionParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3faaf-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3faaf-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3faaf-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3faaf-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3faaf-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3faaf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3faaf-108">DESCRIPTION</span></span>
<span data-ttu-id="3faaf-109">Командлет **New-AzCdnDeliveryRule** создает правило доставки для создания КОНЕЧНОЙ точки CDN.</span><span class="sxs-lookup"><span data-stu-id="3faaf-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="3faaf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3faaf-110">EXAMPLES</span></span>

### <span data-ttu-id="3faaf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3faaf-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="3faaf-112">Создание простого правила доставки.</span><span class="sxs-lookup"><span data-stu-id="3faaf-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="3faaf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3faaf-113">PARAMETERS</span></span>

### <span data-ttu-id="3faaf-114">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="3faaf-114">-Action</span></span>
<span data-ttu-id="3faaf-115">Действие, которое нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="3faaf-115">Action to perform.</span></span>

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

### <span data-ttu-id="3faaf-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="3faaf-116">-CacheBehavior</span></span>
<span data-ttu-id="3faaf-117">Кэширование поведения для действия</span><span class="sxs-lookup"><span data-stu-id="3faaf-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="3faaf-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="3faaf-118">-CacheDuration</span></span>
<span data-ttu-id="3faaf-119">Продолжительность кэширования содержимого.</span><span class="sxs-lookup"><span data-stu-id="3faaf-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="3faaf-120">Разрешенный формат — \[ d. \] чч: мм: СС</span><span class="sxs-lookup"><span data-stu-id="3faaf-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="3faaf-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="3faaf-121">-CustomFragment</span></span>
<span data-ttu-id="3faaf-122">Фрагмент, который нужно добавить в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3faaf-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="3faaf-123">Фрагмент — это часть URL-адреса, который приходится на следующий адрес:</span><span class="sxs-lookup"><span data-stu-id="3faaf-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="3faaf-124">Не включайте номер #.</span><span class="sxs-lookup"><span data-stu-id="3faaf-124">Do not include the #.</span></span>

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

### <span data-ttu-id="3faaf-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="3faaf-125">-CustomHostname</span></span>
<span data-ttu-id="3faaf-126">Hosting (перенаправление).</span><span class="sxs-lookup"><span data-stu-id="3faaf-126">Host to redirect.</span></span>
<span data-ttu-id="3faaf-127">Оставьте пустым, чтобы использовать узел входящей почты в качестве узла назначения.</span><span class="sxs-lookup"><span data-stu-id="3faaf-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="3faaf-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="3faaf-128">-CustomPath</span></span>
<span data-ttu-id="3faaf-129">Полный путь для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3faaf-129">The full path to redirect.</span></span>
<span data-ttu-id="3faaf-130">Путь не может быть пустым и должен начинаться с/.</span><span class="sxs-lookup"><span data-stu-id="3faaf-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="3faaf-131">Оставьте пустым, чтобы использовать входящий путь в качестве конечного пути.</span><span class="sxs-lookup"><span data-stu-id="3faaf-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="3faaf-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="3faaf-132">-CustomQueryString</span></span>
<span data-ttu-id="3faaf-133">Набор строк запроса, которые должны быть помещены в URL-адрес перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3faaf-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="3faaf-134">При задании этого значения все имеющиеся строки запроса будут заменены. Оставьте пустым для сохранения строки входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="3faaf-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="3faaf-135">Строка запроса должна быть в \< \> = \< формате значения ключа \> .</span><span class="sxs-lookup"><span data-stu-id="3faaf-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="3faaf-136">?</span><span class="sxs-lookup"><span data-stu-id="3faaf-136">?</span></span> <span data-ttu-id="3faaf-137">и & будут добавлены автоматически, поэтому их не нужно включать.</span><span class="sxs-lookup"><span data-stu-id="3faaf-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="3faaf-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3faaf-138">-DefaultProfile</span></span>
<span data-ttu-id="3faaf-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3faaf-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3faaf-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="3faaf-140">-DestinationProtocol</span></span>
<span data-ttu-id="3faaf-141">Протокол, используемый для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3faaf-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="3faaf-142">Значением по умолчанию является MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="3faaf-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="3faaf-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="3faaf-143">-HeaderActionType</span></span>
<span data-ttu-id="3faaf-144">Необходимость изменения заголовка запроса или ответа</span><span class="sxs-lookup"><span data-stu-id="3faaf-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="3faaf-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="3faaf-145">-HeaderName</span></span>
<span data-ttu-id="3faaf-146">Имя заголовка, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3faaf-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="3faaf-147">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="3faaf-147">-RedirectType</span></span>
<span data-ttu-id="3faaf-148">Тип перенаправления, который будет использоваться правилом для перенаправления трафика</span><span class="sxs-lookup"><span data-stu-id="3faaf-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="3faaf-149">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="3faaf-149">-Value</span></span>
<span data-ttu-id="3faaf-150">Значение для указанного действия.</span><span class="sxs-lookup"><span data-stu-id="3faaf-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="3faaf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3faaf-151">CommonParameters</span></span>
<span data-ttu-id="3faaf-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3faaf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3faaf-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3faaf-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3faaf-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3faaf-154">INPUTS</span></span>

### <span data-ttu-id="3faaf-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="3faaf-155">None</span></span>

## <span data-ttu-id="3faaf-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3faaf-156">OUTPUTS</span></span>

### <span data-ttu-id="3faaf-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="3faaf-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="3faaf-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="3faaf-158">NOTES</span></span>

## <span data-ttu-id="3faaf-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3faaf-159">RELATED LINKS</span></span>
