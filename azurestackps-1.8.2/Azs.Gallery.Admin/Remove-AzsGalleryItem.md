---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077138"
---
# <span data-ttu-id="13838-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="13838-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="13838-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13838-102">SYNOPSIS</span></span>
<span data-ttu-id="13838-103">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="13838-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="13838-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13838-104">SYNTAX</span></span>

### <span data-ttu-id="13838-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13838-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13838-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13838-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13838-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13838-107">DESCRIPTION</span></span>
<span data-ttu-id="13838-108">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="13838-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="13838-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13838-109">EXAMPLES</span></span>

### <span data-ttu-id="13838-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="13838-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="13838-111">Удаление элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="13838-111">Delete a gallery item.</span></span>

## <span data-ttu-id="13838-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13838-112">PARAMETERS</span></span>

### <span data-ttu-id="13838-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13838-113">-Name</span></span>
<span data-ttu-id="13838-114">Удостоверение элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="13838-114">Identity of the gallery item.</span></span>
<span data-ttu-id="13838-115">Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.</span><span class="sxs-lookup"><span data-stu-id="13838-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13838-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13838-116">-ResourceId</span></span>
<span data-ttu-id="13838-117">Полный идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="13838-117">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="13838-118">-Force</span><span class="sxs-lookup"><span data-stu-id="13838-118">-Force</span></span>
<span data-ttu-id="13838-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13838-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="13838-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13838-120">-WhatIf</span></span>
<span data-ttu-id="13838-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13838-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13838-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13838-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13838-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13838-123">-Confirm</span></span>
<span data-ttu-id="13838-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13838-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13838-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13838-125">CommonParameters</span></span>
<span data-ttu-id="13838-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13838-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13838-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13838-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13838-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13838-128">INPUTS</span></span>

## <span data-ttu-id="13838-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13838-129">OUTPUTS</span></span>

## <span data-ttu-id="13838-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="13838-130">NOTES</span></span>

## <span data-ttu-id="13838-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13838-131">RELATED LINKS</span></span>
