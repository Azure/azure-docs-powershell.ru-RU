---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908150"
---
# <span data-ttu-id="8f3a1-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8f3a1-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="8f3a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3a1-103">Возвращает список всех единиц шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="8f3a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f3a1-104">SYNTAX</span></span>

### <span data-ttu-id="8f3a1-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f3a1-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8f3a1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8f3a1-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8f3a1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3a1-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8f3a1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f3a1-108">DESCRIPTION</span></span>
<span data-ttu-id="8f3a1-109">Возвращает список всех единиц шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="8f3a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f3a1-110">EXAMPLES</span></span>

### <span data-ttu-id="8f3a1-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="8f3a1-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="8f3a1-112">Возвращает список сведений о единицах шкалы.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="8f3a1-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="8f3a1-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="8f3a1-114">Возвращают сведения о конкретном единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="8f3a1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f3a1-115">PARAMETERS</span></span>

### <span data-ttu-id="8f3a1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f3a1-116">-Name</span></span>
<span data-ttu-id="8f3a1-117">Название единиц измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="8f3a1-118">-Location</span><span class="sxs-lookup"><span data-stu-id="8f3a1-118">-Location</span></span>
<span data-ttu-id="8f3a1-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8f3a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f3a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f3a1-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8f3a1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f3a1-122">-ResourceId</span></span>
<span data-ttu-id="8f3a1-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-123">The resource id.</span></span>

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

### <span data-ttu-id="8f3a1-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8f3a1-124">-Filter</span></span>
<span data-ttu-id="8f3a1-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="8f3a1-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="8f3a1-126">-Skip</span></span>
<span data-ttu-id="8f3a1-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8f3a1-128">-Top</span><span class="sxs-lookup"><span data-stu-id="8f3a1-128">-Top</span></span>
<span data-ttu-id="8f3a1-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8f3a1-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8f3a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3a1-131">CommonParameters</span></span>
<span data-ttu-id="8f3a1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f3a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3a1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f3a1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3a1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f3a1-134">INPUTS</span></span>

## <span data-ttu-id="8f3a1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f3a1-135">OUTPUTS</span></span>

### <span data-ttu-id="8f3a1-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8f3a1-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="8f3a1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f3a1-137">NOTES</span></span>

## <span data-ttu-id="8f3a1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f3a1-138">RELATED LINKS</span></span>
