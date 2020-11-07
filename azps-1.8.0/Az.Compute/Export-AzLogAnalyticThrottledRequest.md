---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 65a2dd49b0beee557f062201f27a7235c28d5283
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901365"
---
# <span data-ttu-id="228ee-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="228ee-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="228ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="228ee-102">SYNOPSIS</span></span>
<span data-ttu-id="228ee-103">Экспорт журналов, показывающих общее число запросов API для подписки в заданном окне времени.</span><span class="sxs-lookup"><span data-stu-id="228ee-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="228ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="228ee-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="228ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="228ee-105">DESCRIPTION</span></span>
<span data-ttu-id="228ee-106">Это экспортирует общее количество запросов API Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="228ee-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="228ee-107">Журналы можно дополнительно объединять тремя вариантами: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="228ee-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="228ee-108">Обратите внимание, что этот командлет собирает только CRP журналы.</span><span class="sxs-lookup"><span data-stu-id="228ee-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="228ee-109">Общие сведения о регулировании API поставщика ресурсов вычислительной среды содержатся в разделе https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="228ee-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="228ee-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="228ee-110">EXAMPLES</span></span>

### <span data-ttu-id="228ee-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="228ee-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="228ee-112">Эта команда хранит общее число вызовов API Microsoft. COMPUTE между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в заданном URI SAS, агрегированные по названию операции.</span><span class="sxs-lookup"><span data-stu-id="228ee-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="228ee-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="228ee-113">PARAMETERS</span></span>

### <span data-ttu-id="228ee-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="228ee-114">-AsJob</span></span>
<span data-ttu-id="228ee-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="228ee-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="228ee-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="228ee-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="228ee-117">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="228ee-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228ee-118">-DefaultProfile</span></span>
<span data-ttu-id="228ee-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="228ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="228ee-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="228ee-120">-FromTime</span></span>
<span data-ttu-id="228ee-121">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="228ee-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228ee-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="228ee-122">-GroupByOperationName</span></span>
<span data-ttu-id="228ee-123">Результат запроса группировки по имени операции.</span><span class="sxs-lookup"><span data-stu-id="228ee-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="228ee-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="228ee-124">-GroupByResourceName</span></span>
<span data-ttu-id="228ee-125">Результат запроса Group по названию ресурса.</span><span class="sxs-lookup"><span data-stu-id="228ee-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="228ee-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="228ee-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="228ee-127">Результаты запроса на группировку по политике регулирования.</span><span class="sxs-lookup"><span data-stu-id="228ee-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="228ee-128">-Location</span><span class="sxs-lookup"><span data-stu-id="228ee-128">-Location</span></span>
<span data-ttu-id="228ee-129">Место, на которое запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="228ee-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="228ee-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="228ee-130">-ToTime</span></span>
<span data-ttu-id="228ee-131">Время запроса</span><span class="sxs-lookup"><span data-stu-id="228ee-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228ee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="228ee-132">-Confirm</span></span>
<span data-ttu-id="228ee-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="228ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="228ee-134">-WhatIf</span></span>
<span data-ttu-id="228ee-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="228ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="228ee-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="228ee-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228ee-137">CommonParameters</span></span>
<span data-ttu-id="228ee-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="228ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228ee-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="228ee-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228ee-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="228ee-140">INPUTS</span></span>

### <span data-ttu-id="228ee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="228ee-141">System.String</span></span>

## <span data-ttu-id="228ee-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="228ee-142">OUTPUTS</span></span>

### <span data-ttu-id="228ee-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="228ee-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="228ee-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="228ee-144">NOTES</span></span>

## <span data-ttu-id="228ee-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="228ee-145">RELATED LINKS</span></span>
