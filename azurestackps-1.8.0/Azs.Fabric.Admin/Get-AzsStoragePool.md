---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908133"
---
# <span data-ttu-id="a6c14-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="a6c14-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="a6c14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6c14-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c14-103">Возвращает список всех пулов носителей для местоположения.</span><span class="sxs-lookup"><span data-stu-id="a6c14-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="a6c14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6c14-104">SYNTAX</span></span>

### <span data-ttu-id="a6c14-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6c14-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a6c14-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a6c14-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6c14-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c14-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a6c14-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c14-108">DESCRIPTION</span></span>
<span data-ttu-id="a6c14-109">Возвращает список всех пулов носителей для местоположения.</span><span class="sxs-lookup"><span data-stu-id="a6c14-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="a6c14-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6c14-110">EXAMPLES</span></span>

### <span data-ttu-id="a6c14-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="a6c14-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="a6c14-112">Получение всех пулов носителей в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="a6c14-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="a6c14-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="a6c14-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="a6c14-114">Получение пула носителей в указанном расположении с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="a6c14-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="a6c14-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6c14-115">PARAMETERS</span></span>

### <span data-ttu-id="a6c14-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6c14-116">-Name</span></span>
<span data-ttu-id="a6c14-117">Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="a6c14-117">Storage pool name.</span></span>

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

### <span data-ttu-id="a6c14-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="a6c14-118">-StorageSystem</span></span>
<span data-ttu-id="a6c14-119">Имя подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6c14-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="a6c14-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a6c14-120">-Location</span></span>
<span data-ttu-id="a6c14-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6c14-121">Location of the resource.</span></span>

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

### <span data-ttu-id="a6c14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c14-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6c14-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6c14-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a6c14-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6c14-124">-ResourceId</span></span>
<span data-ttu-id="a6c14-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6c14-125">The resource id.</span></span>

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

### <span data-ttu-id="a6c14-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="a6c14-126">-Filter</span></span>
<span data-ttu-id="a6c14-127">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="a6c14-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="a6c14-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="a6c14-128">-Skip</span></span>
<span data-ttu-id="a6c14-129">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="a6c14-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a6c14-130">-Top</span><span class="sxs-lookup"><span data-stu-id="a6c14-130">-Top</span></span>
<span data-ttu-id="a6c14-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a6c14-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a6c14-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="a6c14-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a6c14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c14-133">CommonParameters</span></span>
<span data-ttu-id="a6c14-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6c14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c14-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c14-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c14-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6c14-136">INPUTS</span></span>

## <span data-ttu-id="a6c14-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c14-137">OUTPUTS</span></span>

### <span data-ttu-id="a6c14-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="a6c14-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="a6c14-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6c14-139">NOTES</span></span>

## <span data-ttu-id="a6c14-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6c14-140">RELATED LINKS</span></span>
