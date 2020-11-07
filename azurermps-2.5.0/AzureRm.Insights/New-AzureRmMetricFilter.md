---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913889"
---
# <span data-ttu-id="16f28-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="16f28-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="16f28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16f28-102">SYNOPSIS</span></span>
<span data-ttu-id="16f28-103">Создает фильтр измерения метрики, который можно использовать для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="16f28-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16f28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16f28-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16f28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16f28-105">DESCRIPTION</span></span>
<span data-ttu-id="16f28-106">Командлет **New-AzureRmMetricFilter** создает фильтр измерения метрики, который можно использовать для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="16f28-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="16f28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16f28-107">EXAMPLES</span></span>

### <span data-ttu-id="16f28-108">Пример 1: Создание фильтра измерения метрики</span><span class="sxs-lookup"><span data-stu-id="16f28-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="16f28-109">Эта команда создает фильтр измерения метрики с форматом "город EQ" Сиэтле "или" город EQ "" Нью Йорк "".</span><span class="sxs-lookup"><span data-stu-id="16f28-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="16f28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16f28-110">PARAMETERS</span></span>

### <span data-ttu-id="16f28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f28-111">-DefaultProfile</span></span>
<span data-ttu-id="16f28-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16f28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f28-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="16f28-113">-Dimension</span></span>
<span data-ttu-id="16f28-114">Имя измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="16f28-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="16f28-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="16f28-115">-Operator</span></span>
<span data-ttu-id="16f28-116">Указывает оператор, используемый для выбора измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="16f28-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="16f28-117">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="16f28-117">-Value</span></span>
<span data-ttu-id="16f28-118">Задает массив значений измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="16f28-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="16f28-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f28-119">CommonParameters</span></span>
<span data-ttu-id="16f28-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16f28-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f28-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f28-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f28-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16f28-122">INPUTS</span></span>

### <span data-ttu-id="16f28-123">System. String</span><span class="sxs-lookup"><span data-stu-id="16f28-123">System.String</span></span>

### <span data-ttu-id="16f28-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="16f28-124">System.String[]</span></span>

## <span data-ttu-id="16f28-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16f28-125">OUTPUTS</span></span>

### <span data-ttu-id="16f28-126">System. String</span><span class="sxs-lookup"><span data-stu-id="16f28-126">System.String</span></span>

## <span data-ttu-id="16f28-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="16f28-127">NOTES</span></span>

## <span data-ttu-id="16f28-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16f28-128">RELATED LINKS</span></span>

<span data-ttu-id="16f28-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="16f28-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

