---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556052"
---
# <span data-ttu-id="a412c-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a412c-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="a412c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a412c-102">SYNOPSIS</span></span>
<span data-ttu-id="a412c-103">Возвращает список всех единиц шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="a412c-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="a412c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a412c-104">SYNTAX</span></span>

### <span data-ttu-id="a412c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a412c-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a412c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a412c-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a412c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a412c-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a412c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a412c-108">DESCRIPTION</span></span>
<span data-ttu-id="a412c-109">Возвращает список всех единиц шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="a412c-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="a412c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a412c-110">EXAMPLES</span></span>

### <span data-ttu-id="a412c-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a412c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="a412c-112">Возвращает список сведений о единицах шкалы.</span><span class="sxs-lookup"><span data-stu-id="a412c-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="a412c-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a412c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="a412c-114">Возвращают сведения о конкретном единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="a412c-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="a412c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a412c-115">PARAMETERS</span></span>

### <span data-ttu-id="a412c-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a412c-116">-Filter</span></span>
<span data-ttu-id="a412c-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a412c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a412c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="a412c-118">-Location</span></span>
<span data-ttu-id="a412c-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a412c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a412c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a412c-120">-Name</span></span>
<span data-ttu-id="a412c-121">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="a412c-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="a412c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a412c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a412c-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a412c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a412c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a412c-124">-ResourceId</span></span>
<span data-ttu-id="a412c-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a412c-125">The resource id.</span></span>

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

### <span data-ttu-id="a412c-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a412c-126">-Skip</span></span>
<span data-ttu-id="a412c-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="a412c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a412c-128">-Top</span><span class="sxs-lookup"><span data-stu-id="a412c-128">-Top</span></span>
<span data-ttu-id="a412c-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a412c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a412c-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="a412c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a412c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a412c-131">CommonParameters</span></span>
<span data-ttu-id="a412c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a412c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a412c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a412c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a412c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a412c-134">INPUTS</span></span>

## <span data-ttu-id="a412c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a412c-135">OUTPUTS</span></span>

### <span data-ttu-id="a412c-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="a412c-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="a412c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a412c-137">NOTES</span></span>

## <span data-ttu-id="a412c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a412c-138">RELATED LINKS</span></span>

