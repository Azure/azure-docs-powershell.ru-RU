---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555200"
---
# <span data-ttu-id="fa0d2-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="fa0d2-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="fa0d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0d2-103">Удаляет изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="fa0d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa0d2-104">SYNTAX</span></span>

### <span data-ttu-id="fa0d2-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa0d2-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa0d2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa0d2-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa0d2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0d2-107">DESCRIPTION</span></span>
<span data-ttu-id="fa0d2-108">Удаляет указанное изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="fa0d2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa0d2-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0d2-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fa0d2-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="fa0d2-111">Удаление расширения образа платформы.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="fa0d2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa0d2-112">PARAMETERS</span></span>

### <span data-ttu-id="fa0d2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fa0d2-113">-Force</span></span>
<span data-ttu-id="fa0d2-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fa0d2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="fa0d2-115">-Location</span></span>
<span data-ttu-id="fa0d2-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-116">Location of the resource.</span></span>

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

### <span data-ttu-id="fa0d2-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fa0d2-117">-Publisher</span></span>
<span data-ttu-id="fa0d2-118">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="fa0d2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa0d2-119">-ResourceId</span></span>
<span data-ttu-id="fa0d2-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-120">The resource id.</span></span>

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

### <span data-ttu-id="fa0d2-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="fa0d2-121">-Type</span></span>
<span data-ttu-id="fa0d2-122">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-122">Type of extension.</span></span>

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

### <span data-ttu-id="fa0d2-123">-Version</span><span class="sxs-lookup"><span data-stu-id="fa0d2-123">-Version</span></span>
<span data-ttu-id="fa0d2-124">Версия образа расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="fa0d2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa0d2-125">-Confirm</span></span>
<span data-ttu-id="fa0d2-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0d2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0d2-127">-WhatIf</span></span>
<span data-ttu-id="fa0d2-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0d2-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0d2-130">CommonParameters</span></span>
<span data-ttu-id="fa0d2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa0d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0d2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0d2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0d2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa0d2-133">INPUTS</span></span>

## <span data-ttu-id="fa0d2-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa0d2-134">OUTPUTS</span></span>

## <span data-ttu-id="fa0d2-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa0d2-135">NOTES</span></span>

## <span data-ttu-id="fa0d2-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa0d2-136">RELATED LINKS</span></span>

