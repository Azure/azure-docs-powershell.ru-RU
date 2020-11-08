---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076645"
---
# <span data-ttu-id="b19cc-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="b19cc-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="b19cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b19cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b19cc-103">Возвращает объекты пула шлюзов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="b19cc-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="b19cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b19cc-104">SYNTAX</span></span>

### <span data-ttu-id="b19cc-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b19cc-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b19cc-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b19cc-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b19cc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b19cc-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b19cc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19cc-108">DESCRIPTION</span></span>
<span data-ttu-id="b19cc-109">Возвращает объекты пула Edge Gateway в местоположении.</span><span class="sxs-lookup"><span data-stu-id="b19cc-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="b19cc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b19cc-110">EXAMPLES</span></span>

### <span data-ttu-id="b19cc-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="b19cc-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="b19cc-112">Получение списка всех пулов шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="b19cc-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="b19cc-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="b19cc-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="b19cc-114">Получение пула шлюзов с определенным краем.</span><span class="sxs-lookup"><span data-stu-id="b19cc-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="b19cc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b19cc-115">PARAMETERS</span></span>

### <span data-ttu-id="b19cc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b19cc-116">-Name</span></span>
<span data-ttu-id="b19cc-117">Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="b19cc-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="b19cc-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b19cc-118">-Location</span></span>
<span data-ttu-id="b19cc-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b19cc-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b19cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b19cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="b19cc-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b19cc-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b19cc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b19cc-122">-ResourceId</span></span>
<span data-ttu-id="b19cc-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b19cc-123">The resource id.</span></span>

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

### <span data-ttu-id="b19cc-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b19cc-124">-Filter</span></span>
<span data-ttu-id="b19cc-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="b19cc-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="b19cc-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="b19cc-126">-Skip</span></span>
<span data-ttu-id="b19cc-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="b19cc-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b19cc-128">-Top</span><span class="sxs-lookup"><span data-stu-id="b19cc-128">-Top</span></span>
<span data-ttu-id="b19cc-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="b19cc-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b19cc-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="b19cc-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b19cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19cc-131">CommonParameters</span></span>
<span data-ttu-id="b19cc-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b19cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19cc-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b19cc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19cc-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b19cc-134">INPUTS</span></span>

## <span data-ttu-id="b19cc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19cc-135">OUTPUTS</span></span>

### <span data-ttu-id="b19cc-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="b19cc-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="b19cc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b19cc-137">NOTES</span></span>

## <span data-ttu-id="b19cc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b19cc-138">RELATED LINKS</span></span>
