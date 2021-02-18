---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 37f4d4b5650060b490e8c6bb691d938b78fa1166
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215257"
---
# <span data-ttu-id="641d6-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="641d6-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="641d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="641d6-102">SYNOPSIS</span></span>
<span data-ttu-id="641d6-103">Запрос данных об использовании для определенной области.</span><span class="sxs-lookup"><span data-stu-id="641d6-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="641d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="641d6-104">SYNTAX</span></span>

### <span data-ttu-id="641d6-105">UsageExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="641d6-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="641d6-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="641d6-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="641d6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="641d6-107">DESCRIPTION</span></span>
<span data-ttu-id="641d6-108">Запрос данных об использовании для определенной области.</span><span class="sxs-lookup"><span data-stu-id="641d6-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="641d6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="641d6-109">EXAMPLES</span></span>

### <span data-ttu-id="641d6-110">Пример 1. Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="641d6-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="641d6-111">Invoke AzCostManagementQuery by Scope</span><span class="sxs-lookup"><span data-stu-id="641d6-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="641d6-112">Пример 2. Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="641d6-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="641d6-113">Invoke AzCostManagementQuery by Scope with Dimensions</span><span class="sxs-lookup"><span data-stu-id="641d6-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="641d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="641d6-114">PARAMETERS</span></span>

### <span data-ttu-id="641d6-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="641d6-115">-ConfigurationColumn</span></span>
<span data-ttu-id="641d6-116">Массив имен столбцов, которые нужно включить в запрос.</span><span class="sxs-lookup"><span data-stu-id="641d6-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="641d6-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="641d6-117">-DatasetAggregation</span></span>
<span data-ttu-id="641d6-118">Словарь агрегирования выражения, используемого в запросе.</span><span class="sxs-lookup"><span data-stu-id="641d6-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="641d6-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="641d6-119">-DatasetFilter</span></span>
<span data-ttu-id="641d6-120">Имеет выражение фильтра, используемую в запросе.</span><span class="sxs-lookup"><span data-stu-id="641d6-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="641d6-121">Сведения о конструкции см. в разделе "Заметки" для свойств DATASETFILTER и создания hash table.</span><span class="sxs-lookup"><span data-stu-id="641d6-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="641d6-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="641d6-122">-DatasetGranularity</span></span>
<span data-ttu-id="641d6-123">Детализация строк в запросе.</span><span class="sxs-lookup"><span data-stu-id="641d6-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="641d6-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="641d6-124">-DatasetGrouping</span></span>
<span data-ttu-id="641d6-125">Массив группировки по выражению, который будет использовать в запросе.</span><span class="sxs-lookup"><span data-stu-id="641d6-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="641d6-126">Сведения о конструкции см. в разделе "ПРИМЕЧАНИЯ" для свойств DATASETGROUPING и создании hash table.</span><span class="sxs-lookup"><span data-stu-id="641d6-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

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

### <span data-ttu-id="641d6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641d6-127">-DefaultProfile</span></span>
<span data-ttu-id="641d6-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="641d6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="641d6-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="641d6-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="641d6-130">Это может быть {externalSubscriptionId}" для связанной учетной записи или {externalBillingAccountId}" для консолидированной учетной записи, которая используется для операций измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="641d6-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

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

### <span data-ttu-id="641d6-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="641d6-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="641d6-132">Тип внешнего облачного поставщика, связанный с операциями измерения или запроса.</span><span class="sxs-lookup"><span data-stu-id="641d6-132">The external cloud provider type associated with dimension/query operations.</span></span>

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

### <span data-ttu-id="641d6-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="641d6-133">-Scope</span></span>
<span data-ttu-id="641d6-134">К ним относятся подписки/{subscriptionId}/" для области действия подписки, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}" for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}" for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}" для области Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}" for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" for billingProfile Scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}" для области invoiceSection и "providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}" для партнеров.</span><span class="sxs-lookup"><span data-stu-id="641d6-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

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

### <span data-ttu-id="641d6-135">-Timeframe</span><span class="sxs-lookup"><span data-stu-id="641d6-135">-Timeframe</span></span>
<span data-ttu-id="641d6-136">Период времени для сбора данных по запросу.</span><span class="sxs-lookup"><span data-stu-id="641d6-136">The time frame for pulling data for the query.</span></span>

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

### <span data-ttu-id="641d6-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="641d6-137">-TimePeriodFrom</span></span>
<span data-ttu-id="641d6-138">Начальную дату для и извлекаемой информации.</span><span class="sxs-lookup"><span data-stu-id="641d6-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="641d6-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="641d6-139">-TimePeriodTo</span></span>
<span data-ttu-id="641d6-140">Даты окончания, к которые нужно вытащить данные.</span><span class="sxs-lookup"><span data-stu-id="641d6-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="641d6-141">-Type</span><span class="sxs-lookup"><span data-stu-id="641d6-141">-Type</span></span>
<span data-ttu-id="641d6-142">Тип запроса.</span><span class="sxs-lookup"><span data-stu-id="641d6-142">The type of the query.</span></span>

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

### <span data-ttu-id="641d6-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="641d6-143">-Confirm</span></span>
<span data-ttu-id="641d6-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="641d6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="641d6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="641d6-145">-WhatIf</span></span>
<span data-ttu-id="641d6-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="641d6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="641d6-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="641d6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="641d6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641d6-148">CommonParameters</span></span>
<span data-ttu-id="641d6-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="641d6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641d6-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="641d6-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641d6-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="641d6-151">INPUTS</span></span>

## <span data-ttu-id="641d6-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="641d6-152">OUTPUTS</span></span>

### <span data-ttu-id="641d6-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span><span class="sxs-lookup"><span data-stu-id="641d6-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="641d6-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="641d6-154">NOTES</span></span>

<span data-ttu-id="641d6-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="641d6-155">ALIASES</span></span>

<span data-ttu-id="641d6-156">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="641d6-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="641d6-157">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="641d6-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="641d6-158">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="641d6-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="641d6-159">DATASETFILTER: <IQueryFilter> имеет выражение фильтра, используемую в запросе.</span><span class="sxs-lookup"><span data-stu-id="641d6-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="641d6-160">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="641d6-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="641d6-161">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="641d6-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="641d6-162">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="641d6-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="641d6-163">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="641d6-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="641d6-164">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="641d6-164">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="641d6-165">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="641d6-165">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="641d6-166">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="641d6-166">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="641d6-167">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="641d6-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="641d6-168">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="641d6-168">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="641d6-169">DATASETGROUPING <IQueryGrouping[]>: массив группировки по выражению, который будет использовать в запросе.</span><span class="sxs-lookup"><span data-stu-id="641d6-169">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="641d6-170">`Name <String>`: имя столбца для группировки.</span><span class="sxs-lookup"><span data-stu-id="641d6-170">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="641d6-171">`Type <QueryColumnType>`: Тип столбца для группировки.</span><span class="sxs-lookup"><span data-stu-id="641d6-171">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="641d6-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="641d6-172">RELATED LINKS</span></span>

