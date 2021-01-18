---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519146"
---
# <span data-ttu-id="830f6-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="830f6-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="830f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="830f6-102">SYNOPSIS</span></span>
<span data-ttu-id="830f6-103">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-103">The operation to create or update a export.</span></span>
<span data-ttu-id="830f6-104">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="830f6-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="830f6-105">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="830f6-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="830f6-106">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="830f6-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="830f6-107">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="830f6-107">SYNTAX</span></span>

### <span data-ttu-id="830f6-108">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="830f6-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="830f6-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="830f6-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="830f6-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="830f6-110">DESCRIPTION</span></span>
<span data-ttu-id="830f6-111">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-111">The operation to create or update a export.</span></span>
<span data-ttu-id="830f6-112">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="830f6-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="830f6-113">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="830f6-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="830f6-114">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="830f6-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="830f6-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="830f6-115">EXAMPLES</span></span>

### <span data-ttu-id="830f6-116">Пример 1. Обновление AzCostManagementExport по области и имени</span><span class="sxs-lookup"><span data-stu-id="830f6-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="830f6-117">Обновление AzCostManagementExport по области и имени</span><span class="sxs-lookup"><span data-stu-id="830f6-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="830f6-118">Пример 2. Обновление AzCostManagementExport с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="830f6-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="830f6-119">Обновление AzCostManagementExport с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="830f6-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="830f6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="830f6-120">PARAMETERS</span></span>

### <span data-ttu-id="830f6-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="830f6-121">-ConfigurationColumn</span></span>
<span data-ttu-id="830f6-122">Массив имен столбцов, которые нужно включить в экспорт.</span><span class="sxs-lookup"><span data-stu-id="830f6-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="830f6-123">Если он не предоставлен, экспорт будет включать все доступные столбцы.</span><span class="sxs-lookup"><span data-stu-id="830f6-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="830f6-124">Доступные столбцы зависят от канала клиента (см. примеры).</span><span class="sxs-lookup"><span data-stu-id="830f6-124">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="830f6-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="830f6-125">-DataSetGranularity</span></span>
<span data-ttu-id="830f6-126">Детализация строк в экспорте.</span><span class="sxs-lookup"><span data-stu-id="830f6-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="830f6-127">В настоящее время поддерживается только "Ежедневно".</span><span class="sxs-lookup"><span data-stu-id="830f6-127">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="830f6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830f6-128">-DefaultProfile</span></span>
<span data-ttu-id="830f6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="830f6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830f6-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="830f6-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="830f6-131">Период времени для сбора данных для экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="830f6-132">Если он настраиваемый, необходимо ука-заметь конкретный период времени.</span><span class="sxs-lookup"><span data-stu-id="830f6-132">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="830f6-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="830f6-133">-DefinitionType</span></span>
<span data-ttu-id="830f6-134">Тип экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-134">The type of the export.</span></span>
<span data-ttu-id="830f6-135">Обратите внимание, что "Использование" эквивалентно actualCost и применимо к экспортам, которые пока не предоставляют данные для сплаты или амортизации для резервирования служб.</span><span class="sxs-lookup"><span data-stu-id="830f6-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="830f6-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="830f6-136">-DestinationContainer</span></span>
<span data-ttu-id="830f6-137">Имя контейнера, в который будет экспортироваться экспорт.</span><span class="sxs-lookup"><span data-stu-id="830f6-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="830f6-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="830f6-138">-DestinationResourceId</span></span>
<span data-ttu-id="830f6-139">ИД ресурса учетной записи хранения, в который будут доставлены экспорты.</span><span class="sxs-lookup"><span data-stu-id="830f6-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="830f6-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="830f6-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="830f6-141">Имя каталога, в который будут экспортироваться экспорты.</span><span class="sxs-lookup"><span data-stu-id="830f6-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="830f6-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="830f6-142">-ETag</span></span>
<span data-ttu-id="830f6-143">eTag of the resource.</span><span class="sxs-lookup"><span data-stu-id="830f6-143">eTag of the resource.</span></span>
<span data-ttu-id="830f6-144">Для обработки одновременного обновления это поле будет использоваться для определения того, обновляет ли пользователь последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="830f6-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="830f6-145">-Format</span><span class="sxs-lookup"><span data-stu-id="830f6-145">-Format</span></span>
<span data-ttu-id="830f6-146">Формат доставки.</span><span class="sxs-lookup"><span data-stu-id="830f6-146">The format of the export being delivered.</span></span>
<span data-ttu-id="830f6-147">В настоящее время поддерживается только "CSV".</span><span class="sxs-lookup"><span data-stu-id="830f6-147">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="830f6-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="830f6-148">-InputObject</span></span>
<span data-ttu-id="830f6-149">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="830f6-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="830f6-150">-Name</span><span class="sxs-lookup"><span data-stu-id="830f6-150">-Name</span></span>
<span data-ttu-id="830f6-151">Имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-151">Export Name.</span></span>

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

