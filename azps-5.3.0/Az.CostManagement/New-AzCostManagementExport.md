---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519150"
---
# <span data-ttu-id="bd7d6-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="bd7d6-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="bd7d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7d6-103">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-103">The operation to create or update a export.</span></span>
<span data-ttu-id="bd7d6-104">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="bd7d6-105">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="bd7d6-106">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="bd7d6-107">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd7d6-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd7d6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd7d6-108">DESCRIPTION</span></span>
<span data-ttu-id="bd7d6-109">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-109">The operation to create or update a export.</span></span>
<span data-ttu-id="bd7d6-110">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="bd7d6-111">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="bd7d6-112">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="bd7d6-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd7d6-113">EXAMPLES</span></span>

### <span data-ttu-id="bd7d6-114">Пример 1. Создание azCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="bd7d6-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="bd7d6-115">Создание azCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="bd7d6-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="bd7d6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd7d6-116">PARAMETERS</span></span>

### <span data-ttu-id="bd7d6-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="bd7d6-117">-ConfigurationColumn</span></span>
<span data-ttu-id="bd7d6-118">Массив имен столбцов, которые нужно включить в экспорт.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="bd7d6-119">Если он не предоставлен, экспорт будет включать все доступные столбцы.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="bd7d6-120">Доступные столбцы зависят от канала клиента (см. примеры).</span><span class="sxs-lookup"><span data-stu-id="bd7d6-120">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="bd7d6-121">-DataSetGranularity</span></span>
<span data-ttu-id="bd7d6-122">Детализация строк в экспорте.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="bd7d6-123">В настоящее время поддерживается только "Ежедневно".</span><span class="sxs-lookup"><span data-stu-id="bd7d6-123">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7d6-124">-DefaultProfile</span></span>
<span data-ttu-id="bd7d6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="bd7d6-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="bd7d6-127">Период времени для сбора данных для экспорта.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="bd7d6-128">Если он настраиваемый, необходимо ука-заметь конкретный период времени.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-128">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="bd7d6-129">-DefinitionType</span></span>
<span data-ttu-id="bd7d6-130">Тип экспорта.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-130">The type of the export.</span></span>
<span data-ttu-id="bd7d6-131">Обратите внимание, что "Использование" эквивалентно actualCost и применимо к экспортам, которые пока не предоставляют данные для сплаты или амортизации для резервирования служб.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="bd7d6-132">-DestinationContainer</span></span>
<span data-ttu-id="bd7d6-133">Имя контейнера, в который будут экспортироваться экспорты.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-133">The name of the container where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="bd7d6-134">-DestinationResourceId</span></span>
<span data-ttu-id="bd7d6-135">ИД ресурса учетной записи хранения, в который будут доставлены экспорты.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-135">The resource id of the storage account where exports will be delivered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="bd7d6-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="bd7d6-137">Имя каталога, в который будут экспортироваться экспорты.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-137">The name of the directory where exports will be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-138">-Format</span><span class="sxs-lookup"><span data-stu-id="bd7d6-138">-Format</span></span>
<span data-ttu-id="bd7d6-139">Формат доставки.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-139">The format of the export being delivered.</span></span>
<span data-ttu-id="bd7d6-140">В настоящее время поддерживается только "CSV".</span><span class="sxs-lookup"><span data-stu-id="bd7d6-140">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-141">-Name</span><span class="sxs-lookup"><span data-stu-id="bd7d6-141">-Name</span></span>
<span data-ttu-id="bd7d6-142">Имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="bd7d6-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="bd7d6-144">Дата начала повторения.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-144">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="bd7d6-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="bd7d6-146">Дата окончания повторения.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-146">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="bd7d6-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="bd7d6-148">Повторение расписания.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-148">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="bd7d6-149">-ScheduleStatus</span></span>
<span data-ttu-id="bd7d6-150">Состояние расписания экспорта.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-150">The status of the export's schedule.</span></span>
<span data-ttu-id="bd7d6-151">Если "Неактивна", расписание экспорта приостанавлилось.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-151">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="bd7d6-152">-Scope</span></span>
<span data-ttu-id="bd7d6-153">Этот параметр определяет область затрат по стоимости с различных точек зрения : "Подписка", "Группа ресурсов" и "Предоставление службы".</span><span class="sxs-lookup"><span data-stu-id="bd7d6-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="bd7d6-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="bd7d6-154">-TimePeriodFrom</span></span>
<span data-ttu-id="bd7d6-155">Дата начала экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-155">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="bd7d6-156">-TimePeriodTo</span></span>
<span data-ttu-id="bd7d6-157">Даты окончания экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-157">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7d6-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd7d6-158">-Confirm</span></span>
<span data-ttu-id="bd7d6-159">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd7d6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd7d6-160">-WhatIf</span></span>
<span data-ttu-id="bd7d6-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd7d6-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd7d6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7d6-163">CommonParameters</span></span>
<span data-ttu-id="bd7d6-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7d6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7d6-165">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd7d6-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7d6-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd7d6-166">INPUTS</span></span>

## <span data-ttu-id="bd7d6-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd7d6-167">OUTPUTS</span></span>

### <span data-ttu-id="bd7d6-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="bd7d6-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="bd7d6-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd7d6-169">NOTES</span></span>

<span data-ttu-id="bd7d6-170">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bd7d6-170">ALIASES</span></span>

## <span data-ttu-id="bd7d6-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd7d6-171">RELATED LINKS</span></span>

