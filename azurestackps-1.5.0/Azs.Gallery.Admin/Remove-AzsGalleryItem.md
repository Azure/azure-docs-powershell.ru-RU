---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555599"
---
# <span data-ttu-id="c6cec-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="c6cec-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="c6cec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6cec-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cec-103">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="c6cec-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="c6cec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6cec-104">SYNTAX</span></span>

### <span data-ttu-id="c6cec-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6cec-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6cec-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6cec-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6cec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6cec-107">DESCRIPTION</span></span>
<span data-ttu-id="c6cec-108">Удаление определенного элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="c6cec-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="c6cec-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6cec-109">EXAMPLES</span></span>

### <span data-ttu-id="c6cec-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c6cec-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="c6cec-111">Удаление элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="c6cec-111">Delete a gallery item.</span></span>

## <span data-ttu-id="c6cec-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6cec-112">PARAMETERS</span></span>

### <span data-ttu-id="c6cec-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c6cec-113">-Force</span></span>
<span data-ttu-id="c6cec-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c6cec-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c6cec-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6cec-115">-Name</span></span>
<span data-ttu-id="c6cec-116">Удостоверение элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="c6cec-116">Identity of the gallery item.</span></span>
<span data-ttu-id="c6cec-117">Содержит имя издателя, имя элемента и может включать версию, разделенную на символ точки.</span><span class="sxs-lookup"><span data-stu-id="c6cec-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="c6cec-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6cec-118">-ResourceId</span></span>
<span data-ttu-id="c6cec-119">Полный идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="c6cec-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="c6cec-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6cec-120">-Confirm</span></span>
<span data-ttu-id="c6cec-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6cec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6cec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6cec-122">-WhatIf</span></span>
<span data-ttu-id="c6cec-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6cec-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6cec-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6cec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6cec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6cec-125">CommonParameters</span></span>
<span data-ttu-id="c6cec-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6cec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6cec-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6cec-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6cec-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6cec-128">INPUTS</span></span>

## <span data-ttu-id="c6cec-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6cec-129">OUTPUTS</span></span>

## <span data-ttu-id="c6cec-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6cec-130">NOTES</span></span>

## <span data-ttu-id="c6cec-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6cec-131">RELATED LINKS</span></span>

