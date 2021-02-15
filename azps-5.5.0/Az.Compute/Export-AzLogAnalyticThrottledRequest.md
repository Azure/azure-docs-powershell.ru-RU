---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 97f921fab8e258d5fbde44a6c148f61da2730999
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238926"
---
# <span data-ttu-id="d3ffa-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d3ffa-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="d3ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ffa-103">Журналы экспорта, в которые в заданное время будут экспортироваться общие запросы API с регулированием для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="d3ffa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3ffa-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3ffa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3ffa-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ffa-106">При этом экспортируется общее количество звонков API, к которые имеет регулирование Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="d3ffa-107">Журналы можно дополнительно агрегировать с помощью трех параметров: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="d3ffa-108">Обратите внимание, что этот cmdlet собирает только журналы CRP.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="d3ffa-109">Обзор регулирования API поставщика ресурсов для компьютеров см. в этой https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits теме.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="d3ffa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3ffa-110">EXAMPLES</span></span>

### <span data-ttu-id="d3ffa-111">Пример 1. Экспорт записей, агрегированных по имени операции</span><span class="sxs-lookup"><span data-stu-id="d3ffa-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="d3ffa-112">Эта команда хранит итоговые звонки API Microsoft.Compute между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, агрегированном по имени операции.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="d3ffa-113">Пример 2. Экспорт записей, агрегированных по id приложения</span><span class="sxs-lookup"><span data-stu-id="d3ffa-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="d3ffa-114">Эта команда хранит итоговые звонки API Microsoft.Compute между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, обобщенном по id appliction.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="d3ffa-115">Пример 3. Экспорт записей, агрегированных агентом пользователя</span><span class="sxs-lookup"><span data-stu-id="d3ffa-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="d3ffa-116">Эта команда хранит итоговые звонки API Microsoft.Compute между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, обобщенном агентом пользователя.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="d3ffa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3ffa-117">PARAMETERS</span></span>

### <span data-ttu-id="d3ffa-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3ffa-118">-AsJob</span></span>
<span data-ttu-id="d3ffa-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d3ffa-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3ffa-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="d3ffa-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="d3ffa-121">SAS Uri контейнера BLOB-приложений, в который LogAnalytics Api записывает журналы вывода.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="d3ffa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ffa-122">-DefaultProfile</span></span>
<span data-ttu-id="d3ffa-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3ffa-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="d3ffa-124">-FromTime</span></span>
<span data-ttu-id="d3ffa-125">Со времени запроса</span><span class="sxs-lookup"><span data-stu-id="d3ffa-125">From time of the query</span></span>

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

### <span data-ttu-id="d3ffa-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="d3ffa-126">-GroupByApplicationId</span></span>
<span data-ttu-id="d3ffa-127">Результат группового запроса по ИД приложения.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="d3ffa-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="d3ffa-128">-GroupByOperationName</span></span>
<span data-ttu-id="d3ffa-129">Результат запроса группы по имени операции.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="d3ffa-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="d3ffa-130">-GroupByResourceName</span></span>
<span data-ttu-id="d3ffa-131">Результат запроса группы по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="d3ffa-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="d3ffa-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="d3ffa-133">Результат группового запроса с примененной политикой Throttle.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="d3ffa-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="d3ffa-134">-GroupByUserAgent</span></span>
<span data-ttu-id="d3ffa-135">Результат запроса группы по userAgent.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="d3ffa-136">-Location</span><span class="sxs-lookup"><span data-stu-id="d3ffa-136">-Location</span></span>
<span data-ttu-id="d3ffa-137">Расположение, для которого запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="d3ffa-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d3ffa-138">-NoWait</span></span>
<span data-ttu-id="d3ffa-139">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d3ffa-140">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d3ffa-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="d3ffa-141">-ToTime</span></span>
<span data-ttu-id="d3ffa-142">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="d3ffa-142">To time of the query</span></span>

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

### <span data-ttu-id="d3ffa-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3ffa-143">-Confirm</span></span>
<span data-ttu-id="d3ffa-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ffa-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ffa-145">-WhatIf</span></span>
<span data-ttu-id="d3ffa-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3ffa-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ffa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ffa-148">CommonParameters</span></span>
<span data-ttu-id="d3ffa-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ffa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ffa-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3ffa-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ffa-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3ffa-151">INPUTS</span></span>

### <span data-ttu-id="d3ffa-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d3ffa-152">System.String</span></span>

## <span data-ttu-id="d3ffa-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3ffa-153">OUTPUTS</span></span>

### <span data-ttu-id="d3ffa-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="d3ffa-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="d3ffa-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3ffa-155">NOTES</span></span>

## <span data-ttu-id="d3ffa-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3ffa-156">RELATED LINKS</span></span>
