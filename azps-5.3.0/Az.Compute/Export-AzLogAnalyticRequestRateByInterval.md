---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 90b467ccd046bf7d08b9faff4c03dcc858ae0076
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519645"
---
# <span data-ttu-id="7cf96-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="7cf96-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="7cf96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cf96-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf96-103">Экспортировать журналы, в которые в заданное время будут экспортироваться запросы API, сделанные этой подпиской, для демонстрации действий регулирования.</span><span class="sxs-lookup"><span data-stu-id="7cf96-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="7cf96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7cf96-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf96-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf96-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf96-106">Экспорт статистических данных о вызовах подписки в API Microsoft.Compute с учетом успешности, сбоя или состояния регулирования заранее определенные интервалы времени.</span><span class="sxs-lookup"><span data-stu-id="7cf96-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="7cf96-107">Журналы можно дополнительно сгруппировать по трем параметрам: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="7cf96-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="7cf96-108">Обратите внимание, что этот cmdlet собирает только журналы поставщиков ресурсов Compute; кроме того, данные о типах ресурсов "Диск" и "Моментальный снимок" пока недоступны.</span><span class="sxs-lookup"><span data-stu-id="7cf96-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="7cf96-109">Обзор регулирования API поставщика ресурсов для компьютеров см. в этой https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits теме.</span><span class="sxs-lookup"><span data-stu-id="7cf96-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="7cf96-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7cf96-110">EXAMPLES</span></span>

### <span data-ttu-id="7cf96-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7cf96-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="7cf96-112">Эта команда хранит агрегированные номера звонков API Microsoft.Compute, разделенные на успех, сбой или регулирование между 2018-02-20T17:54:14 and 2018-02-22T17:54:17 в URI SAS, агрегированном по имени операции.</span><span class="sxs-lookup"><span data-stu-id="7cf96-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="7cf96-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cf96-113">PARAMETERS</span></span>

### <span data-ttu-id="7cf96-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cf96-114">-AsJob</span></span>
<span data-ttu-id="7cf96-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7cf96-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7cf96-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="7cf96-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="7cf96-117">SAS Uri контейнера BLOB-приложений, в который LogAnalytics Api записывает журналы вывода.</span><span class="sxs-lookup"><span data-stu-id="7cf96-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="7cf96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cf96-118">-DefaultProfile</span></span>
<span data-ttu-id="7cf96-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cf96-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="7cf96-120">-FromTime</span></span>
<span data-ttu-id="7cf96-121">Со времени запроса</span><span class="sxs-lookup"><span data-stu-id="7cf96-121">From time of the query</span></span>

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

### <span data-ttu-id="7cf96-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="7cf96-122">-GroupByOperationName</span></span>
<span data-ttu-id="7cf96-123">Результат запроса группы по имени операции.</span><span class="sxs-lookup"><span data-stu-id="7cf96-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="7cf96-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="7cf96-124">-GroupByResourceName</span></span>
<span data-ttu-id="7cf96-125">Результат запроса группы по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="7cf96-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="7cf96-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="7cf96-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="7cf96-127">Результат группового запроса с примененной политикой Throttle.</span><span class="sxs-lookup"><span data-stu-id="7cf96-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="7cf96-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="7cf96-128">-IntervalLength</span></span>
<span data-ttu-id="7cf96-129">Значение интервала в минутах, используемом для создания журналов вызовов LogAnalytics.</span><span class="sxs-lookup"><span data-stu-id="7cf96-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="7cf96-130">-Location</span><span class="sxs-lookup"><span data-stu-id="7cf96-130">-Location</span></span>
<span data-ttu-id="7cf96-131">Расположение, для которого запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="7cf96-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="7cf96-132">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7cf96-132">-NoWait</span></span>
<span data-ttu-id="7cf96-133">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="7cf96-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7cf96-134">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="7cf96-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7cf96-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="7cf96-135">-ToTime</span></span>
<span data-ttu-id="7cf96-136">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="7cf96-136">To time of the query</span></span>

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

### <span data-ttu-id="7cf96-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf96-137">-Confirm</span></span>
<span data-ttu-id="7cf96-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7cf96-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf96-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf96-139">-WhatIf</span></span>
<span data-ttu-id="7cf96-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cf96-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cf96-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7cf96-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf96-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf96-142">CommonParameters</span></span>
<span data-ttu-id="7cf96-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cf96-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf96-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cf96-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf96-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf96-145">INPUTS</span></span>

### <span data-ttu-id="7cf96-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7cf96-146">System.String</span></span>

## <span data-ttu-id="7cf96-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7cf96-147">OUTPUTS</span></span>

### <span data-ttu-id="7cf96-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="7cf96-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="7cf96-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7cf96-149">NOTES</span></span>

## <span data-ttu-id="7cf96-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cf96-150">RELATED LINKS</span></span>
