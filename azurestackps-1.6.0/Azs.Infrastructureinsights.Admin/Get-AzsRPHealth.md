---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731756"
---
# <span data-ttu-id="513a9-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="513a9-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="513a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="513a9-102">SYNOPSIS</span></span>
<span data-ttu-id="513a9-103">Возвращает список работоспособности каждой службы.</span><span class="sxs-lookup"><span data-stu-id="513a9-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="513a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="513a9-104">SYNTAX</span></span>

### <span data-ttu-id="513a9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="513a9-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="513a9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="513a9-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="513a9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="513a9-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="513a9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="513a9-108">DESCRIPTION</span></span>
<span data-ttu-id="513a9-109">Возвращает список работоспособности каждой службы.</span><span class="sxs-lookup"><span data-stu-id="513a9-109">Returns a list of each service's health.</span></span> <span data-ttu-id="513a9-110">Свойство AlertSummary содержит подробные сведения о предупреждениях и счетчиках ошибок.</span><span class="sxs-lookup"><span data-stu-id="513a9-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="513a9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="513a9-111">EXAMPLES</span></span>

### <span data-ttu-id="513a9-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="513a9-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="513a9-113">Возвращает список работоспособности каждой службы.</span><span class="sxs-lookup"><span data-stu-id="513a9-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="513a9-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="513a9-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="513a9-115">Возвращает состояние работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="513a9-115">Returns a service's health.</span></span>

## <span data-ttu-id="513a9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="513a9-116">PARAMETERS</span></span>

### <span data-ttu-id="513a9-117">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="513a9-117">-Filter</span></span>
<span data-ttu-id="513a9-118">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="513a9-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="513a9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="513a9-119">-Location</span></span>
<span data-ttu-id="513a9-120">Название региона</span><span class="sxs-lookup"><span data-stu-id="513a9-120">Name of the region</span></span>

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

### <span data-ttu-id="513a9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="513a9-121">-Name</span></span>
<span data-ttu-id="513a9-122">Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="513a9-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="513a9-124">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="513a9-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="513a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="513a9-125">-ResourceId</span></span>
<span data-ttu-id="513a9-126">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="513a9-126">The resource id.</span></span>

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

### <span data-ttu-id="513a9-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="513a9-127">-Skip</span></span>
<span data-ttu-id="513a9-128">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="513a9-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="513a9-129">-Top</span><span class="sxs-lookup"><span data-stu-id="513a9-129">-Top</span></span>
<span data-ttu-id="513a9-130">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="513a9-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="513a9-131">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="513a9-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="513a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513a9-132">CommonParameters</span></span>
<span data-ttu-id="513a9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="513a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513a9-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513a9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="513a9-135">INPUTS</span></span>

## <span data-ttu-id="513a9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="513a9-136">OUTPUTS</span></span>

### <span data-ttu-id="513a9-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="513a9-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="513a9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="513a9-138">NOTES</span></span>

## <span data-ttu-id="513a9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="513a9-139">RELATED LINKS</span></span>

