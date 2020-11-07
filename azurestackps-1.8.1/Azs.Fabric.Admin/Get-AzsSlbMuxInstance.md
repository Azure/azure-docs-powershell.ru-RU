---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908674"
---
# <span data-ttu-id="4e192-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="4e192-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="4e192-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e192-102">SYNOPSIS</span></span>
<span data-ttu-id="4e192-103">Возвращает список всех экземпляров подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="4e192-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="4e192-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e192-104">SYNTAX</span></span>

### <span data-ttu-id="4e192-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e192-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4e192-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4e192-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4e192-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e192-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4e192-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e192-108">DESCRIPTION</span></span>
<span data-ttu-id="4e192-109">Возвращает список всех экземпляров подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="4e192-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="4e192-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e192-110">EXAMPLES</span></span>

### <span data-ttu-id="4e192-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="4e192-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="4e192-112">Получить весь экземпляр мультиплексора подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="4e192-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="4e192-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="4e192-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="4e192-114">Получение определенного экземпляра мультиплексора подсистемы балансировки нагрузки программного обеспечения на месте с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="4e192-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="4e192-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e192-115">PARAMETERS</span></span>

### <span data-ttu-id="4e192-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e192-116">-Name</span></span>
<span data-ttu-id="4e192-117">Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="4e192-117">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="4e192-118">-Location</span><span class="sxs-lookup"><span data-stu-id="4e192-118">-Location</span></span>
<span data-ttu-id="4e192-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e192-119">Location of the resource.</span></span>

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

### <span data-ttu-id="4e192-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e192-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e192-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e192-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4e192-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e192-122">-ResourceId</span></span>
<span data-ttu-id="4e192-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e192-123">The resource id.</span></span>

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

### <span data-ttu-id="4e192-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="4e192-124">-Filter</span></span>
<span data-ttu-id="4e192-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="4e192-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="4e192-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="4e192-126">-Skip</span></span>
<span data-ttu-id="4e192-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="4e192-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4e192-128">-Top</span><span class="sxs-lookup"><span data-stu-id="4e192-128">-Top</span></span>
<span data-ttu-id="4e192-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="4e192-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4e192-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="4e192-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4e192-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e192-131">CommonParameters</span></span>
<span data-ttu-id="4e192-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e192-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e192-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e192-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e192-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e192-134">INPUTS</span></span>

## <span data-ttu-id="4e192-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e192-135">OUTPUTS</span></span>

### <span data-ttu-id="4e192-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="4e192-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="4e192-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e192-137">NOTES</span></span>

## <span data-ttu-id="4e192-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e192-138">RELATED LINKS</span></span>
