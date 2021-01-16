---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 0b2b27855e0c8248f0e7ceb9f1c096370a54e2fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408863"
---
# <span data-ttu-id="0c06a-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="0c06a-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="0c06a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c06a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c06a-103">Возвращает результаты поиска, основанные на указанных параметрах.</span><span class="sxs-lookup"><span data-stu-id="0c06a-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="0c06a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c06a-104">SYNTAX</span></span>

### <span data-ttu-id="0c06a-105">ByWorkspaceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c06a-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c06a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0c06a-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c06a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c06a-107">DESCRIPTION</span></span>
<span data-ttu-id="0c06a-108">Cmdlet **Invoke-AzOperationalInsightsQuery** возвращает результаты поиска на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="0c06a-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="0c06a-109">Можно получить доступ к статусу поиска в свойстве "Метаданные" возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="0c06a-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="0c06a-110">Если состояние "Ожидание", то поиск не завершился и результаты будут отданы из архива.</span><span class="sxs-lookup"><span data-stu-id="0c06a-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="0c06a-111">Результаты поиска можно получить из свойства Value (Значение) возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="0c06a-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>
<span data-ttu-id="0c06a-112">Ознакомьтесь с общими ограничениями запросов https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language здесь:</span><span class="sxs-lookup"><span data-stu-id="0c06a-112">Please check detail of general query limits here: https://docs.microsoft.com/en-us/azure/azure-monitor/service-limits#log-queries-and-language.</span></span>

## <span data-ttu-id="0c06a-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c06a-113">EXAMPLES</span></span>

### <span data-ttu-id="0c06a-114">Пример 1. Поиск результатов с помощью запроса</span><span class="sxs-lookup"><span data-stu-id="0c06a-114">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="0c06a-115">После вызова запроса $queryResults.Результаты будут содержать все полученные строки из запроса.</span><span class="sxs-lookup"><span data-stu-id="0c06a-115">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="0c06a-116">Пример 2. Преобразование $results. Результат IEnumerable to an array</span><span class="sxs-lookup"><span data-stu-id="0c06a-116">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="0c06a-117">Некоторые запросы могут привести к очень большому набору данных.</span><span class="sxs-lookup"><span data-stu-id="0c06a-117">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="0c06a-118">В связи с этим по умолчанию для работы cmdlet возвращается значение IEnumerable, чтобы снизить затраты на память.</span><span class="sxs-lookup"><span data-stu-id="0c06a-118">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="0c06a-119">Если вы хотите получить массив результатов, используйте метод расширения LINQ Enumerable.ToArray() для преобразования функции IEnumerable в массив.</span><span class="sxs-lookup"><span data-stu-id="0c06a-119">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="0c06a-120">Пример 3. Поиск результатов с помощью запроса за определенный период времени</span><span class="sxs-lookup"><span data-stu-id="0c06a-120">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="0c06a-121">Результаты этого запроса будут ограничены за последние 24 часа.</span><span class="sxs-lookup"><span data-stu-id="0c06a-121">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="0c06a-122">Пример 4. Включить & отрисовки в результат запроса</span><span class="sxs-lookup"><span data-stu-id="0c06a-122">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="0c06a-123">Подробные [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) сведения об отрисовки и статистике см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="0c06a-123">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="0c06a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c06a-124">PARAMETERS</span></span>

### <span data-ttu-id="0c06a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c06a-125">-AsJob</span></span>
<span data-ttu-id="0c06a-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0c06a-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c06a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c06a-127">-DefaultProfile</span></span>
<span data-ttu-id="0c06a-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c06a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c06a-129">-IncludeRender</span><span class="sxs-lookup"><span data-stu-id="0c06a-129">-IncludeRender</span></span>
<span data-ttu-id="0c06a-130">При этом в ответ включаются данные для метрических запросов.</span><span class="sxs-lookup"><span data-stu-id="0c06a-130">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="0c06a-131">-IncludeStatistics</span><span class="sxs-lookup"><span data-stu-id="0c06a-131">-IncludeStatistics</span></span>
<span data-ttu-id="0c06a-132">При этом в ответ включается статистика запроса.</span><span class="sxs-lookup"><span data-stu-id="0c06a-132">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="0c06a-133">-Query</span><span class="sxs-lookup"><span data-stu-id="0c06a-133">-Query</span></span>
<span data-ttu-id="0c06a-134">Выполняемый запрос.</span><span class="sxs-lookup"><span data-stu-id="0c06a-134">The query to execute.</span></span>

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

### <span data-ttu-id="0c06a-135">-Timespan</span><span class="sxs-lookup"><span data-stu-id="0c06a-135">-Timespan</span></span>
<span data-ttu-id="0c06a-136">Период времени, на который будет привязан запрос.</span><span class="sxs-lookup"><span data-stu-id="0c06a-136">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="0c06a-137">-Wait</span><span class="sxs-lookup"><span data-stu-id="0c06a-137">-Wait</span></span>
<span data-ttu-id="0c06a-138">Устанавливает верхнюю границу на время, необходимое серверу для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="0c06a-138">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="0c06a-139">См.: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="0c06a-139">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="0c06a-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="0c06a-140">-Workspace</span></span>
<span data-ttu-id="0c06a-141">Рабочее пространство</span><span class="sxs-lookup"><span data-stu-id="0c06a-141">The workspace</span></span>

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

### <span data-ttu-id="0c06a-142">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="0c06a-142">-WorkspaceId</span></span>
<span data-ttu-id="0c06a-143">ИД рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0c06a-143">The workspace ID.</span></span>

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

### <span data-ttu-id="0c06a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c06a-144">CommonParameters</span></span>
<span data-ttu-id="0c06a-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c06a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c06a-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c06a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c06a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c06a-147">INPUTS</span></span>

### <span data-ttu-id="0c06a-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c06a-148">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="0c06a-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c06a-149">OUTPUTS</span></span>

### <span data-ttu-id="0c06a-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="0c06a-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="0c06a-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c06a-151">NOTES</span></span>

## <span data-ttu-id="0c06a-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c06a-152">RELATED LINKS</span></span>