---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d81043e165600a549bace91458449577b23dbd8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077050"
---
# <span data-ttu-id="4d015-101">Get-AzsQueueServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="4d015-101">Get-AzsQueueServiceMetricDefinition</span></span>

## <span data-ttu-id="4d015-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d015-102">SYNOPSIS</span></span>
<span data-ttu-id="4d015-103">Возвращает список определений метрик для службы очереди.</span><span class="sxs-lookup"><span data-stu-id="4d015-103">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="4d015-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d015-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4d015-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d015-105">DESCRIPTION</span></span>
<span data-ttu-id="4d015-106">Возвращает список определений метрик для службы очереди.</span><span class="sxs-lookup"><span data-stu-id="4d015-106">Returns a list of metric definitions for queue service.</span></span>

## <span data-ttu-id="4d015-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d015-107">EXAMPLES</span></span>

### <span data-ttu-id="4d015-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="4d015-108">EXAMPLE 1</span></span>
```
Get-AzsQueueServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="4d015-109">Получение списка определений метрик для службы очередей.</span><span class="sxs-lookup"><span data-stu-id="4d015-109">Get the list of metric definitions for queue service.</span></span>

## <span data-ttu-id="4d015-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d015-110">PARAMETERS</span></span>

### <span data-ttu-id="4d015-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="4d015-111">-FarmName</span></span>
<span data-ttu-id="4d015-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="4d015-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d015-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d015-113">-ResourceGroupName</span></span>
<span data-ttu-id="4d015-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d015-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d015-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="4d015-115">-Skip</span></span>
<span data-ttu-id="4d015-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="4d015-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d015-117">-Top</span><span class="sxs-lookup"><span data-stu-id="4d015-117">-Top</span></span>
<span data-ttu-id="4d015-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="4d015-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4d015-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="4d015-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d015-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d015-120">CommonParameters</span></span>
<span data-ttu-id="4d015-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d015-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d015-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d015-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d015-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d015-123">INPUTS</span></span>

## <span data-ttu-id="4d015-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d015-124">OUTPUTS</span></span>

### <span data-ttu-id="4d015-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="4d015-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="4d015-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d015-126">NOTES</span></span>

## <span data-ttu-id="4d015-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d015-127">RELATED LINKS</span></span>
