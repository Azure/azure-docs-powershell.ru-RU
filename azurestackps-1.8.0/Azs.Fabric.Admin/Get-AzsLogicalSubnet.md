---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908157"
---
# <span data-ttu-id="12c10-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="12c10-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="12c10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12c10-102">SYNOPSIS</span></span>
<span data-ttu-id="12c10-103">Возвращает список всех логических подсетей.</span><span class="sxs-lookup"><span data-stu-id="12c10-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="12c10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12c10-104">SYNTAX</span></span>

### <span data-ttu-id="12c10-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12c10-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="12c10-106">Получить</span><span class="sxs-lookup"><span data-stu-id="12c10-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="12c10-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="12c10-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="12c10-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12c10-108">DESCRIPTION</span></span>
<span data-ttu-id="12c10-109">Возвращает список всех логических подсетей.</span><span class="sxs-lookup"><span data-stu-id="12c10-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="12c10-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12c10-110">EXAMPLES</span></span>

### <span data-ttu-id="12c10-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="12c10-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="12c10-112">Получение списка всех логических подсетей для указанной логической сети и местоположения.</span><span class="sxs-lookup"><span data-stu-id="12c10-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="12c10-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="12c10-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="12c10-114">Получить специальную логическую подсеть для заданных логических сетей и расположений на основе имени.</span><span class="sxs-lookup"><span data-stu-id="12c10-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="12c10-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12c10-115">PARAMETERS</span></span>

### <span data-ttu-id="12c10-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12c10-116">-Name</span></span>
<span data-ttu-id="12c10-117">Имя логической подсети.</span><span class="sxs-lookup"><span data-stu-id="12c10-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="12c10-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="12c10-118">-LogicalNetwork</span></span>
<span data-ttu-id="12c10-119">Имя логической сети.</span><span class="sxs-lookup"><span data-stu-id="12c10-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="12c10-120">-Location</span><span class="sxs-lookup"><span data-stu-id="12c10-120">-Location</span></span>
<span data-ttu-id="12c10-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="12c10-121">Location of the resource.</span></span>

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

### <span data-ttu-id="12c10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12c10-122">-ResourceGroupName</span></span>
<span data-ttu-id="12c10-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12c10-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="12c10-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12c10-124">-ResourceId</span></span>
<span data-ttu-id="12c10-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="12c10-125">The resource id.</span></span>

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

### <span data-ttu-id="12c10-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="12c10-126">-Filter</span></span>
<span data-ttu-id="12c10-127">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="12c10-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="12c10-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="12c10-128">-Skip</span></span>
<span data-ttu-id="12c10-129">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="12c10-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="12c10-130">-Top</span><span class="sxs-lookup"><span data-stu-id="12c10-130">-Top</span></span>
<span data-ttu-id="12c10-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="12c10-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="12c10-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="12c10-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="12c10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c10-133">CommonParameters</span></span>
<span data-ttu-id="12c10-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12c10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c10-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c10-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c10-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12c10-136">INPUTS</span></span>

## <span data-ttu-id="12c10-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12c10-137">OUTPUTS</span></span>

### <span data-ttu-id="12c10-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="12c10-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="12c10-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="12c10-139">NOTES</span></span>

## <span data-ttu-id="12c10-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12c10-140">RELATED LINKS</span></span>