### <span data-ttu-id="830f6-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="830f6-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="830f6-153">Дата начала повторения.</span><span class="sxs-lookup"><span data-stu-id="830f6-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="830f6-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="830f6-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="830f6-155">Дата окончания повторения.</span><span class="sxs-lookup"><span data-stu-id="830f6-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="830f6-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="830f6-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="830f6-157">Повторение расписания.</span><span class="sxs-lookup"><span data-stu-id="830f6-157">The schedule recurrence.</span></span>

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

### <span data-ttu-id="830f6-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="830f6-158">-ScheduleStatus</span></span>
<span data-ttu-id="830f6-159">Состояние расписания экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-159">The status of the export's schedule.</span></span>
<span data-ttu-id="830f6-160">Если "Неактивна", расписание экспорта приостанавлилось.</span><span class="sxs-lookup"><span data-stu-id="830f6-160">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="830f6-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="830f6-161">-Scope</span></span>
<span data-ttu-id="830f6-162">Этот параметр определяет область затрат по стоимости с различных точек зрения : "Подписка", "Группа ресурсов" и "Предоставление службы".</span><span class="sxs-lookup"><span data-stu-id="830f6-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="830f6-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="830f6-163">-TimePeriodFrom</span></span>
<span data-ttu-id="830f6-164">Дата начала экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="830f6-164">The start date for export data.</span></span>

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

### <span data-ttu-id="830f6-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="830f6-165">-TimePeriodTo</span></span>
<span data-ttu-id="830f6-166">Даты окончания экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="830f6-166">The end date for export data.</span></span>

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

### <span data-ttu-id="830f6-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="830f6-167">-Confirm</span></span>
<span data-ttu-id="830f6-168">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="830f6-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="830f6-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830f6-169">-WhatIf</span></span>
<span data-ttu-id="830f6-170">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="830f6-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="830f6-171">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="830f6-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830f6-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830f6-172">CommonParameters</span></span>
<span data-ttu-id="830f6-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830f6-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830f6-174">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="830f6-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830f6-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="830f6-175">INPUTS</span></span>

### <span data-ttu-id="830f6-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="830f6-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="830f6-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="830f6-177">OUTPUTS</span></span>

### <span data-ttu-id="830f6-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="830f6-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="830f6-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="830f6-179">NOTES</span></span>

<span data-ttu-id="830f6-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="830f6-180">ALIASES</span></span>

<span data-ttu-id="830f6-181">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="830f6-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="830f6-182">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="830f6-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="830f6-183">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="830f6-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="830f6-184">INPUTOBJECT <ICostManagementIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="830f6-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="830f6-185">`[AlertId <String>]`: ИД оповещения</span><span class="sxs-lookup"><span data-stu-id="830f6-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="830f6-186">`[ExportName <String>]`: имя экспорта.</span><span class="sxs-lookup"><span data-stu-id="830f6-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="830f6-187">`[ExternalCloudProviderId <String>]`: {externalSubscriptionId}" для связанной учетной записи или {externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="830f6-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="830f6-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`Внешний поставщик облачных услуг, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="830f6-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="830f6-189">К ним относятся 'externalSubscriptions' для связанных учетных записей и externalBillingAccounts для консолидированной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="830f6-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="830f6-190">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="830f6-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="830f6-191">`[Scope <String>]`: область, связанная с действиями представления.</span><span class="sxs-lookup"><span data-stu-id="830f6-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="830f6-192">К ним относятся подписки/{subscriptionId}, для области действия подписки, "subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" для области resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" для области учетной записи вы выставления счетов, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" для области EnrollmentAccountunt, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for BillingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' для области InvoiceSection, "providers/Microsoft.Management/managementGroups/{managementGroupId}" for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}" for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}" для внешней подписки.</span><span class="sxs-lookup"><span data-stu-id="830f6-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="830f6-193">`[ViewName <String>]`: имя представления</span><span class="sxs-lookup"><span data-stu-id="830f6-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="830f6-194">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="830f6-194">RELATED LINKS</span></span>

