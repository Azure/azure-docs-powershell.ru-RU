---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: d2adba5ac5c75745c43e0d1ef62fb39d9b867c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230745"
---
# <span data-ttu-id="fec6b-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="fec6b-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="fec6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec6b-102">SYNOPSIS</span></span>
<span data-ttu-id="fec6b-103">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="fec6b-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="fec6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fec6b-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="fec6b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fec6b-105">DESCRIPTION</span></span>
<span data-ttu-id="fec6b-106">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="fec6b-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="fec6b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fec6b-107">EXAMPLES</span></span>

### <span data-ttu-id="fec6b-108">Пример 1. Создание объекта фильтра запроса для экспорта управления затратами</span><span class="sxs-lookup"><span data-stu-id="fec6b-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="fec6b-109">эта команда создает объект фильтра запроса для экспорта управления затратами.</span><span class="sxs-lookup"><span data-stu-id="fec6b-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="fec6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fec6b-110">PARAMETERS</span></span>

### <span data-ttu-id="fec6b-111">-And</span><span class="sxs-lookup"><span data-stu-id="fec6b-111">-And</span></span>
<span data-ttu-id="fec6b-112">Логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="fec6b-112">The logical "AND" expression.</span></span>
<span data-ttu-id="fec6b-113">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-113">Must have at least 2 items.</span></span>
<span data-ttu-id="fec6b-114">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств AND и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fec6b-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="fec6b-115">-Размеры</span><span class="sxs-lookup"><span data-stu-id="fec6b-115">-Dimensions</span></span>
<span data-ttu-id="fec6b-116">Выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="fec6b-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="fec6b-117">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств "РАЗМЕРЫ" и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="fec6b-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="fec6b-118">-Not</span><span class="sxs-lookup"><span data-stu-id="fec6b-118">-Not</span></span>
<span data-ttu-id="fec6b-119">Логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="fec6b-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="fec6b-120">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для СВОЙСТВА NOT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fec6b-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fec6b-121">-Или</span><span class="sxs-lookup"><span data-stu-id="fec6b-121">-Or</span></span>
<span data-ttu-id="fec6b-122">Логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="fec6b-122">The logical "OR" expression.</span></span>
<span data-ttu-id="fec6b-123">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-123">Must have at least 2 items.</span></span>
<span data-ttu-id="fec6b-124">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств OR и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fec6b-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="fec6b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fec6b-125">-Tag</span></span>
<span data-ttu-id="fec6b-126">Выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="fec6b-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="fec6b-127">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств тега и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fec6b-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="fec6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec6b-128">CommonParameters</span></span>
<span data-ttu-id="fec6b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec6b-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fec6b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec6b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fec6b-131">INPUTS</span></span>

## <span data-ttu-id="fec6b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fec6b-132">OUTPUTS</span></span>

### <span data-ttu-id="fec6b-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="fec6b-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="fec6b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fec6b-134">NOTES</span></span>

<span data-ttu-id="fec6b-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fec6b-135">ALIASES</span></span>

<span data-ttu-id="fec6b-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fec6b-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fec6b-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fec6b-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fec6b-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fec6b-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fec6b-139">И <IQueryFilter[]>: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="fec6b-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="fec6b-140">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-141">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="fec6b-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="fec6b-142">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-143">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="fec6b-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="fec6b-144">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fec6b-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="fec6b-145">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="fec6b-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="fec6b-146">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="fec6b-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="fec6b-147">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="fec6b-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="fec6b-148">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-149">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="fec6b-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="fec6b-150">DIMENSIONS <IQueryComparisonExpression> : имеет выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="fec6b-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="fec6b-151">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fec6b-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="fec6b-152">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="fec6b-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="fec6b-153">NOT <IQueryFilter> : логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="fec6b-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="fec6b-154">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="fec6b-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="fec6b-155">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-156">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="fec6b-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="fec6b-157">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fec6b-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="fec6b-158">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="fec6b-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="fec6b-159">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="fec6b-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="fec6b-160">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="fec6b-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="fec6b-161">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-162">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="fec6b-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="fec6b-163">ИЛИ <IQueryFilter[]>: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="fec6b-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="fec6b-164">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-165">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="fec6b-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="fec6b-166">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-167">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="fec6b-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="fec6b-168">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fec6b-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="fec6b-169">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="fec6b-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="fec6b-170">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="fec6b-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="fec6b-171">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="fec6b-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="fec6b-172">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="fec6b-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="fec6b-173">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="fec6b-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="fec6b-174">TAG <IQueryComparisonExpression> : имеет выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="fec6b-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="fec6b-175">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="fec6b-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="fec6b-176">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="fec6b-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="fec6b-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fec6b-177">RELATED LINKS</span></span>

