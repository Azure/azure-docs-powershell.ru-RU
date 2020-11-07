---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 1df2e8fc82ba071692f8c7b5bf677d275c429323
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904678"
---
# <span data-ttu-id="3b371-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="3b371-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="3b371-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b371-102">SYNOPSIS</span></span>
<span data-ttu-id="3b371-103">Возвращает результаты поиска на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="3b371-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="3b371-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b371-104">SYNTAX</span></span>

### <span data-ttu-id="3b371-105">ByWorkspaceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b371-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b371-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3b371-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b371-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b371-107">DESCRIPTION</span></span>
<span data-ttu-id="3b371-108">Командлет **Invoke-AzOperationalInsightsQuery** возвращает результаты поиска на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="3b371-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="3b371-109">Вы можете получить доступ к статусу поиска в свойстве Metadata возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="3b371-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="3b371-110">Если состояние имеет значение ожидание, поиск не закончится, и результаты будут отправлены из архива.</span><span class="sxs-lookup"><span data-stu-id="3b371-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="3b371-111">Результаты поиска можно получить из свойства Value возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="3b371-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="3b371-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b371-112">EXAMPLES</span></span>

### <span data-ttu-id="3b371-113">Пример 1: получение результатов поиска с помощью запроса</span><span class="sxs-lookup"><span data-stu-id="3b371-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="3b371-114">После вызова $queryResults. Results будет содержать все результирующие строки из запроса.</span><span class="sxs-lookup"><span data-stu-id="3b371-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="3b371-115">Пример 2: Convert $results. Результат IEnumerable с массивом</span><span class="sxs-lookup"><span data-stu-id="3b371-115">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="3b371-116">Некоторые запросы могут привести к возврату очень больших наборов данных.</span><span class="sxs-lookup"><span data-stu-id="3b371-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="3b371-117">По этой причине по умолчанию командлет возвращает интерфейс IEnumerable, чтобы снизить стоимость памяти.</span><span class="sxs-lookup"><span data-stu-id="3b371-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="3b371-118">Если вы предпочитаете получить массив результатов, можно использовать метод расширения LINQ Enumerable. ToArray () для преобразования IEnumerable в массив.</span><span class="sxs-lookup"><span data-stu-id="3b371-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="3b371-119">Пример 3: получение результатов поиска с помощью запроса за определенный период времени</span><span class="sxs-lookup"><span data-stu-id="3b371-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="3b371-120">Результаты из этого запроса будут ограничены на последние 24 часа.</span><span class="sxs-lookup"><span data-stu-id="3b371-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="3b371-121">Пример 4: включение статистики & отображения в результатах запроса</span><span class="sxs-lookup"><span data-stu-id="3b371-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="3b371-122">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Подробнее об отображении и сведениях о статистике см.</span><span class="sxs-lookup"><span data-stu-id="3b371-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="3b371-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b371-123">PARAMETERS</span></span>

### <span data-ttu-id="3b371-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b371-124">-AsJob</span></span>
<span data-ttu-id="3b371-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3b371-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b371-126">-DefaultProfile</span></span>
<span data-ttu-id="3b371-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b371-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b371-128">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="3b371-128">-IncludeRender</span></span>
<span data-ttu-id="3b371-129">Если задано, сведения о отрисовке запросов метрик будут включены в ответ.</span><span class="sxs-lookup"><span data-stu-id="3b371-129">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-130">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="3b371-130">-IncludeStatistics</span></span>
<span data-ttu-id="3b371-131">Если задано значение, статистика запроса будет включена в ответ.</span><span class="sxs-lookup"><span data-stu-id="3b371-131">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-132">-Query</span><span class="sxs-lookup"><span data-stu-id="3b371-132">-Query</span></span>
<span data-ttu-id="3b371-133">Запрос, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="3b371-133">The query to execute.</span></span>

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

### <span data-ttu-id="3b371-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="3b371-134">-Timespan</span></span>
<span data-ttu-id="3b371-135">Интервал времени, по которому необходимо выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="3b371-135">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-136">-Wait</span><span class="sxs-lookup"><span data-stu-id="3b371-136">-Wait</span></span>
<span data-ttu-id="3b371-137">Применяет верхнюю границу к количеству времени, которое сервер тратит на обработку запроса.</span><span class="sxs-lookup"><span data-stu-id="3b371-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="3b371-138">Обнаружить https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="3b371-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-139">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="3b371-139">-Workspace</span></span>
<span data-ttu-id="3b371-140">Рабочая область</span><span class="sxs-lookup"><span data-stu-id="3b371-140">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-141">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3b371-141">-WorkspaceId</span></span>
<span data-ttu-id="3b371-142">ИДЕНТИФИКАТОР рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b371-142">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b371-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b371-143">CommonParameters</span></span>
<span data-ttu-id="3b371-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b371-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b371-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b371-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b371-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b371-146">INPUTS</span></span>

### <span data-ttu-id="3b371-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3b371-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="3b371-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b371-148">OUTPUTS</span></span>

### <span data-ttu-id="3b371-149">Microsoft. Azure. Commands. OperationalInsights. Models. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="3b371-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="3b371-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b371-150">NOTES</span></span>

## <span data-ttu-id="3b371-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b371-151">RELATED LINKS</span></span>
