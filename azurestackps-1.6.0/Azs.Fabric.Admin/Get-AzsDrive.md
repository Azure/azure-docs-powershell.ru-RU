---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555184"
---
# <span data-ttu-id="b9969-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="b9969-101">Get-AzsDrive</span></span>

## <span data-ttu-id="b9969-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9969-102">SYNOPSIS</span></span>
<span data-ttu-id="b9969-103">Возвращает список всех дисков хранилища для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="b9969-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="b9969-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9969-104">SYNTAX</span></span>

### <span data-ttu-id="b9969-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9969-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b9969-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b9969-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9969-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9969-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b9969-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9969-108">DESCRIPTION</span></span>
<span data-ttu-id="b9969-109">Возвращает список всех дисков хранилища для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="b9969-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="b9969-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9969-110">EXAMPLES</span></span>

### <span data-ttu-id="b9969-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9969-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="b9969-112">Получение списка всех дисков хранилища для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="b9969-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="b9969-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9969-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="b9969-114">Получение имени диска хранилища для данного кластера.</span><span class="sxs-lookup"><span data-stu-id="b9969-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="b9969-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9969-115">PARAMETERS</span></span>

### <span data-ttu-id="b9969-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="b9969-116">-Filter</span></span>
<span data-ttu-id="b9969-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="b9969-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b9969-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b9969-118">-Location</span></span>
<span data-ttu-id="b9969-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9969-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b9969-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9969-120">-Name</span></span>
<span data-ttu-id="b9969-121">Имя диска хранилища.</span><span class="sxs-lookup"><span data-stu-id="b9969-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="b9969-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9969-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9969-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9969-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b9969-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9969-124">-ResourceId</span></span>
<span data-ttu-id="b9969-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9969-125">The resource id.</span></span>

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

### <span data-ttu-id="b9969-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="b9969-126">-ScaleUnit</span></span>
<span data-ttu-id="b9969-127">Название единицы измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="b9969-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="b9969-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="b9969-128">-StorageSubSystem</span></span>
<span data-ttu-id="b9969-129">Подсистема хранилища, в которой находится диск.</span><span class="sxs-lookup"><span data-stu-id="b9969-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="b9969-130">-Top</span><span class="sxs-lookup"><span data-stu-id="b9969-130">-Top</span></span>
<span data-ttu-id="b9969-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="b9969-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b9969-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="b9969-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b9969-133">-Skip</span><span class="sxs-lookup"><span data-stu-id="b9969-133">-Skip</span></span>
<span data-ttu-id="b9969-134">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="b9969-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b9969-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9969-135">CommonParameters</span></span>
<span data-ttu-id="b9969-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9969-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9969-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9969-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9969-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9969-138">INPUTS</span></span>

## <span data-ttu-id="b9969-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9969-139">OUTPUTS</span></span>

### <span data-ttu-id="b9969-140">Microsoft. AzureStack. Management. Fabric. admin. Model. Drive</span><span class="sxs-lookup"><span data-stu-id="b9969-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="b9969-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9969-141">NOTES</span></span>

## <span data-ttu-id="b9969-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9969-142">RELATED LINKS</span></span>
