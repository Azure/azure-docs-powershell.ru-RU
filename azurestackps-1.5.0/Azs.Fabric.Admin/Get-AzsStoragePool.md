---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555659"
---
# <span data-ttu-id="da67b-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="da67b-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="da67b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da67b-102">SYNOPSIS</span></span>
<span data-ttu-id="da67b-103">Возвращает список всех пулов носителей для местоположения.</span><span class="sxs-lookup"><span data-stu-id="da67b-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="da67b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da67b-104">SYNTAX</span></span>

### <span data-ttu-id="da67b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da67b-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="da67b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="da67b-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="da67b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="da67b-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="da67b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da67b-108">DESCRIPTION</span></span>
<span data-ttu-id="da67b-109">Возвращает список всех пулов носителей для местоположения.</span><span class="sxs-lookup"><span data-stu-id="da67b-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="da67b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da67b-110">EXAMPLES</span></span>

### <span data-ttu-id="da67b-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="da67b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="da67b-112">Получение всех пулов носителей в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="da67b-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="da67b-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="da67b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="da67b-114">Получение пула носителей в указанном расположении с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="da67b-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="da67b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da67b-115">PARAMETERS</span></span>

### <span data-ttu-id="da67b-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="da67b-116">-Filter</span></span>
<span data-ttu-id="da67b-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="da67b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="da67b-118">-Location</span><span class="sxs-lookup"><span data-stu-id="da67b-118">-Location</span></span>
<span data-ttu-id="da67b-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="da67b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="da67b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da67b-120">-Name</span></span>
<span data-ttu-id="da67b-121">Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="da67b-121">Storage pool name.</span></span>

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

### <span data-ttu-id="da67b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da67b-122">-ResourceGroupName</span></span>
<span data-ttu-id="da67b-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da67b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="da67b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da67b-124">-ResourceId</span></span>
<span data-ttu-id="da67b-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="da67b-125">The resource id.</span></span>

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

### <span data-ttu-id="da67b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="da67b-126">-Skip</span></span>
<span data-ttu-id="da67b-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="da67b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="da67b-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="da67b-128">-StorageSystem</span></span>
<span data-ttu-id="da67b-129">Система хранения, в которой находится пул носителей.</span><span class="sxs-lookup"><span data-stu-id="da67b-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="da67b-130">-Top</span><span class="sxs-lookup"><span data-stu-id="da67b-130">-Top</span></span>
<span data-ttu-id="da67b-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="da67b-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="da67b-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="da67b-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="da67b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da67b-133">CommonParameters</span></span>
<span data-ttu-id="da67b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da67b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da67b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da67b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da67b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da67b-136">INPUTS</span></span>

## <span data-ttu-id="da67b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da67b-137">OUTPUTS</span></span>

### <span data-ttu-id="da67b-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="da67b-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="da67b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="da67b-139">NOTES</span></span>

## <span data-ttu-id="da67b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da67b-140">RELATED LINKS</span></span>

