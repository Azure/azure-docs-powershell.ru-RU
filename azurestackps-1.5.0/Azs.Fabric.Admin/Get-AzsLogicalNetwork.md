---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdf0c09e087779e9a08161f2af6f9070f193c31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556407"
---
# <span data-ttu-id="147a3-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="147a3-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="147a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="147a3-102">SYNOPSIS</span></span>
<span data-ttu-id="147a3-103">Возвращает список всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="147a3-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="147a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="147a3-104">SYNTAX</span></span>

### <span data-ttu-id="147a3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="147a3-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="147a3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="147a3-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="147a3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="147a3-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="147a3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="147a3-108">DESCRIPTION</span></span>
<span data-ttu-id="147a3-109">Возвращает список всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="147a3-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="147a3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="147a3-110">EXAMPLES</span></span>

### <span data-ttu-id="147a3-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="147a3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="147a3-112">Получение всех логических сетей в расположении.</span><span class="sxs-lookup"><span data-stu-id="147a3-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="147a3-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="147a3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="147a3-114">Получение конкретных логических сетей в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="147a3-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="147a3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="147a3-115">PARAMETERS</span></span>

### <span data-ttu-id="147a3-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="147a3-116">-Filter</span></span>
<span data-ttu-id="147a3-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="147a3-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="147a3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="147a3-118">-Location</span></span>
<span data-ttu-id="147a3-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="147a3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="147a3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="147a3-120">-Name</span></span>
<span data-ttu-id="147a3-121">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="147a3-121">Name of the logical network.</span></span>

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

### <span data-ttu-id="147a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="147a3-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="147a3-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="147a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="147a3-124">-ResourceId</span></span>
<span data-ttu-id="147a3-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="147a3-125">The resource id.</span></span>

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

### <span data-ttu-id="147a3-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="147a3-126">-Skip</span></span>
<span data-ttu-id="147a3-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="147a3-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="147a3-128">-Top</span><span class="sxs-lookup"><span data-stu-id="147a3-128">-Top</span></span>
<span data-ttu-id="147a3-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="147a3-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="147a3-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="147a3-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="147a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147a3-131">CommonParameters</span></span>
<span data-ttu-id="147a3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="147a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147a3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="147a3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147a3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="147a3-134">INPUTS</span></span>

## <span data-ttu-id="147a3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="147a3-135">OUTPUTS</span></span>

### <span data-ttu-id="147a3-136">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="147a3-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="147a3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="147a3-137">NOTES</span></span>

## <span data-ttu-id="147a3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="147a3-138">RELATED LINKS</span></span>

