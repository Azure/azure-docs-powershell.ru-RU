---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908806"
---
# <span data-ttu-id="ae3ea-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="ae3ea-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="ae3ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3ea-103">Возвращает список всех подсистем хранилища для местоположения.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="ae3ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae3ea-104">SYNTAX</span></span>

### <span data-ttu-id="ae3ea-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae3ea-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ae3ea-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ae3ea-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ae3ea-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3ea-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ae3ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae3ea-108">DESCRIPTION</span></span>
<span data-ttu-id="ae3ea-109">Возвращает список всех подсистем хранилища для местоположения.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="ae3ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae3ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ae3ea-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="ae3ea-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="ae3ea-112">Получение всех подсистем хранилища из места.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="ae3ea-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="ae3ea-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="ae3ea-114">Получение подсистемы хранилища с заданными расположением и именем.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="ae3ea-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae3ea-115">PARAMETERS</span></span>

### <span data-ttu-id="ae3ea-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae3ea-116">-Name</span></span>
<span data-ttu-id="ae3ea-117">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ae3ea-118">-Location</span><span class="sxs-lookup"><span data-stu-id="ae3ea-118">-Location</span></span>
<span data-ttu-id="ae3ea-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ae3ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae3ea-121">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ae3ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae3ea-122">-ResourceId</span></span>
<span data-ttu-id="ae3ea-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-123">The resource id.</span></span>

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

### <span data-ttu-id="ae3ea-124">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="ae3ea-124">-Filter</span></span>
<span data-ttu-id="ae3ea-125">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="ae3ea-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="ae3ea-126">-Skip</span></span>
<span data-ttu-id="ae3ea-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ae3ea-128">-Top</span><span class="sxs-lookup"><span data-stu-id="ae3ea-128">-Top</span></span>
<span data-ttu-id="ae3ea-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ae3ea-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ae3ea-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3ea-131">CommonParameters</span></span>
<span data-ttu-id="ae3ea-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae3ea-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3ea-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3ea-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3ea-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae3ea-134">INPUTS</span></span>

## <span data-ttu-id="ae3ea-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae3ea-135">OUTPUTS</span></span>

### <span data-ttu-id="ae3ea-136">Microsoft. AzureStack. Management. Fabric. admin. Models. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="ae3ea-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="ae3ea-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae3ea-137">NOTES</span></span>

## <span data-ttu-id="ae3ea-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae3ea-138">RELATED LINKS</span></span>
