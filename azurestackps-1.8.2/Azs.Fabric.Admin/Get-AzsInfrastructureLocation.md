---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076646"
---
# <span data-ttu-id="cf7ac-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="cf7ac-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="cf7ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7ac-103">Возвращает список всех местоположений структуры.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="cf7ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf7ac-104">SYNTAX</span></span>

### <span data-ttu-id="cf7ac-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf7ac-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf7ac-106">Получить</span><span class="sxs-lookup"><span data-stu-id="cf7ac-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="cf7ac-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf7ac-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cf7ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf7ac-108">DESCRIPTION</span></span>
<span data-ttu-id="cf7ac-109">Возвращает список всех местоположений структуры.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="cf7ac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf7ac-110">EXAMPLES</span></span>

### <span data-ttu-id="cf7ac-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="cf7ac-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="cf7ac-112">Возврат списка всех структурных местоположений.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="cf7ac-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="cf7ac-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="cf7ac-114">Возвращайте расположение на основе имени.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-114">Return a location based on the name.</span></span>

## <span data-ttu-id="cf7ac-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf7ac-115">PARAMETERS</span></span>

### <span data-ttu-id="cf7ac-116">-Location</span><span class="sxs-lookup"><span data-stu-id="cf7ac-116">-Location</span></span>
<span data-ttu-id="cf7ac-117">Расположение структуры.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-117">Fabric location.</span></span>

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

### <span data-ttu-id="cf7ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf7ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="cf7ac-119">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="cf7ac-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf7ac-120">-ResourceId</span></span>
<span data-ttu-id="cf7ac-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-121">The resource id.</span></span>

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

### <span data-ttu-id="cf7ac-122">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="cf7ac-122">-Filter</span></span>
<span data-ttu-id="cf7ac-123">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="cf7ac-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="cf7ac-124">-Skip</span></span>
<span data-ttu-id="cf7ac-125">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cf7ac-126">-Top</span><span class="sxs-lookup"><span data-stu-id="cf7ac-126">-Top</span></span>
<span data-ttu-id="cf7ac-127">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cf7ac-128">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cf7ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7ac-129">CommonParameters</span></span>
<span data-ttu-id="cf7ac-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf7ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7ac-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf7ac-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7ac-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf7ac-132">INPUTS</span></span>

## <span data-ttu-id="cf7ac-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf7ac-133">OUTPUTS</span></span>

### <span data-ttu-id="cf7ac-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="cf7ac-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="cf7ac-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf7ac-135">NOTES</span></span>

## <span data-ttu-id="cf7ac-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf7ac-136">RELATED LINKS</span></span>
