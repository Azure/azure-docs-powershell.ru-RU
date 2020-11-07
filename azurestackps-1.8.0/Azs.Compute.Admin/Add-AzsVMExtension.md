---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908069"
---
# <span data-ttu-id="6433b-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="6433b-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="6433b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6433b-102">SYNOPSIS</span></span>
<span data-ttu-id="6433b-103">Создайте новый образ расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6433b-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="6433b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6433b-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6433b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6433b-105">DESCRIPTION</span></span>
<span data-ttu-id="6433b-106">Создание изображения расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6433b-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="6433b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6433b-107">EXAMPLES</span></span>

### <span data-ttu-id="6433b-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6433b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="6433b-109">Добавьте новое расширение платформы.</span><span class="sxs-lookup"><span data-stu-id="6433b-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="6433b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6433b-110">PARAMETERS</span></span>

### <span data-ttu-id="6433b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6433b-111">-AsJob</span></span>
<span data-ttu-id="6433b-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="6433b-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6433b-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="6433b-113">-ComputeRole</span></span>
<span data-ttu-id="6433b-114">Тип роли, IaaS или PaaS, которое поддерживает это расширение.</span><span class="sxs-lookup"><span data-stu-id="6433b-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6433b-115">-Force</span></span>
<span data-ttu-id="6433b-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6433b-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6433b-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="6433b-117">-IsSystemExtension</span></span>
<span data-ttu-id="6433b-118">Указывает, является ли расширение для системы.</span><span class="sxs-lookup"><span data-stu-id="6433b-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="6433b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="6433b-119">-Location</span></span>
<span data-ttu-id="6433b-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6433b-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6433b-121">-Publisher</span></span>
<span data-ttu-id="6433b-122">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="6433b-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="6433b-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="6433b-123">-SourceBlob</span></span>
<span data-ttu-id="6433b-124">Пакет расширения виртуальной машины в URI.</span><span class="sxs-lookup"><span data-stu-id="6433b-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="6433b-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="6433b-126">Значение true, если поддерживается несколько расширений.</span><span class="sxs-lookup"><span data-stu-id="6433b-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="6433b-127">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="6433b-127">-Type</span></span>
<span data-ttu-id="6433b-128">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="6433b-128">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-129">-Version</span><span class="sxs-lookup"><span data-stu-id="6433b-129">-Version</span></span>
<span data-ttu-id="6433b-130">Версия расширения образа компьютера vritual.</span><span class="sxs-lookup"><span data-stu-id="6433b-130">The version of the vritual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="6433b-131">-VmOsType</span></span>
<span data-ttu-id="6433b-132">Целевой тип операционной системы для виртуальной машины, необходимый для развертывания обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="6433b-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6433b-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="6433b-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="6433b-134">Значение, указывающее на то, включено ли расширение для поддержки установки масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6433b-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="6433b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6433b-135">-Confirm</span></span>
<span data-ttu-id="6433b-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6433b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6433b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6433b-137">-WhatIf</span></span>
<span data-ttu-id="6433b-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6433b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6433b-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6433b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6433b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6433b-140">CommonParameters</span></span>
<span data-ttu-id="6433b-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6433b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6433b-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6433b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6433b-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6433b-143">INPUTS</span></span>

## <span data-ttu-id="6433b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6433b-144">OUTPUTS</span></span>

### <span data-ttu-id="6433b-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="6433b-145">VmExtensionObject</span></span>

## <span data-ttu-id="6433b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6433b-146">NOTES</span></span>

## <span data-ttu-id="6433b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6433b-147">RELATED LINKS</span></span>

