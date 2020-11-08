---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076858"
---
# <span data-ttu-id="77772-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="77772-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="77772-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77772-102">SYNOPSIS</span></span>
<span data-ttu-id="77772-103">Возвращает список всех логических подсетей.</span><span class="sxs-lookup"><span data-stu-id="77772-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="77772-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77772-104">SYNTAX</span></span>

### <span data-ttu-id="77772-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77772-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="77772-106">Получить</span><span class="sxs-lookup"><span data-stu-id="77772-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="77772-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="77772-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="77772-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77772-108">DESCRIPTION</span></span>
<span data-ttu-id="77772-109">Возвращает список всех логических подсетей.</span><span class="sxs-lookup"><span data-stu-id="77772-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="77772-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77772-110">EXAMPLES</span></span>

### <span data-ttu-id="77772-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="77772-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="77772-112">Получение списка всех логических подсетей для указанной логической сети и местоположения.</span><span class="sxs-lookup"><span data-stu-id="77772-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="77772-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="77772-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="77772-114">Получить специальную логическую подсеть для заданных логических сетей и расположений на основе имени.</span><span class="sxs-lookup"><span data-stu-id="77772-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="77772-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77772-115">PARAMETERS</span></span>

### <span data-ttu-id="77772-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77772-116">-Name</span></span>
<span data-ttu-id="77772-117">Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="77772-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="77772-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="77772-118">-LogicalNetwork</span></span>
<span data-ttu-id="77772-119">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="77772-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="77772-120">-Location</span><span class="sxs-lookup"><span data-stu-id="77772-120">-Location</span></span>
<span data-ttu-id="77772-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="77772-121">Location of the resource.</span></span>

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

### <span data-ttu-id="77772-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77772-122">-ResourceGroupName</span></span>
<span data-ttu-id="77772-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77772-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="77772-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77772-124">-ResourceId</span></span>
<span data-ttu-id="77772-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="77772-125">The resource id.</span></span>

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

### <span data-ttu-id="77772-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="77772-126">-Filter</span></span>
<span data-ttu-id="77772-127">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="77772-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="77772-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="77772-128">-Skip</span></span>
<span data-ttu-id="77772-129">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="77772-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="77772-130">-Top</span><span class="sxs-lookup"><span data-stu-id="77772-130">-Top</span></span>
<span data-ttu-id="77772-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="77772-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="77772-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="77772-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="77772-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77772-133">CommonParameters</span></span>
<span data-ttu-id="77772-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77772-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77772-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77772-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77772-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77772-136">INPUTS</span></span>

## <span data-ttu-id="77772-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77772-137">OUTPUTS</span></span>

### <span data-ttu-id="77772-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="77772-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="77772-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="77772-139">NOTES</span></span>

## <span data-ttu-id="77772-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77772-140">RELATED LINKS</span></span>