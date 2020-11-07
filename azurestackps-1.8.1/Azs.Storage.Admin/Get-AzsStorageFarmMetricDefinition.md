---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc0e931c97a60d35db48dbceb1446ff944ee689
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908958"
---
# <span data-ttu-id="a6fa9-101">Get-AzsStorageFarmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a6fa9-101">Get-AzsStorageFarmMetricDefinition</span></span>

## <span data-ttu-id="a6fa9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fa9-103">Возвращает список определений метрик для фермы хранилищ.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-103">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="a6fa9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6fa9-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a6fa9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="a6fa9-106">Возвращает список определений метрик для фермы хранилищ.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-106">Returns a list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="a6fa9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="a6fa9-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="a6fa9-108">EXAMPLE 1</span></span>
```
Get-AzsStorageFarmMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="a6fa9-109">Получите список определений метрик для фермы хранилищ.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-109">Get the list of metric definitions for a storage farm.</span></span>

## <span data-ttu-id="a6fa9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="a6fa9-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a6fa9-111">-FarmName</span></span>
<span data-ttu-id="a6fa9-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-112">Farm Id.</span></span>

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

### <span data-ttu-id="a6fa9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6fa9-113">-ResourceGroupName</span></span>
<span data-ttu-id="a6fa9-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-114">Resource group name.</span></span>

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

### <span data-ttu-id="a6fa9-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="a6fa9-115">-Skip</span></span>
<span data-ttu-id="a6fa9-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a6fa9-117">-Top</span><span class="sxs-lookup"><span data-stu-id="a6fa9-117">-Top</span></span>
<span data-ttu-id="a6fa9-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a6fa9-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a6fa9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fa9-120">CommonParameters</span></span>
<span data-ttu-id="a6fa9-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6fa9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fa9-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6fa9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fa9-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6fa9-123">INPUTS</span></span>

## <span data-ttu-id="a6fa9-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6fa9-124">OUTPUTS</span></span>

### <span data-ttu-id="a6fa9-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a6fa9-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="a6fa9-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6fa9-126">NOTES</span></span>

## <span data-ttu-id="a6fa9-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6fa9-127">RELATED LINKS</span></span>
