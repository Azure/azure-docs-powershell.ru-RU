---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2580e2b6de179cdc3a9407b514848cc832e798e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555223"
---
# <span data-ttu-id="6c2ea-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="6c2ea-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="6c2ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2ea-103">Возвращает образы виртуальных машин, загруженные в репозиторий образов платформы.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="6c2ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c2ea-104">SYNTAX</span></span>

### <span data-ttu-id="6c2ea-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c2ea-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c2ea-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6c2ea-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c2ea-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c2ea-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6c2ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c2ea-108">DESCRIPTION</span></span>
<span data-ttu-id="6c2ea-109">Возвращает образы платформы.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-109">Returns platform images.</span></span>

## <span data-ttu-id="6c2ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c2ea-110">EXAMPLES</span></span>

### <span data-ttu-id="6c2ea-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6c2ea-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="6c2ea-112">Возвращает образы виртуальных машин, загруженные в репозиторий образов платформы в локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="6c2ea-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6c2ea-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="6c2ea-114">Получите определенный образ платформы.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-114">Get a specific platform image.</span></span>

## <span data-ttu-id="6c2ea-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c2ea-115">PARAMETERS</span></span>

### <span data-ttu-id="6c2ea-116">-Location</span><span class="sxs-lookup"><span data-stu-id="6c2ea-116">-Location</span></span>
<span data-ttu-id="6c2ea-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-117">Location of the resource.</span></span>

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

### <span data-ttu-id="6c2ea-118">-Предложение</span><span class="sxs-lookup"><span data-stu-id="6c2ea-118">-Offer</span></span>
<span data-ttu-id="6c2ea-119">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-119">Name of the offer.</span></span>

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

### <span data-ttu-id="6c2ea-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6c2ea-120">-Publisher</span></span>
<span data-ttu-id="6c2ea-121">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="6c2ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c2ea-122">-ResourceId</span></span>
<span data-ttu-id="6c2ea-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-123">The resource id.</span></span>

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

### <span data-ttu-id="6c2ea-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="6c2ea-124">-Sku</span></span>
<span data-ttu-id="6c2ea-125">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="6c2ea-126">-Version</span><span class="sxs-lookup"><span data-stu-id="6c2ea-126">-Version</span></span>
<span data-ttu-id="6c2ea-127">Версия образа платформы.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="6c2ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2ea-128">CommonParameters</span></span>
<span data-ttu-id="6c2ea-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2ea-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c2ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2ea-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c2ea-131">INPUTS</span></span>

## <span data-ttu-id="6c2ea-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c2ea-132">OUTPUTS</span></span>

### <span data-ttu-id="6c2ea-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="6c2ea-133">PlatformImageObject</span></span>

## <span data-ttu-id="6c2ea-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c2ea-134">NOTES</span></span>

## <span data-ttu-id="6c2ea-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c2ea-135">RELATED LINKS</span></span>

