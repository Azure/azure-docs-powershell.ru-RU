---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077015"
---
# <span data-ttu-id="c7bf8-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="c7bf8-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="c7bf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bf8-103">Возвращает список всех пулов носителей для местоположения.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="c7bf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7bf8-104">SYNTAX</span></span>

### <span data-ttu-id="c7bf8-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7bf8-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c7bf8-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c7bf8-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7bf8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7bf8-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c7bf8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7bf8-108">DESCRIPTION</span></span>
<span data-ttu-id="c7bf8-109">Возвращает список всех пулов носителей для местоположения.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="c7bf8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7bf8-110">EXAMPLES</span></span>

### <span data-ttu-id="c7bf8-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="c7bf8-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="c7bf8-112">Получение всех пулов носителей в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="c7bf8-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="c7bf8-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="c7bf8-114">Получение пула носителей в указанном расположении с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="c7bf8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7bf8-115">PARAMETERS</span></span>

### <span data-ttu-id="c7bf8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7bf8-116">-Name</span></span>
<span data-ttu-id="c7bf8-117">Имя пула носителей.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-117">Storage pool name.</span></span>

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

### <span data-ttu-id="c7bf8-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="c7bf8-118">-StorageSystem</span></span>
<span data-ttu-id="c7bf8-119">Имя подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="c7bf8-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c7bf8-120">-Location</span></span>
<span data-ttu-id="c7bf8-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-121">Location of the resource.</span></span>

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

### <span data-ttu-id="c7bf8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7bf8-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7bf8-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c7bf8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7bf8-124">-ResourceId</span></span>
<span data-ttu-id="c7bf8-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-125">The resource id.</span></span>

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

### <span data-ttu-id="c7bf8-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="c7bf8-126">-Filter</span></span>
<span data-ttu-id="c7bf8-127">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="c7bf8-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="c7bf8-128">-Skip</span></span>
<span data-ttu-id="c7bf8-129">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c7bf8-130">-Top</span><span class="sxs-lookup"><span data-stu-id="c7bf8-130">-Top</span></span>
<span data-ttu-id="c7bf8-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c7bf8-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c7bf8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bf8-133">CommonParameters</span></span>
<span data-ttu-id="c7bf8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7bf8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bf8-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7bf8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bf8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7bf8-136">INPUTS</span></span>

## <span data-ttu-id="c7bf8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7bf8-137">OUTPUTS</span></span>

### <span data-ttu-id="c7bf8-138">Microsoft. AzureStack. Management. Fabric. admin. Models. StoragePool</span><span class="sxs-lookup"><span data-stu-id="c7bf8-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="c7bf8-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7bf8-139">NOTES</span></span>

## <span data-ttu-id="c7bf8-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7bf8-140">RELATED LINKS</span></span>
