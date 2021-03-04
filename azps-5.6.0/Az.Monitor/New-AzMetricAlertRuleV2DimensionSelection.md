---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 244e71148557ef46ea3305f7dc2826eb06e3b50d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962899"
---
# <span data-ttu-id="7917f-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7917f-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="7917f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7917f-102">SYNOPSIS</span></span>
<span data-ttu-id="7917f-103">Создание объекта выбора локального измерения, который можно использовать для построения метрических критериев оповещения.</span><span class="sxs-lookup"><span data-stu-id="7917f-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="7917f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7917f-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7917f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7917f-105">DESCRIPTION</span></span>
<span data-ttu-id="7917f-106">С помощью cmdlet **New-AzMetricAlertRuleV2DimensionSelection** создается объект выбора локального измерения, который помогает создать критерии метрических оповещений с помощью [cmdlet New-AzMetricAlertRuleV2Criteria.](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria)</span><span class="sxs-lookup"><span data-stu-id="7917f-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet.</span></span>

## <span data-ttu-id="7917f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7917f-107">EXAMPLES</span></span>

### <span data-ttu-id="7917f-108">Пример 1. Создание объекта выделения размеров</span><span class="sxs-lookup"><span data-stu-id="7917f-108">Example 1: Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="7917f-109">Эта команда создает объект выбора измерения, который указывает, что значения должны быть выбраны для параметра {1,3,4} "ИЗМЕРЕНИЕ"</span><span class="sxs-lookup"><span data-stu-id="7917f-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="7917f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7917f-110">PARAMETERS</span></span>

### <span data-ttu-id="7917f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7917f-111">-DefaultProfile</span></span>
<span data-ttu-id="7917f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7917f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7917f-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="7917f-113">-DimensionName</span></span>
<span data-ttu-id="7917f-114">Имя измерения</span><span class="sxs-lookup"><span data-stu-id="7917f-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7917f-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="7917f-115">-ValuesToExclude</span></span>
<span data-ttu-id="7917f-116">The ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="7917f-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7917f-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="7917f-117">-ValuesToInclude</span></span>
<span data-ttu-id="7917f-118">The IncludeValues</span><span class="sxs-lookup"><span data-stu-id="7917f-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7917f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7917f-119">CommonParameters</span></span>
<span data-ttu-id="7917f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7917f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7917f-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7917f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7917f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7917f-122">INPUTS</span></span>

### <span data-ttu-id="7917f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7917f-123">System.String</span></span>

### <span data-ttu-id="7917f-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7917f-124">System.String[]</span></span>

## <span data-ttu-id="7917f-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7917f-125">OUTPUTS</span></span>

### <span data-ttu-id="7917f-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="7917f-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="7917f-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7917f-127">NOTES</span></span>

## <span data-ttu-id="7917f-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7917f-128">RELATED LINKS</span></span>
