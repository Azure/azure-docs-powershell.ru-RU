---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076792"
---
# <span data-ttu-id="4d96e-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="4d96e-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="4d96e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d96e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d96e-103">Создайте новый образ расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d96e-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="4d96e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d96e-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d96e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d96e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d96e-106">Создание изображения расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d96e-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="4d96e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d96e-107">EXAMPLES</span></span>

### <span data-ttu-id="4d96e-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d96e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="4d96e-109">Добавьте новое расширение платформы.</span><span class="sxs-lookup"><span data-stu-id="4d96e-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="4d96e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d96e-110">PARAMETERS</span></span>

### <span data-ttu-id="4d96e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d96e-111">-AsJob</span></span>
<span data-ttu-id="4d96e-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="4d96e-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4d96e-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="4d96e-113">-ComputeRole</span></span>
<span data-ttu-id="4d96e-114">Тип роли, IaaS или PaaS, которое поддерживает это расширение.</span><span class="sxs-lookup"><span data-stu-id="4d96e-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="4d96e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4d96e-115">-Force</span></span>
<span data-ttu-id="4d96e-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4d96e-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4d96e-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="4d96e-117">-IsSystemExtension</span></span>
<span data-ttu-id="4d96e-118">Указывает, является ли расширение для системы.</span><span class="sxs-lookup"><span data-stu-id="4d96e-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="4d96e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4d96e-119">-Location</span></span>
<span data-ttu-id="4d96e-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4d96e-120">Location of the resource.</span></span>

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

### <span data-ttu-id="4d96e-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4d96e-121">-Publisher</span></span>
<span data-ttu-id="4d96e-122">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="4d96e-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="4d96e-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="4d96e-123">-SourceBlob</span></span>
<span data-ttu-id="4d96e-124">Пакет расширения виртуальной машины в URI.</span><span class="sxs-lookup"><span data-stu-id="4d96e-124">URI to virtual machine extension package.</span></span>

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

### <span data-ttu-id="4d96e-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="4d96e-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="4d96e-126">Значение true, если поддерживается несколько расширений.</span><span class="sxs-lookup"><span data-stu-id="4d96e-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="4d96e-127">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="4d96e-127">-Type</span></span>
<span data-ttu-id="4d96e-128">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="4d96e-128">Type of extension.</span></span>

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

### <span data-ttu-id="4d96e-129">-Version</span><span class="sxs-lookup"><span data-stu-id="4d96e-129">-Version</span></span>
<span data-ttu-id="4d96e-130">Версия расширения образа компьютера vritual.</span><span class="sxs-lookup"><span data-stu-id="4d96e-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="4d96e-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="4d96e-131">-VmOsType</span></span>
<span data-ttu-id="4d96e-132">Целевой тип операционной системы для виртуальной машины, необходимый для развертывания обработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="4d96e-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="4d96e-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="4d96e-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="4d96e-134">Значение, указывающее на то, включено ли расширение для поддержки установки масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="4d96e-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="4d96e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d96e-135">-Confirm</span></span>
<span data-ttu-id="4d96e-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d96e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d96e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d96e-137">-WhatIf</span></span>
<span data-ttu-id="4d96e-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d96e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d96e-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d96e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d96e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d96e-140">CommonParameters</span></span>
<span data-ttu-id="4d96e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d96e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d96e-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d96e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d96e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d96e-143">INPUTS</span></span>

## <span data-ttu-id="4d96e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d96e-144">OUTPUTS</span></span>

### <span data-ttu-id="4d96e-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="4d96e-145">VmExtensionObject</span></span>

## <span data-ttu-id="4d96e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d96e-146">NOTES</span></span>

## <span data-ttu-id="4d96e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d96e-147">RELATED LINKS</span></span>

