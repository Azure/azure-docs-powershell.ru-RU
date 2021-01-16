---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395532"
---
# <span data-ttu-id="3c930-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="3c930-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="3c930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c930-102">SYNOPSIS</span></span>
<span data-ttu-id="3c930-103">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="3c930-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="3c930-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c930-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="3c930-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c930-105">DESCRIPTION</span></span>
<span data-ttu-id="3c930-106">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="3c930-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="3c930-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c930-107">EXAMPLES</span></span>

### <span data-ttu-id="3c930-108">Пример 1. Создание объекта фильтра запроса для экспорта управления затратами</span><span class="sxs-lookup"><span data-stu-id="3c930-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="3c930-109">эта команда создает объект фильтра запроса для экспорта управления затратами.</span><span class="sxs-lookup"><span data-stu-id="3c930-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="3c930-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c930-110">PARAMETERS</span></span>

### <span data-ttu-id="3c930-111">-And</span><span class="sxs-lookup"><span data-stu-id="3c930-111">-And</span></span>
<span data-ttu-id="3c930-112">Логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="3c930-112">The logical "AND" expression.</span></span>
<span data-ttu-id="3c930-113">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-113">Must have at least 2 items.</span></span>
<span data-ttu-id="3c930-114">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств AND и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3c930-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c930-115">-Размеры</span><span class="sxs-lookup"><span data-stu-id="3c930-115">-Dimensions</span></span>
<span data-ttu-id="3c930-116">Выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="3c930-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="3c930-117">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств "РАЗМЕРЫ" и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="3c930-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c930-118">-Not</span><span class="sxs-lookup"><span data-stu-id="3c930-118">-Not</span></span>
<span data-ttu-id="3c930-119">Логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="3c930-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="3c930-120">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для СВОЙСТВА NOT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3c930-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c930-121">-Или</span><span class="sxs-lookup"><span data-stu-id="3c930-121">-Or</span></span>
<span data-ttu-id="3c930-122">Логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="3c930-122">The logical "OR" expression.</span></span>
<span data-ttu-id="3c930-123">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-123">Must have at least 2 items.</span></span>
<span data-ttu-id="3c930-124">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств OR и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3c930-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c930-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c930-125">-Tag</span></span>
<span data-ttu-id="3c930-126">Выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="3c930-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="3c930-127">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств тега и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3c930-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c930-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c930-128">CommonParameters</span></span>
<span data-ttu-id="3c930-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c930-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c930-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c930-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c930-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c930-131">INPUTS</span></span>

## <span data-ttu-id="3c930-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c930-132">OUTPUTS</span></span>

### <span data-ttu-id="3c930-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="3c930-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="3c930-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c930-134">NOTES</span></span>

<span data-ttu-id="3c930-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3c930-135">ALIASES</span></span>

<span data-ttu-id="3c930-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3c930-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c930-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c930-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c930-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c930-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c930-139">AND <IQueryFilter[]>: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="3c930-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="3c930-140">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-141">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="3c930-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="3c930-142">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-143">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="3c930-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="3c930-144">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="3c930-145">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="3c930-146">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="3c930-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="3c930-147">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="3c930-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="3c930-148">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="3c930-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="3c930-149">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-150">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="3c930-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="3c930-151">DIMENSIONS <IQueryComparisonExpression> : имеет выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="3c930-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="3c930-152">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="3c930-153">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="3c930-154">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="3c930-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="3c930-155">NOT <IQueryFilter> : логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="3c930-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="3c930-156">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="3c930-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="3c930-157">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-158">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="3c930-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="3c930-159">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="3c930-160">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="3c930-161">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="3c930-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="3c930-162">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="3c930-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="3c930-163">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="3c930-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="3c930-164">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-165">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="3c930-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="3c930-166">ИЛИ <IQueryFilter[]>: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="3c930-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="3c930-167">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-168">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="3c930-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="3c930-169">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-170">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="3c930-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="3c930-171">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="3c930-172">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="3c930-173">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="3c930-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="3c930-174">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="3c930-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="3c930-175">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="3c930-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="3c930-176">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="3c930-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="3c930-177">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="3c930-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="3c930-178">TAG <IQueryComparisonExpression> : имеет выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="3c930-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="3c930-179">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="3c930-180">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3c930-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="3c930-181">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="3c930-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="3c930-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c930-182">RELATED LINKS</span></span>

