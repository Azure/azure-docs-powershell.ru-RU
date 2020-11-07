---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908241"
---
# <span data-ttu-id="24d75-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="24d75-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="24d75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24d75-102">SYNOPSIS</span></span>
<span data-ttu-id="24d75-103">Создайте новую вычислительную квоту, используемую для ограничения вычислительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24d75-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="24d75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24d75-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24d75-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24d75-105">DESCRIPTION</span></span>
<span data-ttu-id="24d75-106">Создайте новую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="24d75-106">Create a new compute quota.</span></span>

## <span data-ttu-id="24d75-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24d75-107">EXAMPLES</span></span>

### <span data-ttu-id="24d75-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24d75-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="24d75-109">Создайте новую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="24d75-109">Create a new compute quota.</span></span>

## <span data-ttu-id="24d75-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24d75-110">PARAMETERS</span></span>

### <span data-ttu-id="24d75-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="24d75-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="24d75-112">Количество разрешенных наборов доступности.</span><span class="sxs-lookup"><span data-stu-id="24d75-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="24d75-113">-CoresCount</span></span>
<span data-ttu-id="24d75-114">Количество допустимых ядер.</span><span class="sxs-lookup"><span data-stu-id="24d75-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-115">-Location</span><span class="sxs-lookup"><span data-stu-id="24d75-115">-Location</span></span>
<span data-ttu-id="24d75-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="24d75-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24d75-117">-Name</span></span>
<span data-ttu-id="24d75-118">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="24d75-118">Name of the quota.</span></span>

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

### <span data-ttu-id="24d75-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="24d75-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="24d75-120">Размер стандартных управляемых дисков и снимков разрешено.</span><span class="sxs-lookup"><span data-stu-id="24d75-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="24d75-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="24d75-122">Размер стандартных управляемых дисков и снимков разрешено.</span><span class="sxs-lookup"><span data-stu-id="24d75-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="24d75-123">-VirtualMachineCount</span></span>
<span data-ttu-id="24d75-124">Количество разрешенных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="24d75-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="24d75-125">-VmScaleSetCount</span></span>
<span data-ttu-id="24d75-126">Количество допустимых наборов масштабирований.</span><span class="sxs-lookup"><span data-stu-id="24d75-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d75-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24d75-127">-Confirm</span></span>
<span data-ttu-id="24d75-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24d75-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d75-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d75-129">-WhatIf</span></span>
<span data-ttu-id="24d75-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24d75-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24d75-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24d75-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d75-132">CommonParameters</span></span>
<span data-ttu-id="24d75-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24d75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d75-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d75-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d75-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24d75-135">INPUTS</span></span>

## <span data-ttu-id="24d75-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24d75-136">OUTPUTS</span></span>

### <span data-ttu-id="24d75-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="24d75-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="24d75-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="24d75-138">NOTES</span></span>

## <span data-ttu-id="24d75-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24d75-139">RELATED LINKS</span></span>

