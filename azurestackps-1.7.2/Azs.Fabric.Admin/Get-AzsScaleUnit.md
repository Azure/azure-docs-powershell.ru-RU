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
ms.locfileid: "93907457"
---
# <span data-ttu-id="82773-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="82773-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="82773-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82773-102">SYNOPSIS</span></span>
<span data-ttu-id="82773-103">Возвращает список всех единиц шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="82773-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="82773-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82773-104">SYNTAX</span></span>

### <span data-ttu-id="82773-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82773-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="82773-106">Получить</span><span class="sxs-lookup"><span data-stu-id="82773-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="82773-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="82773-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="82773-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82773-108">DESCRIPTION</span></span>
<span data-ttu-id="82773-109">Возвращает список всех единиц шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="82773-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="82773-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82773-110">EXAMPLES</span></span>

### <span data-ttu-id="82773-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="82773-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="82773-112">Возвращает список сведений о единицах шкалы.</span><span class="sxs-lookup"><span data-stu-id="82773-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="82773-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="82773-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="82773-114">Возвращают сведения о конкретном единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="82773-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="82773-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82773-115">PARAMETERS</span></span>

### <span data-ttu-id="82773-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="82773-116">-Filter</span></span>
<span data-ttu-id="82773-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="82773-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="82773-118">-Location</span><span class="sxs-lookup"><span data-stu-id="82773-118">-Location</span></span>
<span data-ttu-id="82773-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="82773-119">Location of the resource.</span></span>

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

### <span data-ttu-id="82773-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82773-120">-Name</span></span>
<span data-ttu-id="82773-121">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="82773-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="82773-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82773-122">-ResourceGroupName</span></span>
<span data-ttu-id="82773-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82773-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="82773-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82773-124">-ResourceId</span></span>
<span data-ttu-id="82773-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="82773-125">The resource id.</span></span>

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

### <span data-ttu-id="82773-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="82773-126">-Skip</span></span>
<span data-ttu-id="82773-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="82773-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="82773-128">-Top</span><span class="sxs-lookup"><span data-stu-id="82773-128">-Top</span></span>
<span data-ttu-id="82773-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="82773-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="82773-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="82773-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="82773-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82773-131">CommonParameters</span></span>
<span data-ttu-id="82773-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82773-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82773-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82773-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82773-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82773-134">INPUTS</span></span>

## <span data-ttu-id="82773-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82773-135">OUTPUTS</span></span>

### <span data-ttu-id="82773-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="82773-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="82773-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="82773-137">NOTES</span></span>

## <span data-ttu-id="82773-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82773-138">RELATED LINKS</span></span>

