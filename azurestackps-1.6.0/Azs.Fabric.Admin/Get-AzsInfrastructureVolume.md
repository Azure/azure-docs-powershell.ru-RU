---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdb6542f9e7bfd594130374d5d72fed8b26596e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556012"
---
# <span data-ttu-id="58da9-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="58da9-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="58da9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58da9-102">SYNOPSIS</span></span>
<span data-ttu-id="58da9-103">Возвращает список всех томов хранилища в местоположении.</span><span class="sxs-lookup"><span data-stu-id="58da9-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="58da9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58da9-104">SYNTAX</span></span>

### <span data-ttu-id="58da9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58da9-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="58da9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="58da9-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="58da9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="58da9-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="58da9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58da9-108">DESCRIPTION</span></span>
<span data-ttu-id="58da9-109">Возвращает список всех томов хранилища в местоположении.</span><span class="sxs-lookup"><span data-stu-id="58da9-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="58da9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58da9-110">EXAMPLES</span></span>

### <span data-ttu-id="58da9-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="58da9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="58da9-112">Получение списка всех томов хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="58da9-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="58da9-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="58da9-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="58da9-114">Получение тома хранилища по имени в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="58da9-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="58da9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58da9-115">PARAMETERS</span></span>

### <span data-ttu-id="58da9-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="58da9-116">-Filter</span></span>
<span data-ttu-id="58da9-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="58da9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="58da9-118">-Location</span><span class="sxs-lookup"><span data-stu-id="58da9-118">-Location</span></span>
<span data-ttu-id="58da9-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="58da9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="58da9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58da9-120">-Name</span></span>
<span data-ttu-id="58da9-121">Имя тома хранилища.</span><span class="sxs-lookup"><span data-stu-id="58da9-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="58da9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58da9-122">-ResourceGroupName</span></span>
<span data-ttu-id="58da9-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58da9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="58da9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58da9-124">-ResourceId</span></span>
<span data-ttu-id="58da9-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="58da9-125">The resource id.</span></span>

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

### <span data-ttu-id="58da9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="58da9-126">-Skip</span></span>
<span data-ttu-id="58da9-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="58da9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="58da9-128">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="58da9-128">-StoragePool</span></span>
<span data-ttu-id="58da9-129">Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="58da9-129">Storage pool name.</span></span>

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

### <span data-ttu-id="58da9-130">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="58da9-130">-StorageSystem</span></span>
<span data-ttu-id="58da9-131">Система хранения, в которой находится том инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="58da9-131">Storage system in which the infrastructure volume is located.</span></span>

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

### <span data-ttu-id="58da9-132">-Top</span><span class="sxs-lookup"><span data-stu-id="58da9-132">-Top</span></span>
<span data-ttu-id="58da9-133">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="58da9-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="58da9-134">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="58da9-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="58da9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58da9-135">CommonParameters</span></span>
<span data-ttu-id="58da9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58da9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58da9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58da9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58da9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58da9-138">INPUTS</span></span>

## <span data-ttu-id="58da9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58da9-139">OUTPUTS</span></span>

### <span data-ttu-id="58da9-140">Microsoft. AzureStack. Management. Fabric. admin. Model. Volume</span><span class="sxs-lookup"><span data-stu-id="58da9-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="58da9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="58da9-141">NOTES</span></span>

## <span data-ttu-id="58da9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58da9-142">RELATED LINKS</span></span>

