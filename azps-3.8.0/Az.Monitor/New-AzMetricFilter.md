---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064866"
---
# <span data-ttu-id="8602e-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="8602e-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="8602e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8602e-102">SYNOPSIS</span></span>
<span data-ttu-id="8602e-103">Создает фильтр измерения метрики, который можно использовать для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="8602e-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="8602e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8602e-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8602e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8602e-105">DESCRIPTION</span></span>
<span data-ttu-id="8602e-106">Командлет **New-AzMetricFilter** создает фильтр измерения метрики, который можно использовать для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="8602e-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="8602e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8602e-107">EXAMPLES</span></span>

### <span data-ttu-id="8602e-108">Пример 1: Создание фильтра измерения метрики</span><span class="sxs-lookup"><span data-stu-id="8602e-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="8602e-109">Эта команда создает фильтр измерения метрики с форматом "город EQ" Сиэтле "или" город EQ "" Нью Йорк "".</span><span class="sxs-lookup"><span data-stu-id="8602e-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="8602e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8602e-110">PARAMETERS</span></span>

### <span data-ttu-id="8602e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8602e-111">-DefaultProfile</span></span>
<span data-ttu-id="8602e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8602e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8602e-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="8602e-113">-Dimension</span></span>
<span data-ttu-id="8602e-114">Имя измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="8602e-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="8602e-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="8602e-115">-Operator</span></span>
<span data-ttu-id="8602e-116">Указывает оператор, используемый для выбора измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="8602e-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="8602e-117">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="8602e-117">-Value</span></span>
<span data-ttu-id="8602e-118">Задает массив значений измерения метрики.</span><span class="sxs-lookup"><span data-stu-id="8602e-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="8602e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8602e-119">CommonParameters</span></span>
<span data-ttu-id="8602e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8602e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8602e-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8602e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8602e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8602e-122">INPUTS</span></span>

### <span data-ttu-id="8602e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8602e-123">System.String</span></span>

### <span data-ttu-id="8602e-124">System. String []</span><span class="sxs-lookup"><span data-stu-id="8602e-124">System.String[]</span></span>

## <span data-ttu-id="8602e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8602e-125">OUTPUTS</span></span>

### <span data-ttu-id="8602e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8602e-126">System.String</span></span>

## <span data-ttu-id="8602e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8602e-127">NOTES</span></span>

## <span data-ttu-id="8602e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8602e-128">RELATED LINKS</span></span>

<span data-ttu-id="8602e-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="8602e-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

