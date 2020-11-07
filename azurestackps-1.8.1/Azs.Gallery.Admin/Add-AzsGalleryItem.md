---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909229"
---
# <span data-ttu-id="26291-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="26291-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="26291-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26291-102">SYNOPSIS</span></span>
<span data-ttu-id="26291-103">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="26291-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="26291-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26291-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26291-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26291-105">DESCRIPTION</span></span>
<span data-ttu-id="26291-106">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="26291-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="26291-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26291-107">EXAMPLES</span></span>

### <span data-ttu-id="26291-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="26291-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="26291-109">Создание нового элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="26291-109">Create a new gallery item.</span></span>

## <span data-ttu-id="26291-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26291-110">PARAMETERS</span></span>

### <span data-ttu-id="26291-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="26291-111">-GalleryItemUri</span></span>
<span data-ttu-id="26291-112">Универсальный код ресурса (URI) для файла JSON элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="26291-112">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="26291-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26291-113">-Force</span></span>
<span data-ttu-id="26291-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="26291-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="26291-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26291-115">-WhatIf</span></span>
<span data-ttu-id="26291-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26291-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26291-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26291-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26291-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26291-118">-Confirm</span></span>
<span data-ttu-id="26291-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26291-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26291-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26291-120">CommonParameters</span></span>
<span data-ttu-id="26291-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26291-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26291-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26291-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26291-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26291-123">INPUTS</span></span>

## <span data-ttu-id="26291-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26291-124">OUTPUTS</span></span>

### <span data-ttu-id="26291-125">Microsoft. AzureStack. Management. Gallery. admin. Model. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="26291-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="26291-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="26291-126">NOTES</span></span>

## <span data-ttu-id="26291-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26291-127">RELATED LINKS</span></span>
