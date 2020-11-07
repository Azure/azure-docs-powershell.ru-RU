---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908217"
---
# <span data-ttu-id="ac09f-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="ac09f-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="ac09f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac09f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac09f-103">Удаляет изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac09f-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="ac09f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac09f-104">SYNTAX</span></span>

### <span data-ttu-id="ac09f-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac09f-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac09f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac09f-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac09f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac09f-107">DESCRIPTION</span></span>
<span data-ttu-id="ac09f-108">Удаляет указанное изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac09f-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="ac09f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac09f-109">EXAMPLES</span></span>

### <span data-ttu-id="ac09f-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ac09f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="ac09f-111">Удаление расширения образа платформы.</span><span class="sxs-lookup"><span data-stu-id="ac09f-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="ac09f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac09f-112">PARAMETERS</span></span>

### <span data-ttu-id="ac09f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ac09f-113">-Force</span></span>
<span data-ttu-id="ac09f-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ac09f-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ac09f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ac09f-115">-Location</span></span>
<span data-ttu-id="ac09f-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac09f-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac09f-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ac09f-117">-Publisher</span></span>
<span data-ttu-id="ac09f-118">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="ac09f-118">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac09f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac09f-119">-ResourceId</span></span>
<span data-ttu-id="ac09f-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac09f-120">The resource id.</span></span>

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

### <span data-ttu-id="ac09f-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="ac09f-121">-Type</span></span>
<span data-ttu-id="ac09f-122">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="ac09f-122">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac09f-123">-Version</span><span class="sxs-lookup"><span data-stu-id="ac09f-123">-Version</span></span>
<span data-ttu-id="ac09f-124">Версия образа расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ac09f-124">The version of the virtual machine extension image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac09f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac09f-125">-Confirm</span></span>
<span data-ttu-id="ac09f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac09f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac09f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac09f-127">-WhatIf</span></span>
<span data-ttu-id="ac09f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac09f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac09f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac09f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac09f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac09f-130">CommonParameters</span></span>
<span data-ttu-id="ac09f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac09f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac09f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac09f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac09f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac09f-133">INPUTS</span></span>

## <span data-ttu-id="ac09f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac09f-134">OUTPUTS</span></span>

## <span data-ttu-id="ac09f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac09f-135">NOTES</span></span>

## <span data-ttu-id="ac09f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac09f-136">RELATED LINKS</span></span>

