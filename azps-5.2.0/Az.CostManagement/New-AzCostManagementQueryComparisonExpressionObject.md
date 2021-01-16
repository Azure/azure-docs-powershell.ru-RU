---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395548"
---
# <span data-ttu-id="9cd9a-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="9cd9a-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="9cd9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd9a-103">Создание объекта в памяти для запросаComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="9cd9a-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="9cd9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9cd9a-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="9cd9a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cd9a-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd9a-106">Создание объекта в памяти для запросаComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="9cd9a-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="9cd9a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9cd9a-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd9a-108">Пример 1. Создание объекта выражения сравнения запроса для экспорта управления затратами</span><span class="sxs-lookup"><span data-stu-id="9cd9a-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="9cd9a-109">Эта команда создает объект выражения сравнения запроса для экспорта управления затратами.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="9cd9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cd9a-110">PARAMETERS</span></span>

### <span data-ttu-id="9cd9a-111">-Name</span><span class="sxs-lookup"><span data-stu-id="9cd9a-111">-Name</span></span>
<span data-ttu-id="9cd9a-112">Имя столбца, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="9cd9a-113">-Operator</span><span class="sxs-lookup"><span data-stu-id="9cd9a-113">-Operator</span></span>
<span data-ttu-id="9cd9a-114">Оператор, который нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-114">The operator to use for comparison.</span></span>

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

### <span data-ttu-id="9cd9a-115">-Value</span><span class="sxs-lookup"><span data-stu-id="9cd9a-115">-Value</span></span>
<span data-ttu-id="9cd9a-116">Массив значений, которые нужно использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="9cd9a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd9a-117">CommonParameters</span></span>
<span data-ttu-id="9cd9a-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd9a-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cd9a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd9a-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cd9a-120">INPUTS</span></span>

## <span data-ttu-id="9cd9a-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9cd9a-121">OUTPUTS</span></span>

### <span data-ttu-id="9cd9a-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="9cd9a-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="9cd9a-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9cd9a-123">NOTES</span></span>

<span data-ttu-id="9cd9a-124">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9cd9a-124">ALIASES</span></span>

## <span data-ttu-id="9cd9a-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cd9a-125">RELATED LINKS</span></span>

