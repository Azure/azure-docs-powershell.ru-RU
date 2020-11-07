---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908885"
---
# <span data-ttu-id="95b73-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="95b73-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="95b73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95b73-102">SYNOPSIS</span></span>
<span data-ttu-id="95b73-103">Удаляет изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95b73-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="95b73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95b73-104">SYNTAX</span></span>

### <span data-ttu-id="95b73-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95b73-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95b73-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="95b73-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95b73-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95b73-107">DESCRIPTION</span></span>
<span data-ttu-id="95b73-108">Удаляет указанное изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95b73-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="95b73-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95b73-109">EXAMPLES</span></span>

### <span data-ttu-id="95b73-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="95b73-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="95b73-111">Удаление расширения образа платформы.</span><span class="sxs-lookup"><span data-stu-id="95b73-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="95b73-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95b73-112">PARAMETERS</span></span>

### <span data-ttu-id="95b73-113">-Force</span><span class="sxs-lookup"><span data-stu-id="95b73-113">-Force</span></span>
<span data-ttu-id="95b73-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="95b73-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="95b73-115">-Location</span><span class="sxs-lookup"><span data-stu-id="95b73-115">-Location</span></span>
<span data-ttu-id="95b73-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="95b73-116">Location of the resource.</span></span>

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

### <span data-ttu-id="95b73-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="95b73-117">-Publisher</span></span>
<span data-ttu-id="95b73-118">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="95b73-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="95b73-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95b73-119">-ResourceId</span></span>
<span data-ttu-id="95b73-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="95b73-120">The resource id.</span></span>

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

### <span data-ttu-id="95b73-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="95b73-121">-Type</span></span>
<span data-ttu-id="95b73-122">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="95b73-122">Type of extension.</span></span>

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

### <span data-ttu-id="95b73-123">-Version</span><span class="sxs-lookup"><span data-stu-id="95b73-123">-Version</span></span>
<span data-ttu-id="95b73-124">Версия образа расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95b73-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="95b73-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95b73-125">-Confirm</span></span>
<span data-ttu-id="95b73-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95b73-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95b73-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b73-127">-WhatIf</span></span>
<span data-ttu-id="95b73-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95b73-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95b73-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95b73-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95b73-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b73-130">CommonParameters</span></span>
<span data-ttu-id="95b73-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95b73-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b73-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b73-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b73-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95b73-133">INPUTS</span></span>

## <span data-ttu-id="95b73-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95b73-134">OUTPUTS</span></span>

## <span data-ttu-id="95b73-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="95b73-135">NOTES</span></span>

## <span data-ttu-id="95b73-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95b73-136">RELATED LINKS</span></span>

