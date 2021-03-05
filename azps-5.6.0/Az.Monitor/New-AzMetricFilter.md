---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: a7fdb0824d464f1704f46a8e8fe19705b2b160fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012904"
---
# <span data-ttu-id="b6382-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="b6382-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="b6382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6382-102">SYNOPSIS</span></span>
<span data-ttu-id="b6382-103">Создает фильтр метрических измерений, который можно использовать для метрики запросов.</span><span class="sxs-lookup"><span data-stu-id="b6382-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="b6382-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6382-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6382-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6382-105">DESCRIPTION</span></span>
<span data-ttu-id="b6382-106">С **помощью нового фильтра AzMetricFilter** создается фильтр метрических измерений, который можно использовать для метрики запроса.</span><span class="sxs-lookup"><span data-stu-id="b6382-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="b6382-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6382-107">EXAMPLES</span></span>

### <span data-ttu-id="b6382-108">Пример 1. Создание фильтра метрических измерений</span><span class="sxs-lookup"><span data-stu-id="b6382-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="b6382-109">Эта команда создает фильтр метрических измерений в формате "Город eq 'Seattle' или City eq 'New York'".</span><span class="sxs-lookup"><span data-stu-id="b6382-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="b6382-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6382-110">PARAMETERS</span></span>

### <span data-ttu-id="b6382-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6382-111">-DefaultProfile</span></span>
<span data-ttu-id="b6382-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6382-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6382-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="b6382-113">-Dimension</span></span>
<span data-ttu-id="b6382-114">Имя измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="b6382-114">The name of the metric dimension.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6382-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="b6382-115">-Operator</span></span>
<span data-ttu-id="b6382-116">Оператор, используемый для выбора измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="b6382-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6382-117">-Value</span><span class="sxs-lookup"><span data-stu-id="b6382-117">-Value</span></span>
<span data-ttu-id="b6382-118">Массив значений метрических измерений.</span><span class="sxs-lookup"><span data-stu-id="b6382-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6382-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6382-119">CommonParameters</span></span>
<span data-ttu-id="b6382-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6382-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6382-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6382-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6382-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6382-122">INPUTS</span></span>

### <span data-ttu-id="b6382-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b6382-123">System.String</span></span>

### <span data-ttu-id="b6382-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b6382-124">System.String[]</span></span>

## <span data-ttu-id="b6382-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6382-125">OUTPUTS</span></span>

### <span data-ttu-id="b6382-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b6382-126">System.String</span></span>

## <span data-ttu-id="b6382-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6382-127">NOTES</span></span>

## <span data-ttu-id="b6382-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6382-128">RELATED LINKS</span></span>

<span data-ttu-id="b6382-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="b6382-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

