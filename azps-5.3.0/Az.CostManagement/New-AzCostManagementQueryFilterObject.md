---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519149"
---
# <span data-ttu-id="b4abb-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="b4abb-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="b4abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4abb-102">SYNOPSIS</span></span>
<span data-ttu-id="b4abb-103">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="b4abb-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="b4abb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4abb-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="b4abb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4abb-105">DESCRIPTION</span></span>
<span data-ttu-id="b4abb-106">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="b4abb-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="b4abb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4abb-107">EXAMPLES</span></span>

### <span data-ttu-id="b4abb-108">Пример 1. Создание объекта фильтра запроса для экспорта управления затратами</span><span class="sxs-lookup"><span data-stu-id="b4abb-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="b4abb-109">эта команда создает объект фильтра запроса для экспорта управления затратами.</span><span class="sxs-lookup"><span data-stu-id="b4abb-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="b4abb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4abb-110">PARAMETERS</span></span>

### <span data-ttu-id="b4abb-111">-And</span><span class="sxs-lookup"><span data-stu-id="b4abb-111">-And</span></span>
<span data-ttu-id="b4abb-112">Логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="b4abb-112">The logical "AND" expression.</span></span>
<span data-ttu-id="b4abb-113">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-113">Must have at least 2 items.</span></span>
<span data-ttu-id="b4abb-114">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств AND и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b4abb-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4abb-115">-Размеры</span><span class="sxs-lookup"><span data-stu-id="b4abb-115">-Dimensions</span></span>
<span data-ttu-id="b4abb-116">Выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="b4abb-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="b4abb-117">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств "РАЗМЕРЫ" и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="b4abb-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4abb-118">-Not</span><span class="sxs-lookup"><span data-stu-id="b4abb-118">-Not</span></span>
<span data-ttu-id="b4abb-119">Логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="b4abb-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="b4abb-120">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для СВОЙСТВА NOT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b4abb-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4abb-121">-Или</span><span class="sxs-lookup"><span data-stu-id="b4abb-121">-Or</span></span>
<span data-ttu-id="b4abb-122">Логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="b4abb-122">The logical "OR" expression.</span></span>
<span data-ttu-id="b4abb-123">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-123">Must have at least 2 items.</span></span>
<span data-ttu-id="b4abb-124">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств OR и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b4abb-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4abb-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4abb-125">-Tag</span></span>
<span data-ttu-id="b4abb-126">Выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="b4abb-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="b4abb-127">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств тега и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b4abb-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4abb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4abb-128">CommonParameters</span></span>
<span data-ttu-id="b4abb-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4abb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4abb-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4abb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4abb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4abb-131">INPUTS</span></span>

## <span data-ttu-id="b4abb-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4abb-132">OUTPUTS</span></span>

### <span data-ttu-id="b4abb-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="b4abb-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="b4abb-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4abb-134">NOTES</span></span>

<span data-ttu-id="b4abb-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b4abb-135">ALIASES</span></span>

<span data-ttu-id="b4abb-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b4abb-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b4abb-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b4abb-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4abb-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4abb-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b4abb-139">И <IQueryFilter[]>: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="b4abb-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="b4abb-140">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-141">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="b4abb-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="b4abb-142">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-143">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="b4abb-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="b4abb-144">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="b4abb-145">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="b4abb-146">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="b4abb-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="b4abb-147">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="b4abb-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="b4abb-148">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="b4abb-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="b4abb-149">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-150">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="b4abb-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="b4abb-151">DIMENSIONS <IQueryComparisonExpression> : имеет выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="b4abb-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="b4abb-152">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="b4abb-153">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="b4abb-154">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="b4abb-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="b4abb-155">NOT <IQueryFilter> : логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="b4abb-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="b4abb-156">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="b4abb-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="b4abb-157">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-158">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="b4abb-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="b4abb-159">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="b4abb-160">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="b4abb-161">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="b4abb-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="b4abb-162">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="b4abb-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="b4abb-163">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="b4abb-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="b4abb-164">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-165">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="b4abb-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="b4abb-166">ИЛИ <IQueryFilter[]>: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="b4abb-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="b4abb-167">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-168">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="b4abb-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="b4abb-169">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-170">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="b4abb-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="b4abb-171">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="b4abb-172">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="b4abb-173">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="b4abb-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="b4abb-174">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="b4abb-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="b4abb-175">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="b4abb-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="b4abb-176">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="b4abb-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="b4abb-177">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="b4abb-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="b4abb-178">TAG <IQueryComparisonExpression> : имеет выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="b4abb-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="b4abb-179">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="b4abb-180">`Operator <OperatorType>`Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4abb-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="b4abb-181">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="b4abb-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="b4abb-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4abb-182">RELATED LINKS</span></span>

