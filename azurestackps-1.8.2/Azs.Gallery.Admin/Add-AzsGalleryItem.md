---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076877"
---
# <span data-ttu-id="1847e-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="1847e-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="1847e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1847e-102">SYNOPSIS</span></span>
<span data-ttu-id="1847e-103">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="1847e-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="1847e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1847e-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1847e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1847e-105">DESCRIPTION</span></span>
<span data-ttu-id="1847e-106">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="1847e-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="1847e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1847e-107">EXAMPLES</span></span>

### <span data-ttu-id="1847e-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="1847e-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="1847e-109">Создание нового элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="1847e-109">Create a new gallery item.</span></span>

## <span data-ttu-id="1847e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1847e-110">PARAMETERS</span></span>

### <span data-ttu-id="1847e-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="1847e-111">-GalleryItemUri</span></span>
<span data-ttu-id="1847e-112">Универсальный код ресурса (URI) для файла JSON элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="1847e-112">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1847e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1847e-113">-Force</span></span>
<span data-ttu-id="1847e-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1847e-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1847e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1847e-115">-WhatIf</span></span>
<span data-ttu-id="1847e-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1847e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1847e-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1847e-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1847e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1847e-118">-Confirm</span></span>
<span data-ttu-id="1847e-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1847e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1847e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1847e-120">CommonParameters</span></span>
<span data-ttu-id="1847e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1847e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1847e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1847e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1847e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1847e-123">INPUTS</span></span>

## <span data-ttu-id="1847e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1847e-124">OUTPUTS</span></span>

### <span data-ttu-id="1847e-125">Microsoft. AzureStack. Management. Gallery. admin. Model. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="1847e-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="1847e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1847e-126">NOTES</span></span>

## <span data-ttu-id="1847e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1847e-127">RELATED LINKS</span></span>
