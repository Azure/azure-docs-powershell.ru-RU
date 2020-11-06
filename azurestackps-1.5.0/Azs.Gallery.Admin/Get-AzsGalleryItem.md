---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555604"
---
# <span data-ttu-id="5e130-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="5e130-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="5e130-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e130-102">SYNOPSIS</span></span>
<span data-ttu-id="5e130-103">Список элементов коллекции.</span><span class="sxs-lookup"><span data-stu-id="5e130-103">Lists gallery items.</span></span>

## <span data-ttu-id="5e130-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e130-104">SYNTAX</span></span>

### <span data-ttu-id="5e130-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e130-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="5e130-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5e130-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="5e130-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e130-107">DESCRIPTION</span></span>
<span data-ttu-id="5e130-108">Получение списка элементов коллекции, доступных в Azure Stack Marketplace</span><span class="sxs-lookup"><span data-stu-id="5e130-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="5e130-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e130-109">EXAMPLES</span></span>

### <span data-ttu-id="5e130-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e130-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="5e130-111">Элементы коллекции списка.</span><span class="sxs-lookup"><span data-stu-id="5e130-111">List gallery items.</span></span>

### <span data-ttu-id="5e130-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e130-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="5e130-113">Получение элемента коллекции по имени.</span><span class="sxs-lookup"><span data-stu-id="5e130-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="5e130-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e130-114">PARAMETERS</span></span>

### <span data-ttu-id="5e130-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e130-115">-Name</span></span>
<span data-ttu-id="5e130-116">Удостоверение элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="5e130-116">Identity of the gallery item.</span></span>
<span data-ttu-id="5e130-117">Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.</span><span class="sxs-lookup"><span data-stu-id="5e130-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="5e130-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e130-118">CommonParameters</span></span>
<span data-ttu-id="5e130-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e130-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e130-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e130-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e130-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e130-121">INPUTS</span></span>

## <span data-ttu-id="5e130-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e130-122">OUTPUTS</span></span>

### <span data-ttu-id="5e130-123">Microsoft. AzureStack. Management. Gallery. admin. Model. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="5e130-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="5e130-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e130-124">NOTES</span></span>

## <span data-ttu-id="5e130-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e130-125">RELATED LINKS</span></span>

