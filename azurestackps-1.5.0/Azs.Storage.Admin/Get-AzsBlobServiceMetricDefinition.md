---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b43acb45bc5b606303cbd33c20f0975919bb6b59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556403"
---
# <span data-ttu-id="d0294-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="d0294-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="d0294-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0294-102">SYNOPSIS</span></span>
<span data-ttu-id="d0294-103">Возвращает список определений метрик для службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="d0294-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="d0294-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0294-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d0294-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0294-105">DESCRIPTION</span></span>
<span data-ttu-id="d0294-106">Возвращает список определений метрик для службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="d0294-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="d0294-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0294-107">EXAMPLES</span></span>

### <span data-ttu-id="d0294-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0294-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="d0294-109">Получите список определений метрик для службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="d0294-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="d0294-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0294-110">PARAMETERS</span></span>

### <span data-ttu-id="d0294-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="d0294-111">-FarmName</span></span>
<span data-ttu-id="d0294-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="d0294-112">Farm Id.</span></span>

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

### <span data-ttu-id="d0294-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0294-113">-ResourceGroupName</span></span>
<span data-ttu-id="d0294-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0294-114">Resource group name.</span></span>

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

### <span data-ttu-id="d0294-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="d0294-115">-Skip</span></span>
<span data-ttu-id="d0294-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="d0294-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="d0294-117">-Top</span><span class="sxs-lookup"><span data-stu-id="d0294-117">-Top</span></span>
<span data-ttu-id="d0294-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="d0294-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d0294-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="d0294-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="d0294-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0294-120">CommonParameters</span></span>
<span data-ttu-id="d0294-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0294-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0294-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0294-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0294-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0294-123">INPUTS</span></span>

## <span data-ttu-id="d0294-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0294-124">OUTPUTS</span></span>

### <span data-ttu-id="d0294-125">Microsoft. AzureStack. Management. Storage. admin. Models. MetricDefinition</span><span class="sxs-lookup"><span data-stu-id="d0294-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="d0294-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0294-126">NOTES</span></span>

## <span data-ttu-id="d0294-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0294-127">RELATED LINKS</span></span>

