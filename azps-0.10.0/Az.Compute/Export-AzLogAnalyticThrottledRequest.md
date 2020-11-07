---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-AzLogAnalyticThrottledRequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 45f0a75b07d0fae07092ffbe2b23f42cfa6d707a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911567"
---
# <span data-ttu-id="c22e9-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="c22e9-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="c22e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c22e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c22e9-103">Экспорт журналов, показывающих общее число запросов API для подписки в заданном окне времени.</span><span class="sxs-lookup"><span data-stu-id="c22e9-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="c22e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c22e9-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String>
 [-GroupByOperationName]  [-GroupByThrottlePolicy] [-GroupByResourceName] 
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c22e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c22e9-105">DESCRIPTION</span></span>
<span data-ttu-id="c22e9-106">Это экспортирует общее количество запросов API Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="c22e9-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="c22e9-107">Журналы можно дополнительно объединять тремя вариантами: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="c22e9-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="c22e9-108">Обратите внимание, что этот командлет собирает только CRP журналы.</span><span class="sxs-lookup"><span data-stu-id="c22e9-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="c22e9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c22e9-109">EXAMPLES</span></span>

### <span data-ttu-id="c22e9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c22e9-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="c22e9-111">Эта команда хранит общее число вызовов API Microsoft. COMPUTE между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в заданном URI SAS, агрегированные по названию операции.</span><span class="sxs-lookup"><span data-stu-id="c22e9-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="c22e9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c22e9-112">PARAMETERS</span></span>

### <span data-ttu-id="c22e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c22e9-113">-AsJob</span></span>
<span data-ttu-id="c22e9-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c22e9-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c22e9-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="c22e9-116">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="c22e9-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22e9-117">-DefaultProfile</span></span>
<span data-ttu-id="c22e9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c22e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="c22e9-119">-FromTime</span></span>
<span data-ttu-id="c22e9-120">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="c22e9-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="c22e9-121">-GroupByOperationName</span></span>
<span data-ttu-id="c22e9-122">Результат запроса группировки по имени операции.</span><span class="sxs-lookup"><span data-stu-id="c22e9-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="c22e9-123">-GroupByResourceName</span></span>
<span data-ttu-id="c22e9-124">Результат запроса Group по названию ресурса.</span><span class="sxs-lookup"><span data-stu-id="c22e9-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="c22e9-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="c22e9-126">Результаты запроса на группировку по политике регулирования.</span><span class="sxs-lookup"><span data-stu-id="c22e9-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-127">-Location</span><span class="sxs-lookup"><span data-stu-id="c22e9-127">-Location</span></span>
<span data-ttu-id="c22e9-128">Место, на которое запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="c22e9-128">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-129">-ToTime</span><span class="sxs-lookup"><span data-stu-id="c22e9-129">-ToTime</span></span>
<span data-ttu-id="c22e9-130">Время запроса</span><span class="sxs-lookup"><span data-stu-id="c22e9-130">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c22e9-131">-Confirm</span></span>
<span data-ttu-id="c22e9-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c22e9-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c22e9-133">-WhatIf</span></span>
<span data-ttu-id="c22e9-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c22e9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c22e9-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c22e9-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c22e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22e9-136">CommonParameters</span></span>
<span data-ttu-id="c22e9-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c22e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22e9-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22e9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22e9-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c22e9-139">INPUTS</span></span>

### <span data-ttu-id="c22e9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c22e9-140">System.String</span></span>

## <span data-ttu-id="c22e9-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c22e9-141">OUTPUTS</span></span>

### <span data-ttu-id="c22e9-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="c22e9-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="c22e9-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c22e9-143">NOTES</span></span>

## <span data-ttu-id="c22e9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c22e9-144">RELATED LINKS</span></span>

