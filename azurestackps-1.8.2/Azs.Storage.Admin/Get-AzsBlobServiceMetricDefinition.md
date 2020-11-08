---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2e80ea57424b350a1255a2a19c7bea8c22c34c71
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077053"
---
# <span data-ttu-id="940bc-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="940bc-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="940bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="940bc-102">SYNOPSIS</span></span>
<span data-ttu-id="940bc-103">Возвращает список определений метрик для службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="940bc-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="940bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="940bc-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="940bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="940bc-105">DESCRIPTION</span></span>
<span data-ttu-id="940bc-106">Возвращает список определений метрик для службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="940bc-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="940bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="940bc-107">EXAMPLES</span></span>

### <span data-ttu-id="940bc-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="940bc-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="940bc-109">Получите список определений метрик для службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="940bc-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="940bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="940bc-110">PARAMETERS</span></span>

### <span data-ttu-id="940bc-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="940bc-111">-FarmName</span></span>
<span data-ttu-id="940bc-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="940bc-112">Farm Id.</span></span>

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

### <span data-ttu-id="940bc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940bc-113">-ResourceGroupName</span></span>
<span data-ttu-id="940bc-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="940bc-114">Resource group name.</span></span>

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

### <span data-ttu-id="940bc-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="940bc-115">-Skip</span></span>
<span data-ttu-id="940bc-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="940bc-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="940bc-117">-Top</span><span class="sxs-lookup"><span data-stu-id="940bc-117">-Top</span></span>
<span data-ttu-id="940bc-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="940bc-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="940bc-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="940bc-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="940bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940bc-120">CommonParameters</span></span>
<span data-ttu-id="940bc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="940bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940bc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940bc-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940bc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="940bc-123">INPUTS</span></span>

## <span data-ttu-id="940bc-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="940bc-124">OUTPUTS</span></span>

### <span data-ttu-id="940bc-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="940bc-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="940bc-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="940bc-126">NOTES</span></span>

## <span data-ttu-id="940bc-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="940bc-127">RELATED LINKS</span></span>
