---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392164"
---
# <span data-ttu-id="878fa-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="878fa-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="878fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="878fa-102">SYNOPSIS</span></span>
<span data-ttu-id="878fa-103">Создает фильтр метрических измерений, который можно использовать для метрики запросов.</span><span class="sxs-lookup"><span data-stu-id="878fa-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="878fa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="878fa-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="878fa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="878fa-105">DESCRIPTION</span></span>
<span data-ttu-id="878fa-106">С **помощью нового фильтра AzMetricFilter** создается фильтр метрических измерений, который можно использовать для метрики запроса.</span><span class="sxs-lookup"><span data-stu-id="878fa-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="878fa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="878fa-107">EXAMPLES</span></span>

### <span data-ttu-id="878fa-108">Пример 1. Создание фильтра метрических измерений</span><span class="sxs-lookup"><span data-stu-id="878fa-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="878fa-109">Эта команда создает фильтр метрических измерений в формате "Город eq 'Seattle' или City eq 'New York'".</span><span class="sxs-lookup"><span data-stu-id="878fa-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="878fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="878fa-110">PARAMETERS</span></span>

### <span data-ttu-id="878fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878fa-111">-DefaultProfile</span></span>
<span data-ttu-id="878fa-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="878fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="878fa-113">-Размерность</span><span class="sxs-lookup"><span data-stu-id="878fa-113">-Dimension</span></span>
<span data-ttu-id="878fa-114">Имя измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="878fa-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="878fa-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="878fa-115">-Operator</span></span>
<span data-ttu-id="878fa-116">Оператор, используемый для выбора измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="878fa-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="878fa-117">-Значение</span><span class="sxs-lookup"><span data-stu-id="878fa-117">-Value</span></span>
<span data-ttu-id="878fa-118">Массив значений метрических измерений.</span><span class="sxs-lookup"><span data-stu-id="878fa-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="878fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878fa-119">CommonParameters</span></span>
<span data-ttu-id="878fa-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="878fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878fa-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="878fa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878fa-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="878fa-122">INPUTS</span></span>

### <span data-ttu-id="878fa-123">System.String</span><span class="sxs-lookup"><span data-stu-id="878fa-123">System.String</span></span>

### <span data-ttu-id="878fa-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="878fa-124">System.String[]</span></span>

## <span data-ttu-id="878fa-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="878fa-125">OUTPUTS</span></span>

### <span data-ttu-id="878fa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="878fa-126">System.String</span></span>

## <span data-ttu-id="878fa-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="878fa-127">NOTES</span></span>

## <span data-ttu-id="878fa-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="878fa-128">RELATED LINKS</span></span>

<span data-ttu-id="878fa-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="878fa-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

