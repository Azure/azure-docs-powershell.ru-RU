---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249202"
---
# <span data-ttu-id="5ce9a-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5ce9a-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="5ce9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ce9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce9a-103">Экспорт журналов, показывающих общее число запросов API для подписки в заданном окне времени.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="5ce9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ce9a-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce9a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ce9a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ce9a-106">Это экспортирует общее количество запросов API Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="5ce9a-107">Журналы можно дополнительно объединять тремя вариантами: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="5ce9a-108">Обратите внимание, что этот командлет собирает только CRP журналы.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="5ce9a-109">Общие сведения о регулировании API поставщика ресурсов вычислительной среды содержатся в разделе https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="5ce9a-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="5ce9a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ce9a-110">EXAMPLES</span></span>

### <span data-ttu-id="5ce9a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ce9a-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="5ce9a-112">Эта команда хранит общее число вызовов API Microsoft. COMPUTE между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в заданном URI SAS, агрегированные по названию операции.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="5ce9a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ce9a-113">PARAMETERS</span></span>

### <span data-ttu-id="5ce9a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ce9a-114">-AsJob</span></span>
<span data-ttu-id="5ce9a-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ce9a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ce9a-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="5ce9a-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="5ce9a-117">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="5ce9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce9a-118">-DefaultProfile</span></span>
<span data-ttu-id="5ce9a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce9a-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="5ce9a-120">-FromTime</span></span>
<span data-ttu-id="5ce9a-121">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="5ce9a-121">From time of the query</span></span>

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

### <span data-ttu-id="5ce9a-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="5ce9a-122">-GroupByOperationName</span></span>
<span data-ttu-id="5ce9a-123">Результат запроса группировки по имени операции.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="5ce9a-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="5ce9a-124">-GroupByResourceName</span></span>
<span data-ttu-id="5ce9a-125">Результат запроса Group по названию ресурса.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="5ce9a-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="5ce9a-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="5ce9a-127">Результаты запроса на группировку по политике регулирования.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="5ce9a-128">-Location</span><span class="sxs-lookup"><span data-stu-id="5ce9a-128">-Location</span></span>
<span data-ttu-id="5ce9a-129">Место, на которое запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="5ce9a-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="5ce9a-130">-NoWait</span></span>
<span data-ttu-id="5ce9a-131">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5ce9a-132">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5ce9a-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="5ce9a-133">-ToTime</span></span>
<span data-ttu-id="5ce9a-134">Время запроса</span><span class="sxs-lookup"><span data-stu-id="5ce9a-134">To time of the query</span></span>

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

### <span data-ttu-id="5ce9a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ce9a-135">-Confirm</span></span>
<span data-ttu-id="5ce9a-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce9a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce9a-137">-WhatIf</span></span>
<span data-ttu-id="5ce9a-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce9a-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce9a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce9a-140">CommonParameters</span></span>
<span data-ttu-id="5ce9a-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ce9a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce9a-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ce9a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce9a-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ce9a-143">INPUTS</span></span>

### <span data-ttu-id="5ce9a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5ce9a-144">System.String</span></span>

## <span data-ttu-id="5ce9a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ce9a-145">OUTPUTS</span></span>

### <span data-ttu-id="5ce9a-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="5ce9a-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="5ce9a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ce9a-147">NOTES</span></span>

## <span data-ttu-id="5ce9a-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ce9a-148">RELATED LINKS</span></span>
