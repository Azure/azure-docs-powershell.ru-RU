---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909110"
---
# <span data-ttu-id="7f01f-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="7f01f-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="7f01f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f01f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f01f-103">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="7f01f-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="7f01f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f01f-104">SYNTAX</span></span>

### <span data-ttu-id="7f01f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f01f-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f01f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7f01f-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="7f01f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f01f-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7f01f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f01f-108">DESCRIPTION</span></span>
<span data-ttu-id="7f01f-109">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="7f01f-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="7f01f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f01f-110">EXAMPLES</span></span>

### <span data-ttu-id="7f01f-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="7f01f-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="7f01f-112">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="7f01f-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="7f01f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f01f-113">PARAMETERS</span></span>

### <span data-ttu-id="7f01f-114">-Location</span><span class="sxs-lookup"><span data-stu-id="7f01f-114">-Location</span></span>
<span data-ttu-id="7f01f-115">Название региона</span><span class="sxs-lookup"><span data-stu-id="7f01f-115">Name of the region</span></span>

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

### <span data-ttu-id="7f01f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f01f-116">-ResourceGroupName</span></span>
<span data-ttu-id="7f01f-117">Имя группы ресурсов (необязательно).</span><span class="sxs-lookup"><span data-stu-id="7f01f-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="7f01f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f01f-118">-ResourceId</span></span>
<span data-ttu-id="7f01f-119">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7f01f-119">The resource id.</span></span>

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

### <span data-ttu-id="7f01f-120">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="7f01f-120">-Filter</span></span>
<span data-ttu-id="7f01f-121">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="7f01f-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="7f01f-122">-Top</span><span class="sxs-lookup"><span data-stu-id="7f01f-122">-Top</span></span>
<span data-ttu-id="7f01f-123">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="7f01f-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7f01f-124">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="7f01f-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7f01f-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="7f01f-125">-Skip</span></span>
<span data-ttu-id="7f01f-126">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="7f01f-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7f01f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f01f-127">CommonParameters</span></span>
<span data-ttu-id="7f01f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f01f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f01f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f01f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f01f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f01f-130">INPUTS</span></span>

## <span data-ttu-id="7f01f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f01f-131">OUTPUTS</span></span>

### <span data-ttu-id="7f01f-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="7f01f-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="7f01f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f01f-133">NOTES</span></span>

## <span data-ttu-id="7f01f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f01f-134">RELATED LINKS</span></span>
