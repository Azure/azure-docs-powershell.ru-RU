---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556055"
---
# <span data-ttu-id="5c648-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="5c648-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="5c648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c648-102">SYNOPSIS</span></span>
<span data-ttu-id="5c648-103">Возвращает список всех экземпляров подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="5c648-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="5c648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c648-104">SYNTAX</span></span>

### <span data-ttu-id="5c648-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c648-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5c648-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5c648-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5c648-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c648-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5c648-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c648-108">DESCRIPTION</span></span>
<span data-ttu-id="5c648-109">Возвращает список всех экземпляров подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="5c648-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="5c648-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c648-110">EXAMPLES</span></span>

### <span data-ttu-id="5c648-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5c648-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="5c648-112">Получить весь экземпляр мультиплексора подсистемы балансировки нагрузки программного обеспечения в местоположении.</span><span class="sxs-lookup"><span data-stu-id="5c648-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="5c648-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5c648-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="5c648-114">Получение определенного экземпляра мультиплексора подсистемы балансировки нагрузки программного обеспечения на месте с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="5c648-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="5c648-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c648-115">PARAMETERS</span></span>

### <span data-ttu-id="5c648-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="5c648-116">-Filter</span></span>
<span data-ttu-id="5c648-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="5c648-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="5c648-118">-Location</span><span class="sxs-lookup"><span data-stu-id="5c648-118">-Location</span></span>
<span data-ttu-id="5c648-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="5c648-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5c648-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c648-120">-Name</span></span>
<span data-ttu-id="5c648-121">Имя экземпляра МУЛЬТИПЛЕКСОРа SLB.</span><span class="sxs-lookup"><span data-stu-id="5c648-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="5c648-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c648-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c648-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c648-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5c648-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c648-124">-ResourceId</span></span>
<span data-ttu-id="5c648-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="5c648-125">The resource id.</span></span>

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

### <span data-ttu-id="5c648-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="5c648-126">-Skip</span></span>
<span data-ttu-id="5c648-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="5c648-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5c648-128">-Top</span><span class="sxs-lookup"><span data-stu-id="5c648-128">-Top</span></span>
<span data-ttu-id="5c648-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="5c648-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5c648-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="5c648-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5c648-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c648-131">CommonParameters</span></span>
<span data-ttu-id="5c648-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c648-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c648-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c648-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c648-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c648-134">INPUTS</span></span>

## <span data-ttu-id="5c648-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c648-135">OUTPUTS</span></span>

### <span data-ttu-id="5c648-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="5c648-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="5c648-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c648-137">NOTES</span></span>

## <span data-ttu-id="5c648-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c648-138">RELATED LINKS</span></span>

