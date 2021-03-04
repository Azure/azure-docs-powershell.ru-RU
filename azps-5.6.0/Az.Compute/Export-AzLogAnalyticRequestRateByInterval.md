---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969411"
---
# <span data-ttu-id="3cf8c-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="3cf8c-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="3cf8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf8c-103">Экспортировать журналы, в которые в заданное время будут экспортироваться запросы API, сделанные этой подпиской, для демонстрации действий регулирования.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="3cf8c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cf8c-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf8c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf8c-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf8c-106">Экспорт статистических данных о вызовах подписки в API Microsoft.Compute с учетом успешности, сбоя или состояния регулирования заранее определенные интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="3cf8c-107">Журналы можно дополнительно сгруппировать по пяти параметрам: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent или GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="3cf8c-108">Обратите внимание, что этот cmdlet собирает только журналы поставщиков ресурсов Compute; кроме того, данные о типах ресурсов "Диск" и "Моментальный снимок" пока недоступны.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="3cf8c-109">Обзор регулирования API поставщика ресурсов для компьютеров см. в . https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits</span><span class="sxs-lookup"><span data-stu-id="3cf8c-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="3cf8c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cf8c-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf8c-111">Пример 1. Экспорт записей, агрегированных по имени операции</span><span class="sxs-lookup"><span data-stu-id="3cf8c-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="3cf8c-112">Эта команда хранит агрегированные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 and 2018-02-22T17:54:17 в URI SAS, агрегированном по имени операции.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="3cf8c-113">Пример 2. Экспорт записей, агрегированных по id приложения</span><span class="sxs-lookup"><span data-stu-id="3cf8c-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="3cf8c-114">Эта команда хранит совокупные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, агрегированном по id приложения.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="3cf8c-115">Пример 3. Экспорт записей, агрегированных агентом пользователя</span><span class="sxs-lookup"><span data-stu-id="3cf8c-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="3cf8c-116">Эта команда хранит агрегированные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, обобщенном агентом пользователя.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="3cf8c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cf8c-117">PARAMETERS</span></span>

### <span data-ttu-id="3cf8c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cf8c-118">-AsJob</span></span>
<span data-ttu-id="3cf8c-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3cf8c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cf8c-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="3cf8c-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="3cf8c-121">SAS Uri контейнера BLOB-приложений, в который LogAnalytics Api записывает журналы вывода.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="3cf8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf8c-122">-DefaultProfile</span></span>
<span data-ttu-id="3cf8c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf8c-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="3cf8c-124">-FromTime</span></span>
<span data-ttu-id="3cf8c-125">Со времени запроса</span><span class="sxs-lookup"><span data-stu-id="3cf8c-125">From time of the query</span></span>

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

### <span data-ttu-id="3cf8c-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="3cf8c-126">-GroupByApplicationId</span></span>
<span data-ttu-id="3cf8c-127">Результат группового запроса по ИД приложения.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="3cf8c-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="3cf8c-128">-GroupByOperationName</span></span>
<span data-ttu-id="3cf8c-129">Результат запроса группы по имени операции.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="3cf8c-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="3cf8c-130">-GroupByResourceName</span></span>
<span data-ttu-id="3cf8c-131">Результат запроса группы по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="3cf8c-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="3cf8c-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="3cf8c-133">Результат группового запроса с примененной политикой Throttle.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="3cf8c-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="3cf8c-134">-GroupByUserAgent</span></span>
<span data-ttu-id="3cf8c-135">Результат запроса группы по userAgent.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="3cf8c-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="3cf8c-136">-IntervalLength</span></span>
<span data-ttu-id="3cf8c-137">Значение интервала в минутах, используемом для создания журналов вызовов LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf8c-138">-Location</span><span class="sxs-lookup"><span data-stu-id="3cf8c-138">-Location</span></span>
<span data-ttu-id="3cf8c-139">Расположение, для которого запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="3cf8c-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3cf8c-140">-NoWait</span></span>
<span data-ttu-id="3cf8c-141">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3cf8c-142">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3cf8c-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="3cf8c-143">-ToTime</span></span>
<span data-ttu-id="3cf8c-144">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="3cf8c-144">To time of the query</span></span>

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

### <span data-ttu-id="3cf8c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cf8c-145">-Confirm</span></span>
<span data-ttu-id="3cf8c-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf8c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf8c-147">-WhatIf</span></span>
<span data-ttu-id="3cf8c-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf8c-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf8c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf8c-150">CommonParameters</span></span>
<span data-ttu-id="3cf8c-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf8c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf8c-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cf8c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf8c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cf8c-153">INPUTS</span></span>

### <span data-ttu-id="3cf8c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="3cf8c-154">System.String</span></span>

## <span data-ttu-id="3cf8c-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cf8c-155">OUTPUTS</span></span>

### <span data-ttu-id="3cf8c-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="3cf8c-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="3cf8c-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cf8c-157">NOTES</span></span>

## <span data-ttu-id="3cf8c-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cf8c-158">RELATED LINKS</span></span>
