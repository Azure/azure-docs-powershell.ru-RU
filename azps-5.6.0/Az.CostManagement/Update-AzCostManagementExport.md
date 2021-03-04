---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: d4be10cf33952b026ceabe6cd407929acbe5c058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952744"
---
# <span data-ttu-id="acfd2-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="acfd2-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="acfd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acfd2-102">SYNOPSIS</span></span>
<span data-ttu-id="acfd2-103">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-103">The operation to create or update a export.</span></span>
<span data-ttu-id="acfd2-104">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="acfd2-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="acfd2-105">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="acfd2-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="acfd2-106">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="acfd2-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="acfd2-107">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acfd2-107">SYNTAX</span></span>

### <span data-ttu-id="acfd2-108">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acfd2-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="acfd2-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="acfd2-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="acfd2-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acfd2-110">DESCRIPTION</span></span>
<span data-ttu-id="acfd2-111">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-111">The operation to create or update a export.</span></span>
<span data-ttu-id="acfd2-112">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="acfd2-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="acfd2-113">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="acfd2-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="acfd2-114">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="acfd2-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="acfd2-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acfd2-115">EXAMPLES</span></span>

### <span data-ttu-id="acfd2-116">Пример 1. Обновление AzCostManagementExport по области и имени</span><span class="sxs-lookup"><span data-stu-id="acfd2-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="acfd2-117">Обновление AzCostManagementExport по области и имени</span><span class="sxs-lookup"><span data-stu-id="acfd2-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="acfd2-118">Пример 2. Обновление AzCostManagementExport с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="acfd2-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="acfd2-119">Обновление AzCostManagementExport с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="acfd2-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="acfd2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acfd2-120">PARAMETERS</span></span>

### <span data-ttu-id="acfd2-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="acfd2-121">-ConfigurationColumn</span></span>
<span data-ttu-id="acfd2-122">Массив имен столбцов, которые нужно включить в экспорт.</span><span class="sxs-lookup"><span data-stu-id="acfd2-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="acfd2-123">Если он не предоставлен, экспорт будет включать все доступные столбцы.</span><span class="sxs-lookup"><span data-stu-id="acfd2-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="acfd2-124">Доступные столбцы зависят от канала клиента (см. примеры).</span><span class="sxs-lookup"><span data-stu-id="acfd2-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="acfd2-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="acfd2-125">-DataSetGranularity</span></span>
<span data-ttu-id="acfd2-126">Детализация строк в экспорте.</span><span class="sxs-lookup"><span data-stu-id="acfd2-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="acfd2-127">В настоящее время поддерживается только "Ежедневно".</span><span class="sxs-lookup"><span data-stu-id="acfd2-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="acfd2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acfd2-128">-DefaultProfile</span></span>
<span data-ttu-id="acfd2-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acfd2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acfd2-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="acfd2-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="acfd2-131">Период времени для сбора данных для экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="acfd2-132">Если он настраиваемый, необходимо ука-заметь конкретный период времени.</span><span class="sxs-lookup"><span data-stu-id="acfd2-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="acfd2-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="acfd2-133">-DefinitionType</span></span>
<span data-ttu-id="acfd2-134">Тип экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-134">The type of the export.</span></span>
<span data-ttu-id="acfd2-135">Обратите внимание, что "Использование" эквивалентно actualCost и применимо к экспорту, в который еще не взимается плата или амортизация данных для резервирования служб.</span><span class="sxs-lookup"><span data-stu-id="acfd2-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="acfd2-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="acfd2-136">-DestinationContainer</span></span>
<span data-ttu-id="acfd2-137">Имя контейнера, в который будут экспортироваться экспорты.</span><span class="sxs-lookup"><span data-stu-id="acfd2-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="acfd2-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="acfd2-138">-DestinationResourceId</span></span>
<span data-ttu-id="acfd2-139">ИД ресурса учетной записи хранения, в который будут доставлены экспорты.</span><span class="sxs-lookup"><span data-stu-id="acfd2-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="acfd2-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="acfd2-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="acfd2-141">Имя каталога, в который будут экспортироваться экспорты.</span><span class="sxs-lookup"><span data-stu-id="acfd2-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="acfd2-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="acfd2-142">-ETag</span></span>
<span data-ttu-id="acfd2-143">eTag ресурса.</span><span class="sxs-lookup"><span data-stu-id="acfd2-143">eTag of the resource.</span></span>
<span data-ttu-id="acfd2-144">Для обработки сценария одновременного обновления это поле будет использоваться для определения того, обновляет ли пользователь последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="acfd2-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="acfd2-145">-Format</span><span class="sxs-lookup"><span data-stu-id="acfd2-145">-Format</span></span>
<span data-ttu-id="acfd2-146">Формат доставки.</span><span class="sxs-lookup"><span data-stu-id="acfd2-146">The format of the export being delivered.</span></span>
<span data-ttu-id="acfd2-147">В настоящее время поддерживается только "CSV".</span><span class="sxs-lookup"><span data-stu-id="acfd2-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="acfd2-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acfd2-148">-InputObject</span></span>
<span data-ttu-id="acfd2-149">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="acfd2-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acfd2-150">-Name</span><span class="sxs-lookup"><span data-stu-id="acfd2-150">-Name</span></span>
<span data-ttu-id="acfd2-151">Имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acfd2-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="acfd2-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="acfd2-153">Дата начала повторения.</span><span class="sxs-lookup"><span data-stu-id="acfd2-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="acfd2-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="acfd2-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="acfd2-155">Дата окончания повторения.</span><span class="sxs-lookup"><span data-stu-id="acfd2-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="acfd2-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="acfd2-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="acfd2-157">Повторение расписания.</span><span class="sxs-lookup"><span data-stu-id="acfd2-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="acfd2-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="acfd2-158">-ScheduleStatus</span></span>
<span data-ttu-id="acfd2-159">Состояние расписания экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-159">The status of the export's schedule.</span></span>
<span data-ttu-id="acfd2-160">Если неактивна, расписание экспорта приостанавлилось.</span><span class="sxs-lookup"><span data-stu-id="acfd2-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="acfd2-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="acfd2-161">-Scope</span></span>
<span data-ttu-id="acfd2-162">Этот параметр определяет область затрат по стоимости с различных точек зрения : "Подписка", "Группа ресурсов" и "Предоставление службы".</span><span class="sxs-lookup"><span data-stu-id="acfd2-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acfd2-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="acfd2-163">-TimePeriodFrom</span></span>
<span data-ttu-id="acfd2-164">Дата начала экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="acfd2-164">The start date for export data.</span></span>

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

