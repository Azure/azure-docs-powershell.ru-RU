---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908142"
---
# <span data-ttu-id="b7904-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b7904-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b7904-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7904-102">SYNOPSIS</span></span>
<span data-ttu-id="b7904-103">Возвращает список всех узлов единиц масштабирования в местоположении.</span><span class="sxs-lookup"><span data-stu-id="b7904-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="b7904-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7904-104">SYNTAX</span></span>

### <span data-ttu-id="b7904-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7904-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b7904-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b7904-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b7904-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7904-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b7904-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7904-108">DESCRIPTION</span></span>
<span data-ttu-id="b7904-109">Возвращает список всех узлов единиц масштабирования в местоположении.</span><span class="sxs-lookup"><span data-stu-id="b7904-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="b7904-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7904-110">EXAMPLES</span></span>

### <span data-ttu-id="b7904-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="b7904-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="b7904-112">Получить все узлы единиц измерения шкалы в местоположении.</span><span class="sxs-lookup"><span data-stu-id="b7904-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="b7904-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="b7904-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="b7904-114">Получение определенного узла единиц измерения на месте с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="b7904-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="b7904-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7904-115">PARAMETERS</span></span>

### <span data-ttu-id="b7904-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7904-116">-Name</span></span>
<span data-ttu-id="b7904-117">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b7904-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="b7904-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b7904-118">-Location</span></span>
<span data-ttu-id="b7904-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7904-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b7904-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7904-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7904-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7904-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b7904-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7904-122">-ResourceId</span></span>
<span data-ttu-id="b7904-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7904-123">The resource id.</span></span>

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

### <span data-ttu-id="b7904-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b7904-124">-Filter</span></span>
<span data-ttu-id="b7904-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="b7904-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b7904-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="b7904-126">-Skip</span></span>
<span data-ttu-id="b7904-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="b7904-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b7904-128">-Top</span><span class="sxs-lookup"><span data-stu-id="b7904-128">-Top</span></span>
<span data-ttu-id="b7904-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="b7904-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b7904-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="b7904-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b7904-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7904-131">CommonParameters</span></span>
<span data-ttu-id="b7904-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7904-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7904-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7904-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7904-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7904-134">INPUTS</span></span>

## <span data-ttu-id="b7904-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7904-135">OUTPUTS</span></span>

### <span data-ttu-id="b7904-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b7904-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="b7904-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7904-137">NOTES</span></span>

## <span data-ttu-id="b7904-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7904-138">RELATED LINKS</span></span>
