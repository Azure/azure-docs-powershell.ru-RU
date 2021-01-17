---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391212"
---
# <span data-ttu-id="92441-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="92441-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="92441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92441-102">SYNOPSIS</span></span>
<span data-ttu-id="92441-103">Экспортировать журналы, в которые в заданное время будут экспортироваться общие запросы API с регулированием для этой подписки.</span><span class="sxs-lookup"><span data-stu-id="92441-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="92441-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92441-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92441-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92441-105">DESCRIPTION</span></span>
<span data-ttu-id="92441-106">При этом экспортируется общее количество звонков API, к которые имеет регулирование Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="92441-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="92441-107">Журналы можно дополнительно агрегировать с помощью трех параметров: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="92441-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="92441-108">Обратите внимание, что этот cmdlet собирает только журналы CRP.</span><span class="sxs-lookup"><span data-stu-id="92441-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="92441-109">Обзор регулирования API поставщика ресурсов для компьютеров см. в . https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits</span><span class="sxs-lookup"><span data-stu-id="92441-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="92441-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92441-110">EXAMPLES</span></span>

### <span data-ttu-id="92441-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92441-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="92441-112">Эта команда хранит общее регулирование вызовов API Microsoft.Compute между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в URI SAS, агрегированном по имени операции.</span><span class="sxs-lookup"><span data-stu-id="92441-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="92441-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92441-113">PARAMETERS</span></span>

### <span data-ttu-id="92441-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92441-114">-AsJob</span></span>
<span data-ttu-id="92441-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="92441-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92441-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="92441-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="92441-117">SAS Uri контейнера BLOB-приложений, в который LogAnalytics Api записывает журналы вывода.</span><span class="sxs-lookup"><span data-stu-id="92441-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="92441-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92441-118">-DefaultProfile</span></span>
<span data-ttu-id="92441-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92441-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92441-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="92441-120">-FromTime</span></span>
<span data-ttu-id="92441-121">Со времени запроса</span><span class="sxs-lookup"><span data-stu-id="92441-121">From time of the query</span></span>

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

### <span data-ttu-id="92441-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="92441-122">-GroupByOperationName</span></span>
<span data-ttu-id="92441-123">Результат запроса группы по имени операции.</span><span class="sxs-lookup"><span data-stu-id="92441-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="92441-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="92441-124">-GroupByResourceName</span></span>
<span data-ttu-id="92441-125">Результат запроса группы по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="92441-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="92441-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="92441-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="92441-127">Результат группового запроса с примененной политикой Throttle.</span><span class="sxs-lookup"><span data-stu-id="92441-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="92441-128">-Location</span><span class="sxs-lookup"><span data-stu-id="92441-128">-Location</span></span>
<span data-ttu-id="92441-129">Расположение, для которого запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="92441-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="92441-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92441-130">-NoWait</span></span>
<span data-ttu-id="92441-131">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="92441-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="92441-132">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="92441-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="92441-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="92441-133">-ToTime</span></span>
<span data-ttu-id="92441-134">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="92441-134">To time of the query</span></span>

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

### <span data-ttu-id="92441-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92441-135">-Confirm</span></span>
<span data-ttu-id="92441-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92441-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92441-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92441-137">-WhatIf</span></span>
<span data-ttu-id="92441-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92441-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92441-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92441-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92441-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92441-140">CommonParameters</span></span>
<span data-ttu-id="92441-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92441-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92441-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92441-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92441-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92441-143">INPUTS</span></span>

### <span data-ttu-id="92441-144">System.String</span><span class="sxs-lookup"><span data-stu-id="92441-144">System.String</span></span>

## <span data-ttu-id="92441-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92441-145">OUTPUTS</span></span>

### <span data-ttu-id="92441-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="92441-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="92441-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92441-147">NOTES</span></span>

## <span data-ttu-id="92441-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92441-148">RELATED LINKS</span></span>
