---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908193"
---
# <span data-ttu-id="3ca8a-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="3ca8a-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="3ca8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ca8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca8a-103">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="3ca8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ca8a-104">SYNTAX</span></span>

### <span data-ttu-id="3ca8a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ca8a-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3ca8a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="3ca8a-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ca8a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca8a-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3ca8a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ca8a-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca8a-109">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="3ca8a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ca8a-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca8a-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="3ca8a-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="3ca8a-112">Получение списка всех шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="3ca8a-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="3ca8a-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="3ca8a-114">Получение определенного шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="3ca8a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ca8a-115">PARAMETERS</span></span>

### <span data-ttu-id="3ca8a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ca8a-116">-Name</span></span>
<span data-ttu-id="3ca8a-117">Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="3ca8a-118">-Location</span><span class="sxs-lookup"><span data-stu-id="3ca8a-118">-Location</span></span>
<span data-ttu-id="3ca8a-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="3ca8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="3ca8a-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3ca8a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca8a-122">-ResourceId</span></span>
<span data-ttu-id="3ca8a-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-123">The resource id.</span></span>

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

### <span data-ttu-id="3ca8a-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="3ca8a-124">-Filter</span></span>
<span data-ttu-id="3ca8a-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="3ca8a-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="3ca8a-126">-Skip</span></span>
<span data-ttu-id="3ca8a-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3ca8a-128">-Top</span><span class="sxs-lookup"><span data-stu-id="3ca8a-128">-Top</span></span>
<span data-ttu-id="3ca8a-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3ca8a-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3ca8a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca8a-131">CommonParameters</span></span>
<span data-ttu-id="3ca8a-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ca8a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca8a-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca8a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca8a-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ca8a-134">INPUTS</span></span>

## <span data-ttu-id="3ca8a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ca8a-135">OUTPUTS</span></span>

### <span data-ttu-id="3ca8a-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="3ca8a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="3ca8a-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ca8a-137">NOTES</span></span>

## <span data-ttu-id="3ca8a-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ca8a-138">RELATED LINKS</span></span>