### <span data-ttu-id="acfd2-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="acfd2-165">-TimePeriodTo</span></span>
<span data-ttu-id="acfd2-166">Даты окончания экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="acfd2-166">The end date for export data.</span></span>

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

### <span data-ttu-id="acfd2-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acfd2-167">-Confirm</span></span>
<span data-ttu-id="acfd2-168">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="acfd2-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acfd2-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acfd2-169">-WhatIf</span></span>
<span data-ttu-id="acfd2-170">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acfd2-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acfd2-171">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="acfd2-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acfd2-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acfd2-172">CommonParameters</span></span>
<span data-ttu-id="acfd2-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acfd2-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acfd2-174">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acfd2-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acfd2-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acfd2-175">INPUTS</span></span>

### <span data-ttu-id="acfd2-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="acfd2-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="acfd2-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acfd2-177">OUTPUTS</span></span>

### <span data-ttu-id="acfd2-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="acfd2-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="acfd2-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acfd2-179">NOTES</span></span>

<span data-ttu-id="acfd2-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="acfd2-180">ALIASES</span></span>

<span data-ttu-id="acfd2-181">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="acfd2-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="acfd2-182">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="acfd2-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="acfd2-183">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="acfd2-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="acfd2-184">INPUTOBJECT <ICostManagementIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="acfd2-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="acfd2-185">`[AlertId <String>]`: ИД оповещения</span><span class="sxs-lookup"><span data-stu-id="acfd2-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="acfd2-186">`[ExportName <String>]`: имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="acfd2-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="acfd2-187">`[ExternalCloudProviderId <String>]`: "{externalSubscriptionId}" для связанной учетной записи или "{externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="acfd2-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="acfd2-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`Внешний поставщик облачных услуг, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="acfd2-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="acfd2-189">К ним относятся 'externalSubscriptions' для связанных учетных записей и externalBillingAccounts для консолидированной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="acfd2-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="acfd2-190">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="acfd2-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="acfd2-191">`[Scope <String>]`: область, связанная с действиями представления.</span><span class="sxs-lookup"><span data-stu-id="acfd2-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="acfd2-192">К ним относятся подписки/{subscriptionId}" для области подписки, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" для области resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" для области учетной записи вы выставления счетов, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" для области EnrollmentAccountunt, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' для области InvoiceSection, "providers/Microsoft.Management/managementGroups/{managementGroupId}" for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" для внешней подписки.</span><span class="sxs-lookup"><span data-stu-id="acfd2-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="acfd2-193">`[ViewName <String>]`: имя представления</span><span class="sxs-lookup"><span data-stu-id="acfd2-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="acfd2-194">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acfd2-194">RELATED LINKS</span></span>

