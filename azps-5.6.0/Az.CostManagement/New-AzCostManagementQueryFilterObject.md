---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: 84b54353b1f36dbfbb3cef068987c50a4b60923e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010648"
---
# <span data-ttu-id="7dfca-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="7dfca-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="7dfca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dfca-102">SYNOPSIS</span></span>
<span data-ttu-id="7dfca-103">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="7dfca-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="7dfca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7dfca-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="7dfca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dfca-105">DESCRIPTION</span></span>
<span data-ttu-id="7dfca-106">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="7dfca-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="7dfca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7dfca-107">EXAMPLES</span></span>

### <span data-ttu-id="7dfca-108">Пример 1. Создание объекта фильтра запроса для экспорта управления затратами</span><span class="sxs-lookup"><span data-stu-id="7dfca-108">Example 1: Create a filter object of query for cost management export</span></span>
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

<span data-ttu-id="7dfca-109">эта команда создает объект фильтра запроса для экспорта управления затратами.</span><span class="sxs-lookup"><span data-stu-id="7dfca-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="7dfca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dfca-110">PARAMETERS</span></span>

### <span data-ttu-id="7dfca-111">-And</span><span class="sxs-lookup"><span data-stu-id="7dfca-111">-And</span></span>
<span data-ttu-id="7dfca-112">Логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="7dfca-112">The logical "AND" expression.</span></span>
<span data-ttu-id="7dfca-113">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-113">Must have at least 2 items.</span></span>
<span data-ttu-id="7dfca-114">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств AND и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7dfca-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

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

### <span data-ttu-id="7dfca-115">-Размеры</span><span class="sxs-lookup"><span data-stu-id="7dfca-115">-Dimensions</span></span>
<span data-ttu-id="7dfca-116">Выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="7dfca-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="7dfca-117">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств "РАЗМЕРЫ" и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="7dfca-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

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

### <span data-ttu-id="7dfca-118">-Not</span><span class="sxs-lookup"><span data-stu-id="7dfca-118">-Not</span></span>
<span data-ttu-id="7dfca-119">Логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="7dfca-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="7dfca-120">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для СВОЙСТВА NOT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7dfca-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7dfca-121">-Или</span><span class="sxs-lookup"><span data-stu-id="7dfca-121">-Or</span></span>
<span data-ttu-id="7dfca-122">Логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="7dfca-122">The logical "OR" expression.</span></span>
<span data-ttu-id="7dfca-123">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-123">Must have at least 2 items.</span></span>
<span data-ttu-id="7dfca-124">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств OR и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7dfca-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

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

### <span data-ttu-id="7dfca-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7dfca-125">-Tag</span></span>
<span data-ttu-id="7dfca-126">Выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="7dfca-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="7dfca-127">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств тега и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="7dfca-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

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

### <span data-ttu-id="7dfca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dfca-128">CommonParameters</span></span>
<span data-ttu-id="7dfca-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dfca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dfca-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dfca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dfca-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dfca-131">INPUTS</span></span>

## <span data-ttu-id="7dfca-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7dfca-132">OUTPUTS</span></span>

### <span data-ttu-id="7dfca-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span><span class="sxs-lookup"><span data-stu-id="7dfca-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="7dfca-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7dfca-134">NOTES</span></span>

<span data-ttu-id="7dfca-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7dfca-135">ALIASES</span></span>

<span data-ttu-id="7dfca-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7dfca-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7dfca-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7dfca-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7dfca-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7dfca-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7dfca-139">AND <IQueryFilter[]>: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="7dfca-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="7dfca-140">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-141">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="7dfca-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="7dfca-142">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-143">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="7dfca-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="7dfca-144">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7dfca-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="7dfca-145">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="7dfca-145">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="7dfca-146">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="7dfca-146">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="7dfca-147">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="7dfca-147">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="7dfca-148">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-148">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-149">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="7dfca-149">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="7dfca-150">DIMENSIONS <IQueryComparisonExpression> : имеет выражение сравнения для измерений.</span><span class="sxs-lookup"><span data-stu-id="7dfca-150">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="7dfca-151">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7dfca-151">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="7dfca-152">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="7dfca-152">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="7dfca-153">NOT <IQueryFilter> : логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="7dfca-153">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="7dfca-154">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="7dfca-154">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="7dfca-155">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-155">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-156">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="7dfca-156">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="7dfca-157">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7dfca-157">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="7dfca-158">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="7dfca-158">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="7dfca-159">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="7dfca-159">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="7dfca-160">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="7dfca-160">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="7dfca-161">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-162">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="7dfca-162">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="7dfca-163">ИЛИ <IQueryFilter[]>: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="7dfca-163">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="7dfca-164">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-165">`[And <IQueryFilter[]>]`: логическое выражение AND.</span><span class="sxs-lookup"><span data-stu-id="7dfca-165">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="7dfca-166">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-166">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-167">`[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения</span><span class="sxs-lookup"><span data-stu-id="7dfca-167">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="7dfca-168">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7dfca-168">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="7dfca-169">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="7dfca-169">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="7dfca-170">`[Not <IQueryFilter>]`: логическое выражение NOT.</span><span class="sxs-lookup"><span data-stu-id="7dfca-170">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="7dfca-171">`[Or <IQueryFilter[]>]`: логическое выражение OR.</span><span class="sxs-lookup"><span data-stu-id="7dfca-171">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="7dfca-172">Должен иметь не менее 2 элементов.</span><span class="sxs-lookup"><span data-stu-id="7dfca-172">Must have at least 2 items.</span></span>
  - <span data-ttu-id="7dfca-173">`[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега</span><span class="sxs-lookup"><span data-stu-id="7dfca-173">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="7dfca-174">TAG <IQueryComparisonExpression> : имеет выражение сравнения для тега.</span><span class="sxs-lookup"><span data-stu-id="7dfca-174">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="7dfca-175">`Name <String>`: имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7dfca-175">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="7dfca-176">`Value <String[]>`: массив значений, которые нужно использовать для сравнения</span><span class="sxs-lookup"><span data-stu-id="7dfca-176">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="7dfca-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7dfca-177">RELATED LINKS</span></span>

