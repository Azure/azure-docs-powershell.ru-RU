---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 608736e8ddb85b877995bed8a42b9bd629dcdba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215241"
---
# New-AzCostManagementQueryComparisonExpressionObject

## SYNOPSIS
Создание объекта в памяти для запросаComparisonExpression

## СИНТАКСИС

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## ОПИСАНИЕ
Создание объекта в памяти для запросаComparisonExpression

## ПРИМЕРЫ

### Пример 1. Создание объекта выражения сравнения запроса для экспорта управления затратами
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

Эта команда создает объект выражения сравнения запроса для экспорта управления затратами.

## PARAMETERS

### -Name
Имя столбца, который нужно использовать для сравнения.

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

### -Operator
Оператор для сравнения.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Массив значений, которые нужно использовать для сравнения.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression

## ПРИМЕЧАНИЯ

ALIASES

## СВЯЗАННЫЕ ССЫЛКИ

