---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc92bcc617c771c15330d1a24e8ed24466f7ffc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906737"
---
# <span data-ttu-id="83a5a-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="83a5a-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="83a5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="83a5a-103">Создайте новую вычислительную квоту, используемую для ограничения вычислительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83a5a-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="83a5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83a5a-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83a5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="83a5a-106">Создайте новую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="83a5a-106">Create a new compute quota.</span></span>

## <span data-ttu-id="83a5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="83a5a-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83a5a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="83a5a-109">Создайте новую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="83a5a-109">Create a new compute quota.</span></span>

## <span data-ttu-id="83a5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="83a5a-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="83a5a-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="83a5a-112">Количество разрешенных наборов доступности.</span><span class="sxs-lookup"><span data-stu-id="83a5a-112">Number  of availability sets allowed.</span></span>

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

### <span data-ttu-id="83a5a-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="83a5a-113">-CoresCount</span></span>
<span data-ttu-id="83a5a-114">Количество допустимых ядер.</span><span class="sxs-lookup"><span data-stu-id="83a5a-114">Number  of cores allowed.</span></span>

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

### <span data-ttu-id="83a5a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="83a5a-115">-Location</span></span>
<span data-ttu-id="83a5a-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="83a5a-116">Location of the resource.</span></span>

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

### <span data-ttu-id="83a5a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="83a5a-117">-Name</span></span>
<span data-ttu-id="83a5a-118">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="83a5a-118">Name of the quota.</span></span>

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

### <span data-ttu-id="83a5a-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="83a5a-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="83a5a-120">Размер стандартных управляемых дисков и снимков разрешено.</span><span class="sxs-lookup"><span data-stu-id="83a5a-120">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="83a5a-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="83a5a-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="83a5a-122">Размер стандартных управляемых дисков и снимков разрешено.</span><span class="sxs-lookup"><span data-stu-id="83a5a-122">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="83a5a-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="83a5a-123">-VirtualMachineCount</span></span>
<span data-ttu-id="83a5a-124">Количество разрешенных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="83a5a-124">Number  of virtual machines allowed.</span></span>

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

### <span data-ttu-id="83a5a-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="83a5a-125">-VmScaleSetCount</span></span>
<span data-ttu-id="83a5a-126">Количество допустимых наборов масштабирований.</span><span class="sxs-lookup"><span data-stu-id="83a5a-126">Number  of scale sets allowed.</span></span>

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

### <span data-ttu-id="83a5a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83a5a-127">-Confirm</span></span>
<span data-ttu-id="83a5a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="83a5a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83a5a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83a5a-129">-WhatIf</span></span>
<span data-ttu-id="83a5a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="83a5a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83a5a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="83a5a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83a5a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a5a-132">CommonParameters</span></span>
<span data-ttu-id="83a5a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83a5a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a5a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83a5a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a5a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83a5a-135">INPUTS</span></span>

## <span data-ttu-id="83a5a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83a5a-136">OUTPUTS</span></span>

### <span data-ttu-id="83a5a-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="83a5a-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="83a5a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="83a5a-138">NOTES</span></span>

## <span data-ttu-id="83a5a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83a5a-139">RELATED LINKS</span></span>

