---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734962"
---
# <span data-ttu-id="480aa-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="480aa-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="480aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="480aa-102">SYNOPSIS</span></span>
<span data-ttu-id="480aa-103">Создает фильтр измерения метрики, который можно использовать для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="480aa-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="480aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="480aa-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="480aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="480aa-105">DESCRIPTION</span></span>
<span data-ttu-id="480aa-106">Командлет **New-AzureRmMetricFilter** создает фильтр измерения метрики, который можно использовать для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="480aa-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="480aa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="480aa-107">EXAMPLES</span></span>

### <span data-ttu-id="480aa-108">Пример 1: Создание фильтра измерения метрики</span><span class="sxs-lookup"><span data-stu-id="480aa-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="480aa-109">Эта команда создает фильтр измерения метрики с форматом "город EQ" Сиэтле "или" город EQ "" Нью Йорк "".</span><span class="sxs-lookup"><span data-stu-id="480aa-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="480aa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="480aa-110">PARAMETERS</span></span>

### <span data-ttu-id="480aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480aa-111">-DefaultProfile</span></span>
<span data-ttu-id="480aa-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="480aa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480aa-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="480aa-113">-Dimension</span></span>
<span data-ttu-id="480aa-114">Имя измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="480aa-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="480aa-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="480aa-115">-Operator</span></span>
<span data-ttu-id="480aa-116">Указывает оператор, используемый для выбора измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="480aa-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="480aa-117">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="480aa-117">-Value</span></span>
<span data-ttu-id="480aa-118">Задает массив значений измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="480aa-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="480aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480aa-119">CommonParameters</span></span>
<span data-ttu-id="480aa-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="480aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480aa-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="480aa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480aa-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="480aa-122">INPUTS</span></span>

### <span data-ttu-id="480aa-123">System. String</span><span class="sxs-lookup"><span data-stu-id="480aa-123">System.String</span></span>

### <span data-ttu-id="480aa-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="480aa-124">System.String[]</span></span>

## <span data-ttu-id="480aa-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="480aa-125">OUTPUTS</span></span>

### <span data-ttu-id="480aa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="480aa-126">System.String</span></span>

## <span data-ttu-id="480aa-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="480aa-127">NOTES</span></span>

## <span data-ttu-id="480aa-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="480aa-128">RELATED LINKS</span></span>

<span data-ttu-id="480aa-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="480aa-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

