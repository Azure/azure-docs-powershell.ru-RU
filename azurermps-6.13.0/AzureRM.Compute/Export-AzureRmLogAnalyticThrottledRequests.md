---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561104"
---
# <span data-ttu-id="22037-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="22037-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="22037-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22037-102">SYNOPSIS</span></span>
<span data-ttu-id="22037-103">Экспорт журналов, показывающих общее число запросов API для подписки в заданном окне времени.</span><span class="sxs-lookup"><span data-stu-id="22037-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22037-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22037-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22037-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22037-105">DESCRIPTION</span></span>
<span data-ttu-id="22037-106">Это экспортирует общее количество запросов API Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="22037-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="22037-107">Журналы можно дополнительно объединять тремя вариантами: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="22037-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="22037-108">Обратите внимание, что этот командлет собирает только CRP журналы.</span><span class="sxs-lookup"><span data-stu-id="22037-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="22037-109">Общие сведения о регулировании API поставщика ресурсов вычислительной среды содержатся в разделе https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="22037-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="22037-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22037-110">EXAMPLES</span></span>

### <span data-ttu-id="22037-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22037-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="22037-112">Эта команда хранит общее число вызовов API Microsoft. COMPUTE между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в заданном URI SAS, агрегированные по названию операции.</span><span class="sxs-lookup"><span data-stu-id="22037-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="22037-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22037-113">PARAMETERS</span></span>

### <span data-ttu-id="22037-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22037-114">-AsJob</span></span>
<span data-ttu-id="22037-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="22037-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22037-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="22037-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="22037-117">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="22037-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22037-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22037-118">-DefaultProfile</span></span>
<span data-ttu-id="22037-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22037-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22037-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="22037-120">-FromTime</span></span>
<span data-ttu-id="22037-121">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="22037-121">From time of the query</span></span>

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

### <span data-ttu-id="22037-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="22037-122">-GroupByOperationName</span></span>
<span data-ttu-id="22037-123">Результат запроса группировки по имени операции.</span><span class="sxs-lookup"><span data-stu-id="22037-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="22037-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="22037-124">-GroupByResourceName</span></span>
<span data-ttu-id="22037-125">Результат запроса Group по названию ресурса.</span><span class="sxs-lookup"><span data-stu-id="22037-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="22037-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="22037-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="22037-127">Результаты запроса на группировку по политике регулирования.</span><span class="sxs-lookup"><span data-stu-id="22037-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="22037-128">-Location</span><span class="sxs-lookup"><span data-stu-id="22037-128">-Location</span></span>
<span data-ttu-id="22037-129">Место, на которое запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="22037-129">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22037-130">-ToTime</span><span class="sxs-lookup"><span data-stu-id="22037-130">-ToTime</span></span>
<span data-ttu-id="22037-131">Время запроса</span><span class="sxs-lookup"><span data-stu-id="22037-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22037-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22037-132">-Confirm</span></span>
<span data-ttu-id="22037-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22037-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22037-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22037-134">-WhatIf</span></span>
<span data-ttu-id="22037-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22037-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22037-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22037-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22037-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22037-137">CommonParameters</span></span>
<span data-ttu-id="22037-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22037-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22037-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22037-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22037-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22037-140">INPUTS</span></span>

### <span data-ttu-id="22037-141">System. String</span><span class="sxs-lookup"><span data-stu-id="22037-141">System.String</span></span>

## <span data-ttu-id="22037-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22037-142">OUTPUTS</span></span>

### <span data-ttu-id="22037-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="22037-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="22037-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="22037-144">NOTES</span></span>

## <span data-ttu-id="22037-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22037-145">RELATED LINKS</span></span>
