---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 403f980af6b00272ca67b3ba180808ba8c82ebce
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077122"
---
# <span data-ttu-id="a7aa1-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="a7aa1-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="a7aa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="a7aa1-103">Возвращает образы виртуальных машин, загруженные в репозиторий образов платформы.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-103">Returns virtual machine images loaded into the platform image repository.</span></span>

## <span data-ttu-id="a7aa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7aa1-104">SYNTAX</span></span>

### <span data-ttu-id="a7aa1-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7aa1-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Publisher <String>] [-Offer <String>] [-Sku <String>] [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7aa1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a7aa1-106">Get</span></span>
```
Get-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7aa1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7aa1-107">ResourceId</span></span>
```
Get-AzsPlatformImage -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a7aa1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7aa1-108">DESCRIPTION</span></span>
<span data-ttu-id="a7aa1-109">Возвращает образы платформы.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-109">Returns platform images.</span></span>

## <span data-ttu-id="a7aa1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7aa1-110">EXAMPLES</span></span>

### <span data-ttu-id="a7aa1-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7aa1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlatformImage
```

<span data-ttu-id="a7aa1-112">Возвращает образы виртуальных машин, загруженные в репозиторий образов платформы в локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-112">Returns virtual machine images loaded into the platform image repository at the location local.</span></span>

### <span data-ttu-id="a7aa1-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="a7aa1-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsPlatformImage -Publisher Canonical -Offer UbuntuServer -Sku 16.04-LTS -Version 0.1.0
```

<span data-ttu-id="a7aa1-114">Получите определенный образ платформы.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-114">Get a specific platform image.</span></span>

## <span data-ttu-id="a7aa1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7aa1-115">PARAMETERS</span></span>

### <span data-ttu-id="a7aa1-116">-Location</span><span class="sxs-lookup"><span data-stu-id="a7aa1-116">-Location</span></span>
<span data-ttu-id="a7aa1-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-117">Location of the resource.</span></span>

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

### <span data-ttu-id="a7aa1-118">-Предложение</span><span class="sxs-lookup"><span data-stu-id="a7aa1-118">-Offer</span></span>
<span data-ttu-id="a7aa1-119">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-119">Name of the offer.</span></span>

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

### <span data-ttu-id="a7aa1-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a7aa1-120">-Publisher</span></span>
<span data-ttu-id="a7aa1-121">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="a7aa1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7aa1-122">-ResourceId</span></span>
<span data-ttu-id="a7aa1-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-123">The resource id.</span></span>

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

### <span data-ttu-id="a7aa1-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="a7aa1-124">-Sku</span></span>
<span data-ttu-id="a7aa1-125">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-125">Name of the SKU.</span></span>

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

### <span data-ttu-id="a7aa1-126">-Version</span><span class="sxs-lookup"><span data-stu-id="a7aa1-126">-Version</span></span>
<span data-ttu-id="a7aa1-127">Версия образа платформы.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-127">The version of the platform image.</span></span>

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

### <span data-ttu-id="a7aa1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7aa1-128">CommonParameters</span></span>
<span data-ttu-id="a7aa1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7aa1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7aa1-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7aa1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7aa1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7aa1-131">INPUTS</span></span>

## <span data-ttu-id="a7aa1-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7aa1-132">OUTPUTS</span></span>

### <span data-ttu-id="a7aa1-133">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="a7aa1-133">PlatformImageObject</span></span>

## <span data-ttu-id="a7aa1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7aa1-134">NOTES</span></span>

## <span data-ttu-id="a7aa1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7aa1-135">RELATED LINKS</span></span>
