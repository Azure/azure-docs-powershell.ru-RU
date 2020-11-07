---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908330"
---
# <span data-ttu-id="152da-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="152da-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="152da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="152da-102">SYNOPSIS</span></span>
<span data-ttu-id="152da-103">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="152da-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="152da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="152da-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="152da-105">DESCRIPTION</span></span>
<span data-ttu-id="152da-106">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="152da-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="152da-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="152da-107">EXAMPLES</span></span>

### <span data-ttu-id="152da-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="152da-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="152da-109">Создание нового элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="152da-109">Create a new gallery item.</span></span>

## <span data-ttu-id="152da-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="152da-110">PARAMETERS</span></span>

### <span data-ttu-id="152da-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="152da-111">-GalleryItemUri</span></span>
<span data-ttu-id="152da-112">Универсальный код ресурса (URI) для файла JSON элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="152da-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="152da-113">-Force</span><span class="sxs-lookup"><span data-stu-id="152da-113">-Force</span></span>
<span data-ttu-id="152da-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="152da-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="152da-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152da-115">-WhatIf</span></span>
<span data-ttu-id="152da-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="152da-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152da-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="152da-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152da-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="152da-118">-Confirm</span></span>
<span data-ttu-id="152da-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="152da-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152da-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152da-120">CommonParameters</span></span>
<span data-ttu-id="152da-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="152da-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152da-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="152da-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152da-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="152da-123">INPUTS</span></span>

## <span data-ttu-id="152da-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="152da-124">OUTPUTS</span></span>

### <span data-ttu-id="152da-125">Microsoft. AzureStack. Management. Gallery. admin. Model. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="152da-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="152da-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="152da-126">NOTES</span></span>

## <span data-ttu-id="152da-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="152da-127">RELATED LINKS</span></span>
