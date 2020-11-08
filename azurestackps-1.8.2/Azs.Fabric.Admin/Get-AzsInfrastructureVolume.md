---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077130"
---
# <span data-ttu-id="6b47a-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="6b47a-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="6b47a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b47a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b47a-103">Возвращает список всех томов хранилища в местоположении.</span><span class="sxs-lookup"><span data-stu-id="6b47a-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="6b47a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b47a-104">SYNTAX</span></span>

### <span data-ttu-id="6b47a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b47a-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6b47a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6b47a-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b47a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b47a-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6b47a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b47a-108">DESCRIPTION</span></span>
<span data-ttu-id="6b47a-109">Возвращает список всех томов хранилища в местоположении.</span><span class="sxs-lookup"><span data-stu-id="6b47a-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="6b47a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b47a-110">EXAMPLES</span></span>

### <span data-ttu-id="6b47a-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="6b47a-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="6b47a-112">Получение списка всех томов хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="6b47a-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="6b47a-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="6b47a-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="6b47a-114">Получение тома хранилища по имени в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="6b47a-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="6b47a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b47a-115">PARAMETERS</span></span>

### <span data-ttu-id="6b47a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b47a-116">-Name</span></span>
<span data-ttu-id="6b47a-117">Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b47a-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="6b47a-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="6b47a-118">-StoragePool</span></span>
<span data-ttu-id="6b47a-119">Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="6b47a-119">Storage pool name.</span></span>

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

### <span data-ttu-id="6b47a-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="6b47a-120">-StorageSystem</span></span>
<span data-ttu-id="6b47a-121">Представление ресурса системы хранилища.</span><span class="sxs-lookup"><span data-stu-id="6b47a-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="6b47a-122">-Location</span><span class="sxs-lookup"><span data-stu-id="6b47a-122">-Location</span></span>
<span data-ttu-id="6b47a-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b47a-123">Location of the resource.</span></span>

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

### <span data-ttu-id="6b47a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b47a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b47a-125">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b47a-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6b47a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b47a-126">-ResourceId</span></span>
<span data-ttu-id="6b47a-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b47a-127">The resource id.</span></span>

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

### <span data-ttu-id="6b47a-128">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="6b47a-128">-Filter</span></span>
<span data-ttu-id="6b47a-129">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="6b47a-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="6b47a-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="6b47a-130">-Skip</span></span>
<span data-ttu-id="6b47a-131">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="6b47a-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6b47a-132">-Top</span><span class="sxs-lookup"><span data-stu-id="6b47a-132">-Top</span></span>
<span data-ttu-id="6b47a-133">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="6b47a-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6b47a-134">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="6b47a-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6b47a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b47a-135">CommonParameters</span></span>
<span data-ttu-id="6b47a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b47a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b47a-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b47a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b47a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b47a-138">INPUTS</span></span>

## <span data-ttu-id="6b47a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b47a-139">OUTPUTS</span></span>

### <span data-ttu-id="6b47a-140">Microsoft. AzureStack. Management. Fabric. admin. Model. Volume</span><span class="sxs-lookup"><span data-stu-id="6b47a-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="6b47a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b47a-141">NOTES</span></span>

## <span data-ttu-id="6b47a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b47a-142">RELATED LINKS</span></span>
