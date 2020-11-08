---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076605"
---
# <span data-ttu-id="8e26b-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="8e26b-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="8e26b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e26b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e26b-103">Возвращает список всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="8e26b-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="8e26b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e26b-104">SYNTAX</span></span>

### <span data-ttu-id="8e26b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e26b-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8e26b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8e26b-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8e26b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e26b-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8e26b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e26b-108">DESCRIPTION</span></span>
<span data-ttu-id="8e26b-109">Возвращает список всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="8e26b-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="8e26b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e26b-110">EXAMPLES</span></span>

### <span data-ttu-id="8e26b-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="8e26b-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="8e26b-112">Получение всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="8e26b-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="8e26b-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="8e26b-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="8e26b-114">Получение конкретных логических сетей в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="8e26b-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="8e26b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e26b-115">PARAMETERS</span></span>

### <span data-ttu-id="8e26b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e26b-116">-Name</span></span>
<span data-ttu-id="8e26b-117">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="8e26b-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="8e26b-118">-Location</span><span class="sxs-lookup"><span data-stu-id="8e26b-118">-Location</span></span>
<span data-ttu-id="8e26b-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e26b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8e26b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e26b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e26b-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e26b-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8e26b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e26b-122">-ResourceId</span></span>
<span data-ttu-id="8e26b-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e26b-123">The resource id.</span></span>

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

### <span data-ttu-id="8e26b-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="8e26b-124">-Filter</span></span>
<span data-ttu-id="8e26b-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="8e26b-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="8e26b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="8e26b-126">-Skip</span></span>
<span data-ttu-id="8e26b-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="8e26b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8e26b-128">-Top</span><span class="sxs-lookup"><span data-stu-id="8e26b-128">-Top</span></span>
<span data-ttu-id="8e26b-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="8e26b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8e26b-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="8e26b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8e26b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e26b-131">CommonParameters</span></span>
<span data-ttu-id="8e26b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e26b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e26b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e26b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e26b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e26b-134">INPUTS</span></span>

## <span data-ttu-id="8e26b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e26b-135">OUTPUTS</span></span>

### <span data-ttu-id="8e26b-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="8e26b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="8e26b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e26b-137">NOTES</span></span>

## <span data-ttu-id="8e26b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e26b-138">RELATED LINKS</span></span>