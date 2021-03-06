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
# New-AzCostManagementQueryFilterObject

## SYNOPSIS
Создание объекта в памяти для queryFilter

## СИНТАКСИС

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## ОПИСАНИЕ
Создание объекта в памяти для queryFilter

## ПРИМЕРЫ

### Пример 1. Создание объекта фильтра запроса для экспорта управления затратами
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

эта команда создает объект фильтра запроса для экспорта управления затратами.

## PARAMETERS

### -And
Логическое выражение AND.
Должен иметь не менее 2 элементов.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств AND и создание hash table.

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

### -Размеры
Выражение сравнения для измерений.
Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств "РАЗМЕРЫ" и создание таблицы с hash.

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

### -Not
Логическое выражение NOT.
Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для СВОЙСТВА NOT и создание hash table.

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

### -Или
Логическое выражение OR.
Должен иметь не менее 2 элементов.
Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств OR и создание hash table.

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

### -Tag
Выражение сравнения для тега.
Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств тега и создание hash table.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


И <IQueryFilter[]>: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[And <IQueryFilter[]>]`: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения
    - `Name <String>`: имя столбца, который нужно использовать для сравнения.
    - `Value <String[]>`: массив значений, которые нужно использовать для сравнения
  - `[Not <IQueryFilter>]`: логическое выражение NOT.
  - `[Or <IQueryFilter[]>]`: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега

DIMENSIONS <IQueryComparisonExpression> : имеет выражение сравнения для измерений.
  - `Name <String>`: имя столбца, который нужно использовать для сравнения.
  - `Value <String[]>`: массив значений, которые нужно использовать для сравнения

NOT <IQueryFilter> : логическое выражение NOT.
  - `[And <IQueryFilter[]>]`: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения
    - `Name <String>`: имя столбца, который нужно использовать для сравнения.
    - `Value <String[]>`: массив значений, которые нужно использовать для сравнения
  - `[Not <IQueryFilter>]`: логическое выражение NOT.
  - `[Or <IQueryFilter[]>]`: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега

ИЛИ <IQueryFilter[]>: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[And <IQueryFilter[]>]`: логическое выражение AND. Должен иметь не менее 2 элементов.
  - `[Dimensions <IQueryComparisonExpression>]`: имеет выражение сравнения для измерения
    - `Name <String>`: имя столбца, который нужно использовать для сравнения.
    - `Value <String[]>`: массив значений, которые нужно использовать для сравнения
  - `[Not <IQueryFilter>]`: логическое выражение NOT.
  - `[Or <IQueryFilter[]>]`: логическое выражение OR. Должен иметь не менее 2 элементов.
  - `[Tag <IQueryComparisonExpression>]`: имеет выражение сравнения для тега

TAG <IQueryComparisonExpression> : имеет выражение сравнения для тега.
  - `Name <String>`: имя столбца, который нужно использовать для сравнения.
  - `Value <String[]>`: массив значений, которые нужно использовать для сравнения

## СВЯЗАННЫЕ ССЫЛКИ

