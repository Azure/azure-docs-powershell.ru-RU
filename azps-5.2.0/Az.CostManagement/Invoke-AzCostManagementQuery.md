---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394223"
---
# <span data-ttu-id="4a21f-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="4a21f-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="4a21f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a21f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a21f-103">Запрос данных об использовании для определенной области.</span><span class="sxs-lookup"><span data-stu-id="4a21f-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="4a21f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a21f-104">SYNTAX</span></span>

### <span data-ttu-id="4a21f-105">UsageExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a21f-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a21f-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="4a21f-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a21f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a21f-107">DESCRIPTION</span></span>
<span data-ttu-id="4a21f-108">Запрос данных об использовании для определенной области.</span><span class="sxs-lookup"><span data-stu-id="4a21f-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="4a21f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a21f-109">EXAMPLES</span></span>

### <span data-ttu-id="4a21f-110">Пример 1. Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="4a21f-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="4a21f-111">Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="4a21f-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="4a21f-112">Пример 2. Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="4a21f-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="4a21f-113">Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="4a21f-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="4a21f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a21f-114">PARAMETERS</span></span>

### <span data-ttu-id="4a21f-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="4a21f-115">-ConfigurationColumn</span></span>
<span data-ttu-id="4a21f-116">Массив имен столбцов, которые нужно включить в запрос.</span><span class="sxs-lookup"><span data-stu-id="4a21f-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="4a21f-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="4a21f-117">-DatasetAggregation</span></span>
<span data-ttu-id="4a21f-118">Словарь агрегирования выражения, используемого в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a21f-118">Dictionary of aggregation expression to use in the query.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="4a21f-119">-DatasetFilter</span></span>
<span data-ttu-id="4a21f-120">Имеет выражение фильтра, используемую в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a21f-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="4a21f-121">Сведения о конструкции см. в разделе "Заметки" для свойств DATASETFILTER и создании hash table.</span><span class="sxs-lookup"><span data-stu-id="4a21f-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="4a21f-122">-DatasetGranularity</span></span>
<span data-ttu-id="4a21f-123">Детализация строк в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a21f-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="4a21f-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="4a21f-124">-DatasetGrouping</span></span>
<span data-ttu-id="4a21f-125">Массив групп по выражению, который будет использовать в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a21f-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="4a21f-126">Сведения о конструкции см. в разделе "ПРИМЕЧАНИЯ" для свойств DATASETGROUPING и создании hash table.</span><span class="sxs-lookup"><span data-stu-id="4a21f-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a21f-127">-DefaultProfile</span></span>
<span data-ttu-id="4a21f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a21f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a21f-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="4a21f-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="4a21f-130">Это может быть {externalSubscriptionId}" для связанной учетной записи или {externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="4a21f-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="4a21f-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="4a21f-132">Тип внешнего облачного поставщика, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="4a21f-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="4a21f-133">-Scope</span></span>
<span data-ttu-id="4a21f-134">К ним относятся подписки/{subscriptionId}/" для области действия подписки, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for billingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}" для области invoiceSection и "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}" для партнеров.</span><span class="sxs-lookup"><span data-stu-id="4a21f-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-135">-Timeframe</span><span class="sxs-lookup"><span data-stu-id="4a21f-135">-Timeframe</span></span>
<span data-ttu-id="4a21f-136">Период времени, за который нужно получить данные для запроса.</span><span class="sxs-lookup"><span data-stu-id="4a21f-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="4a21f-137">-TimePeriodFrom</span></span>
<span data-ttu-id="4a21f-138">Начальную дату для и извлекаемой информации.</span><span class="sxs-lookup"><span data-stu-id="4a21f-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="4a21f-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="4a21f-139">-TimePeriodTo</span></span>
<span data-ttu-id="4a21f-140">Даты окончания, до которые нужно вытащить данные.</span><span class="sxs-lookup"><span data-stu-id="4a21f-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="4a21f-141">-Type</span><span class="sxs-lookup"><span data-stu-id="4a21f-141">-Type</span></span>
<span data-ttu-id="4a21f-142">Тип запроса.</span><span class="sxs-lookup"><span data-stu-id="4a21f-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a21f-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a21f-143">-Confirm</span></span>
<span data-ttu-id="4a21f-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a21f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a21f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a21f-145">-WhatIf</span></span>
<span data-ttu-id="4a21f-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a21f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a21f-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a21f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a21f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a21f-148">CommonParameters</span></span>
<span data-ttu-id="4a21f-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a21f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a21f-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a21f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a21f-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a21f-151">INPUTS</span></span>

## <span data-ttu-id="4a21f-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a21f-152">OUTPUTS</span></span>

### <span data-ttu-id="4a21f-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="4a21f-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="4a21f-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a21f-154">NOTES</span></span>

<span data-ttu-id="4a21f-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4a21f-155">ALIASES</span></span>

<span data-ttu-id="4a21f-156">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4a21f-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a21f-157">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a21f-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a21f-158">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a21f-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a21f-159">DATASETFILTER: <IQueryFilter> имеет выражение фильтра, используемую в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a21f-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="4a21f-160">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="4a21f-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="4a21f-161">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="4a21f-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4a21f-162">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="4a21f-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="4a21f-163">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="4a21f-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="4a21f-164">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="4a21f-164">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="4a21f-165">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="4a21f-165">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="4a21f-166">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="4a21f-166">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="4a21f-167">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="4a21f-167">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="4a21f-168">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="4a21f-168">Must have at least 2 items.</span></span>
  - <span data-ttu-id="4a21f-169">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="4a21f-169">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="4a21f-170">DATASETGROUPING <IQueryGrouping[]>: массив группировки по выражению, который будет использовать в запросе.</span><span class="sxs-lookup"><span data-stu-id="4a21f-170">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="4a21f-171">`Name <String>`: имя столбца для группировки.</span><span class="sxs-lookup"><span data-stu-id="4a21f-171">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="4a21f-172">`Type <QueryColumnType>`: Тип столбца для группировки.</span><span class="sxs-lookup"><span data-stu-id="4a21f-172">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="4a21f-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a21f-173">RELATED LINKS</span></span>
