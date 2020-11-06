---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556212"
---
# <span data-ttu-id="a7b6d-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="a7b6d-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="a7b6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b6d-103">Возвращает список всех логических подсетей.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="a7b6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7b6d-104">SYNTAX</span></span>

### <span data-ttu-id="a7b6d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7b6d-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a7b6d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a7b6d-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7b6d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7b6d-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a7b6d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7b6d-108">DESCRIPTION</span></span>
<span data-ttu-id="a7b6d-109">Возвращает список всех логических подсетей.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="a7b6d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7b6d-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b6d-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7b6d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="a7b6d-112">Получение списка всех логических подсетей для указанной логической сети и местоположения.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="a7b6d-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7b6d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="a7b6d-114">Получить специальную логическую подсеть для заданных логических сетей и расположений на основе имени.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="a7b6d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7b6d-115">PARAMETERS</span></span>

### <span data-ttu-id="a7b6d-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a7b6d-116">-Filter</span></span>
<span data-ttu-id="a7b6d-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="a7b6d-118">-Location</span><span class="sxs-lookup"><span data-stu-id="a7b6d-118">-Location</span></span>
<span data-ttu-id="a7b6d-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a7b6d-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="a7b6d-120">-LogicalNetwork</span></span>
<span data-ttu-id="a7b6d-121">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b6d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7b6d-122">-Name</span></span>
<span data-ttu-id="a7b6d-123">Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7b6d-125">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a7b6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7b6d-126">-ResourceId</span></span>
<span data-ttu-id="a7b6d-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-127">The resource id.</span></span>

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

### <span data-ttu-id="a7b6d-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="a7b6d-128">-Skip</span></span>
<span data-ttu-id="a7b6d-129">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a7b6d-130">-Top</span><span class="sxs-lookup"><span data-stu-id="a7b6d-130">-Top</span></span>
<span data-ttu-id="a7b6d-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a7b6d-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a7b6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b6d-133">CommonParameters</span></span>
<span data-ttu-id="a7b6d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7b6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b6d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7b6d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b6d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7b6d-136">INPUTS</span></span>

## <span data-ttu-id="a7b6d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7b6d-137">OUTPUTS</span></span>

### <span data-ttu-id="a7b6d-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="a7b6d-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="a7b6d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7b6d-139">NOTES</span></span>

## <span data-ttu-id="a7b6d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7b6d-140">RELATED LINKS</span></span>

