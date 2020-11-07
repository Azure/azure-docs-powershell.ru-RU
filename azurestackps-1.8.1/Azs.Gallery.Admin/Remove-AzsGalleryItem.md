---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909118"
---
# <span data-ttu-id="e136c-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="e136c-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="e136c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e136c-102">SYNOPSIS</span></span>
<span data-ttu-id="e136c-103">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="e136c-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="e136c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e136c-104">SYNTAX</span></span>

### <span data-ttu-id="e136c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e136c-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e136c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e136c-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e136c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e136c-107">DESCRIPTION</span></span>
<span data-ttu-id="e136c-108">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="e136c-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="e136c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e136c-109">EXAMPLES</span></span>

### <span data-ttu-id="e136c-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="e136c-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="e136c-111">Удаление элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="e136c-111">Delete a gallery item.</span></span>

## <span data-ttu-id="e136c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e136c-112">PARAMETERS</span></span>

### <span data-ttu-id="e136c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e136c-113">-Name</span></span>
<span data-ttu-id="e136c-114">Удостоверение элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="e136c-114">Identity of the gallery item.</span></span>
<span data-ttu-id="e136c-115">Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.</span><span class="sxs-lookup"><span data-stu-id="e136c-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="e136c-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e136c-116">-ResourceId</span></span>
<span data-ttu-id="e136c-117">Полный идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e136c-117">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="e136c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e136c-118">-Force</span></span>
<span data-ttu-id="e136c-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e136c-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e136c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e136c-120">-WhatIf</span></span>
<span data-ttu-id="e136c-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e136c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e136c-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e136c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e136c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e136c-123">-Confirm</span></span>
<span data-ttu-id="e136c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e136c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e136c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e136c-125">CommonParameters</span></span>
<span data-ttu-id="e136c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e136c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e136c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e136c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e136c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e136c-128">INPUTS</span></span>

## <span data-ttu-id="e136c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e136c-129">OUTPUTS</span></span>

## <span data-ttu-id="e136c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e136c-130">NOTES</span></span>

## <span data-ttu-id="e136c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e136c-131">RELATED LINKS</span></span>
