---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077110"
---
# <span data-ttu-id="89ee4-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="89ee4-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="89ee4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="89ee4-103">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="89ee4-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="89ee4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89ee4-104">SYNTAX</span></span>

### <span data-ttu-id="89ee4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89ee4-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="89ee4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="89ee4-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="89ee4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ee4-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="89ee4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ee4-108">DESCRIPTION</span></span>
<span data-ttu-id="89ee4-109">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="89ee4-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="89ee4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89ee4-110">EXAMPLES</span></span>

### <span data-ttu-id="89ee4-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="89ee4-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="89ee4-112">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="89ee4-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="89ee4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89ee4-113">PARAMETERS</span></span>

### <span data-ttu-id="89ee4-114">-Location</span><span class="sxs-lookup"><span data-stu-id="89ee4-114">-Location</span></span>
<span data-ttu-id="89ee4-115">Название региона</span><span class="sxs-lookup"><span data-stu-id="89ee4-115">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ee4-116">-ResourceGroupName</span></span>
<span data-ttu-id="89ee4-117">Имя группы ресурсов (необязательно).</span><span class="sxs-lookup"><span data-stu-id="89ee4-117">Resource group name, optional.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ee4-118">-ResourceId</span></span>
<span data-ttu-id="89ee4-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="89ee4-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ee4-120">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="89ee4-120">-Filter</span></span>
<span data-ttu-id="89ee4-121">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="89ee4-121">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee4-122">-Top</span><span class="sxs-lookup"><span data-stu-id="89ee4-122">-Top</span></span>
<span data-ttu-id="89ee4-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="89ee4-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="89ee4-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="89ee4-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee4-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="89ee4-125">-Skip</span></span>
<span data-ttu-id="89ee4-126">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="89ee4-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ee4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ee4-127">CommonParameters</span></span>
<span data-ttu-id="89ee4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89ee4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ee4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ee4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ee4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89ee4-130">INPUTS</span></span>

## <span data-ttu-id="89ee4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ee4-131">OUTPUTS</span></span>

### <span data-ttu-id="89ee4-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="89ee4-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="89ee4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="89ee4-133">NOTES</span></span>

## <span data-ttu-id="89ee4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ee4-134">RELATED LINKS</span></span>
