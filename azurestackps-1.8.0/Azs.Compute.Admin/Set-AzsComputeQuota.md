---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908213"
---
# <span data-ttu-id="d2d3b-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d2d3b-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="d2d3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2d3b-103">Обновите существующую вычислительную квоту с помощью указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="d2d3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2d3b-104">SYNTAX</span></span>

### <span data-ttu-id="d2d3b-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2d3b-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2d3b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d3b-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2d3b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2d3b-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2d3b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="d2d3b-109">Обновите существующую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="d2d3b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="d2d3b-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d2d3b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="d2d3b-112">Обновите расчетную квоту.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-112">Update a compute quota.</span></span>

## <span data-ttu-id="d2d3b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2d3b-113">PARAMETERS</span></span>

### <span data-ttu-id="d2d3b-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="d2d3b-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="d2d3b-115">Количество разрешенных наборов доступности.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="d2d3b-116">-CoresCount</span></span>
<span data-ttu-id="d2d3b-117">Количество допустимых ядер.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2d3b-118">-InputObject</span></span>
<span data-ttu-id="d2d3b-119">Возможно, возвращенная вычисляемая квота формы Get-AzsComputeQuota была изменена.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="d2d3b-120">-Location</span></span>
<span data-ttu-id="d2d3b-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2d3b-122">-Name</span></span>
<span data-ttu-id="d2d3b-123">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="d2d3b-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="d2d3b-125">Размер стандартных управляемых дисков и снимков разрешено.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2d3b-126">-ResourceId</span></span>
<span data-ttu-id="d2d3b-127">Идентификатор квоты вычислений ARM.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="d2d3b-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="d2d3b-129">Размер стандартных управляемых дисков и снимков разрешено.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="d2d3b-130">-VirtualMachineCount</span></span>
<span data-ttu-id="d2d3b-131">Количество разрешенных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="d2d3b-132">-VmScaleSetCount</span></span>
<span data-ttu-id="d2d3b-133">Количество допустимых наборов масштабирований.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2d3b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2d3b-134">-Confirm</span></span>
<span data-ttu-id="d2d3b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2d3b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2d3b-136">-WhatIf</span></span>
<span data-ttu-id="d2d3b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2d3b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2d3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2d3b-139">CommonParameters</span></span>
<span data-ttu-id="d2d3b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2d3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2d3b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2d3b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2d3b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2d3b-142">INPUTS</span></span>

## <span data-ttu-id="d2d3b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2d3b-143">OUTPUTS</span></span>

### <span data-ttu-id="d2d3b-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="d2d3b-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="d2d3b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2d3b-145">NOTES</span></span>

## <span data-ttu-id="d2d3b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2d3b-146">RELATED LINKS</span></span>

