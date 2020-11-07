---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a81fcf688e1c269aabd64250e9b0694730edc8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907630"
---
# <span data-ttu-id="0fa02-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="0fa02-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="0fa02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fa02-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa02-103">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="0fa02-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="0fa02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fa02-104">SYNTAX</span></span>

### <span data-ttu-id="0fa02-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fa02-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0fa02-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0fa02-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="0fa02-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa02-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0fa02-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fa02-108">DESCRIPTION</span></span>
<span data-ttu-id="0fa02-109">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="0fa02-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="0fa02-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fa02-110">EXAMPLES</span></span>

### <span data-ttu-id="0fa02-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0fa02-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="0fa02-112">Получение списка всех шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="0fa02-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="0fa02-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0fa02-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="0fa02-114">Получение определенного шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="0fa02-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="0fa02-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fa02-115">PARAMETERS</span></span>

### <span data-ttu-id="0fa02-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="0fa02-116">-Filter</span></span>
<span data-ttu-id="0fa02-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="0fa02-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="0fa02-118">-Location</span><span class="sxs-lookup"><span data-stu-id="0fa02-118">-Location</span></span>
<span data-ttu-id="0fa02-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0fa02-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0fa02-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fa02-120">-Name</span></span>
<span data-ttu-id="0fa02-121">Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="0fa02-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="0fa02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa02-122">-ResourceGroupName</span></span>
<span data-ttu-id="0fa02-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fa02-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0fa02-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa02-124">-ResourceId</span></span>
<span data-ttu-id="0fa02-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0fa02-125">The resource id.</span></span>

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

### <span data-ttu-id="0fa02-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="0fa02-126">-Skip</span></span>
<span data-ttu-id="0fa02-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="0fa02-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0fa02-128">-Top</span><span class="sxs-lookup"><span data-stu-id="0fa02-128">-Top</span></span>
<span data-ttu-id="0fa02-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="0fa02-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0fa02-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="0fa02-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0fa02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa02-131">CommonParameters</span></span>
<span data-ttu-id="0fa02-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fa02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa02-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa02-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa02-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fa02-134">INPUTS</span></span>

## <span data-ttu-id="0fa02-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fa02-135">OUTPUTS</span></span>

### <span data-ttu-id="0fa02-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="0fa02-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="0fa02-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fa02-137">NOTES</span></span>

## <span data-ttu-id="0fa02-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fa02-138">RELATED LINKS</span></span>

