---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076647"
---
# <span data-ttu-id="5b8d0-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="5b8d0-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="5b8d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5b8d0-103">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="5b8d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b8d0-104">SYNTAX</span></span>

### <span data-ttu-id="5b8d0-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b8d0-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5b8d0-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5b8d0-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b8d0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b8d0-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5b8d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b8d0-108">DESCRIPTION</span></span>
<span data-ttu-id="5b8d0-109">Возвращает список всех шлюзов EDGE в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="5b8d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b8d0-110">EXAMPLES</span></span>

### <span data-ttu-id="5b8d0-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="5b8d0-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="5b8d0-112">Получение списка всех шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="5b8d0-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="5b8d0-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="5b8d0-114">Получение определенного шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="5b8d0-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b8d0-115">PARAMETERS</span></span>

### <span data-ttu-id="5b8d0-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b8d0-116">-Name</span></span>
<span data-ttu-id="5b8d0-117">Имя шлюза Edge.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="5b8d0-118">-Location</span><span class="sxs-lookup"><span data-stu-id="5b8d0-118">-Location</span></span>
<span data-ttu-id="5b8d0-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5b8d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b8d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b8d0-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5b8d0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b8d0-122">-ResourceId</span></span>
<span data-ttu-id="5b8d0-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-123">The resource id.</span></span>

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

### <span data-ttu-id="5b8d0-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="5b8d0-124">-Filter</span></span>
<span data-ttu-id="5b8d0-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="5b8d0-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5b8d0-126">-Skip</span></span>
<span data-ttu-id="5b8d0-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5b8d0-128">-Top</span><span class="sxs-lookup"><span data-stu-id="5b8d0-128">-Top</span></span>
<span data-ttu-id="5b8d0-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5b8d0-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5b8d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b8d0-131">CommonParameters</span></span>
<span data-ttu-id="5b8d0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b8d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b8d0-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b8d0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b8d0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b8d0-134">INPUTS</span></span>

## <span data-ttu-id="5b8d0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b8d0-135">OUTPUTS</span></span>

### <span data-ttu-id="5b8d0-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="5b8d0-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="5b8d0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b8d0-137">NOTES</span></span>

## <span data-ttu-id="5b8d0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b8d0-138">RELATED LINKS</span></span>
