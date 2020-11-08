---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 57741aa1f06816e8fac1bbb6722ea4d3c6f66761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064865"
---
# <span data-ttu-id="63dab-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="63dab-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="63dab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63dab-102">SYNOPSIS</span></span>
<span data-ttu-id="63dab-103">Создает объект выбора локального измерения, который можно использовать для создания критерия оповещения метрики.</span><span class="sxs-lookup"><span data-stu-id="63dab-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="63dab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63dab-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63dab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63dab-105">DESCRIPTION</span></span>
<span data-ttu-id="63dab-106">Командлет **New-AzMetricAlertRuleV2DimensionSelection** создает объект выбора локального измерения, чтобы упростить создание критериев оповещения метрики с помощью командлета **New-AzMetricAlertRuleV2Criteria** .</span><span class="sxs-lookup"><span data-stu-id="63dab-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="63dab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63dab-107">EXAMPLES</span></span>

### <span data-ttu-id="63dab-108">Пример 1: создание объекта выделения измерения</span><span class="sxs-lookup"><span data-stu-id="63dab-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="63dab-109">Эта команда создает объект выделения измерения, указывающий на то, что {1,3,4} для измерения "LUN" необходимо выбрать значения.</span><span class="sxs-lookup"><span data-stu-id="63dab-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="63dab-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63dab-110">PARAMETERS</span></span>

### <span data-ttu-id="63dab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63dab-111">-DefaultProfile</span></span>
<span data-ttu-id="63dab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63dab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63dab-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="63dab-113">-DimensionName</span></span>
<span data-ttu-id="63dab-114">Имя измерения</span><span class="sxs-lookup"><span data-stu-id="63dab-114">The Dimension name</span></span>

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

### <span data-ttu-id="63dab-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="63dab-115">-ValuesToExclude</span></span>
<span data-ttu-id="63dab-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="63dab-116">The ExcludeValues</span></span>

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

### <span data-ttu-id="63dab-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="63dab-117">-ValuesToInclude</span></span>
<span data-ttu-id="63dab-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="63dab-118">The IncludeValues</span></span>

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

### <span data-ttu-id="63dab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63dab-119">CommonParameters</span></span>
<span data-ttu-id="63dab-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63dab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63dab-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63dab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63dab-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63dab-122">INPUTS</span></span>

### <span data-ttu-id="63dab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="63dab-123">System.String</span></span>

### <span data-ttu-id="63dab-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="63dab-124">System.String[]</span></span>

## <span data-ttu-id="63dab-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63dab-125">OUTPUTS</span></span>

### <span data-ttu-id="63dab-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="63dab-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="63dab-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="63dab-127">NOTES</span></span>

## <span data-ttu-id="63dab-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63dab-128">RELATED LINKS</span></span>
