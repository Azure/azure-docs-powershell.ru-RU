---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908158"
---
# <span data-ttu-id="682f2-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="682f2-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="682f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="682f2-102">SYNOPSIS</span></span>
<span data-ttu-id="682f2-103">Возвращает список всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="682f2-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="682f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="682f2-104">SYNTAX</span></span>

### <span data-ttu-id="682f2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="682f2-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="682f2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="682f2-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="682f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="682f2-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="682f2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="682f2-108">DESCRIPTION</span></span>
<span data-ttu-id="682f2-109">Возвращает список всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="682f2-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="682f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="682f2-110">EXAMPLES</span></span>

### <span data-ttu-id="682f2-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="682f2-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="682f2-112">Получение всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="682f2-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="682f2-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="682f2-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="682f2-114">Получение конкретных логических сетей в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="682f2-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="682f2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="682f2-115">PARAMETERS</span></span>

### <span data-ttu-id="682f2-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="682f2-116">-Name</span></span>
<span data-ttu-id="682f2-117">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="682f2-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="682f2-118">-Location</span><span class="sxs-lookup"><span data-stu-id="682f2-118">-Location</span></span>
<span data-ttu-id="682f2-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="682f2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="682f2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="682f2-120">-ResourceGroupName</span></span>
<span data-ttu-id="682f2-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="682f2-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="682f2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="682f2-122">-ResourceId</span></span>
<span data-ttu-id="682f2-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="682f2-123">The resource id.</span></span>

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

### <span data-ttu-id="682f2-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="682f2-124">-Filter</span></span>
<span data-ttu-id="682f2-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="682f2-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="682f2-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="682f2-126">-Skip</span></span>
<span data-ttu-id="682f2-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="682f2-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="682f2-128">-Top</span><span class="sxs-lookup"><span data-stu-id="682f2-128">-Top</span></span>
<span data-ttu-id="682f2-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="682f2-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="682f2-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="682f2-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="682f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682f2-131">CommonParameters</span></span>
<span data-ttu-id="682f2-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="682f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682f2-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="682f2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682f2-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="682f2-134">INPUTS</span></span>

## <span data-ttu-id="682f2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="682f2-135">OUTPUTS</span></span>

### <span data-ttu-id="682f2-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="682f2-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="682f2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="682f2-137">NOTES</span></span>

## <span data-ttu-id="682f2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="682f2-138">RELATED LINKS</span></span>
