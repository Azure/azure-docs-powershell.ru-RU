---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 438F549D-1AF6-49FE-83AC-B45BAB701AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSearchResult.md
ms.openlocfilehash: 47a8edf304ebc5481073151c180c01a65259149c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904694"
---
# <span data-ttu-id="6e118-101">Get-AzOperationalInsightsSearchResult</span><span class="sxs-lookup"><span data-stu-id="6e118-101">Get-AzOperationalInsightsSearchResult</span></span>

## <span data-ttu-id="6e118-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e118-102">SYNOPSIS</span></span>
<span data-ttu-id="6e118-103">Возвращает результаты поиска на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="6e118-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="6e118-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e118-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String> [[-Top] <Int64>]
 [[-PreHighlight] <String>] [[-PostHighlight] <String>] [[-Query] <String>] [[-Start] <DateTime>]
 [[-End] <DateTime>] [[-Id] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e118-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e118-105">DESCRIPTION</span></span>
<span data-ttu-id="6e118-106">Командлет **Get-AzOperationalInsightsSearchResult** возвращает результаты поиска на основе указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="6e118-106">The **Get-AzOperationalInsightsSearchResult** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="6e118-107">Вы можете получить доступ к статусу поиска в свойстве Metadata возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="6e118-107">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="6e118-108">Если состояние имеет значение ожидание, поиск не закончится, и результаты будут отправлены из архива.</span><span class="sxs-lookup"><span data-stu-id="6e118-108">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="6e118-109">Результаты поиска можно получить из свойства Value возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="6e118-109">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="6e118-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e118-110">EXAMPLES</span></span>

### <span data-ttu-id="6e118-111">Пример 1: получение результатов поиска с помощью запроса</span><span class="sxs-lookup"><span data-stu-id="6e118-111">Example 1: Get search results using a query</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Query "Type=Event" -Top 100
```

<span data-ttu-id="6e118-112">Эта команда получает все результаты поиска с помощью запроса.</span><span class="sxs-lookup"><span data-stu-id="6e118-112">This command gets all search results by using a query.</span></span>

### <span data-ttu-id="6e118-113">Пример 2: получение результатов поиска с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="6e118-113">Example 2: Get search results using an ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Id "ContosoSearchId"
```

<span data-ttu-id="6e118-114">Эта команда возвращает результаты поиска с помощью идентификатора.</span><span class="sxs-lookup"><span data-stu-id="6e118-114">This command gets search results by using an ID.</span></span>

### <span data-ttu-id="6e118-115">Пример 3: ожидание завершения поиска перед отображением результатов</span><span class="sxs-lookup"><span data-stu-id="6e118-115">Example 3: Wait for a search to complete before displaying results</span></span>
```
PS C:\>$error.clear()
$response = @{}
$StartTime = Get-Date

$resGroup = "ContosoResourceGroup"
$wrkspace = "ContosoWorkspace"

# Sample Query
$query = "Type=Event"

# Get Initial response
$response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Query $query -Top 15000
$elapsedTime = $(get-date) - $script:StartTime
Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status

# Split and extract request Id
$reqIdParts = $response.Id.Split("/")
$reqId = $reqIdParts[$reqIdParts.Count -1]

# Poll if pending
while($response.Metadata.Status -eq "Pending" -and $error.Count -eq 0) {
    $response = Get-AzOperationalInsightsSearchResult -WorkspaceName $wrkspace -ResourceGroupName $resGroup -Id $reqId
    $elapsedTime = $(get-date) - $script:StartTime
    Write-Host "Elapsed: " $elapsedTime "Status: " $response.Metadata.Status
}

Write-Host "Returned " $response.Value.Count " documents"
Write-Host $error
```

<span data-ttu-id="6e118-116">Этот сценарий запускает поиск и ждет, пока он не завершится, прежде чем отобразить результаты.</span><span class="sxs-lookup"><span data-stu-id="6e118-116">This script starts a search and waits until it completes before displaying the results.</span></span>

## <span data-ttu-id="6e118-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e118-117">PARAMETERS</span></span>

### <span data-ttu-id="6e118-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e118-118">-DefaultProfile</span></span>
<span data-ttu-id="6e118-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6e118-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e118-120">-End</span><span class="sxs-lookup"><span data-stu-id="6e118-120">-End</span></span>
<span data-ttu-id="6e118-121">Конец запрашиваемого интервала времени.</span><span class="sxs-lookup"><span data-stu-id="6e118-121">End of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-122">-ID</span><span class="sxs-lookup"><span data-stu-id="6e118-122">-Id</span></span>
<span data-ttu-id="6e118-123">Если указан идентификатор, результаты поиска для этого идентификатора будут извлекаться с помощью исходных параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="6e118-123">If an id is given, the search results for that id will be retrieved using the original query parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-124">-Выдели</span><span class="sxs-lookup"><span data-stu-id="6e118-124">-PostHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-125">-Выделение</span><span class="sxs-lookup"><span data-stu-id="6e118-125">-PreHighlight</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-126">-Query</span><span class="sxs-lookup"><span data-stu-id="6e118-126">-Query</span></span>
<span data-ttu-id="6e118-127">Запрос поиска, который будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="6e118-127">The search query that will be executed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e118-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e118-129">Имя группы ресурсов, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="6e118-129">The name of the resource group that contains the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-130">-Start</span><span class="sxs-lookup"><span data-stu-id="6e118-130">-Start</span></span>
<span data-ttu-id="6e118-131">Начало запрашиваемого интервала времени.</span><span class="sxs-lookup"><span data-stu-id="6e118-131">Start of the queried time range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-132">-Top</span><span class="sxs-lookup"><span data-stu-id="6e118-132">-Top</span></span>
<span data-ttu-id="6e118-133">Максимальное количество возвращаемых результатов, доступное только в 5000.</span><span class="sxs-lookup"><span data-stu-id="6e118-133">The maximum number of results to be returned, limited to 5000.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 10
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e118-134">-WorkspaceName</span></span>
<span data-ttu-id="6e118-135">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6e118-135">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e118-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e118-136">CommonParameters</span></span>
<span data-ttu-id="6e118-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e118-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e118-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e118-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e118-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e118-139">INPUTS</span></span>

### <span data-ttu-id="6e118-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6e118-140">System.String</span></span>

### <span data-ttu-id="6e118-141">System. Int64</span><span class="sxs-lookup"><span data-stu-id="6e118-141">System.Int64</span></span>

### <span data-ttu-id="6e118-142">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6e118-142">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6e118-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e118-143">OUTPUTS</span></span>

### <span data-ttu-id="6e118-144">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="6e118-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="6e118-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e118-145">NOTES</span></span>

## <span data-ttu-id="6e118-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e118-146">RELATED LINKS</span></span>

[<span data-ttu-id="6e118-147">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="6e118-147">Get-AzOperationalInsightsSavedSearchResult</span></span>](./Get-AzOperationalInsightsSavedSearchResult.md)


