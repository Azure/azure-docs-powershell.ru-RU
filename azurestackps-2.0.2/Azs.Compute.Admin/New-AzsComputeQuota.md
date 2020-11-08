---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076729"
---
# <span data-ttu-id="a801b-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="a801b-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="a801b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a801b-102">SYNOPSIS</span></span>
<span data-ttu-id="a801b-103">Создание или обновление вычислительной квоты с указанными параметрами квоты.</span><span class="sxs-lookup"><span data-stu-id="a801b-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="a801b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a801b-104">SYNTAX</span></span>

### <span data-ttu-id="a801b-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a801b-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a801b-106">Заново</span><span class="sxs-lookup"><span data-stu-id="a801b-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a801b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a801b-107">DESCRIPTION</span></span>
<span data-ttu-id="a801b-108">Создание или обновление вычислительной квоты с указанными параметрами квоты.</span><span class="sxs-lookup"><span data-stu-id="a801b-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="a801b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a801b-109">EXAMPLES</span></span>

### <span data-ttu-id="a801b-110">Пример 1: создание вычислительной квоты с параметрами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a801b-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="a801b-111">Для всех параметров, которые не указаны, будет задан параметр по умолчанию, показанный выше.</span><span class="sxs-lookup"><span data-stu-id="a801b-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="a801b-112">Пример 2: создание вычислительной квоты с пользовательскими параметрами</span><span class="sxs-lookup"><span data-stu-id="a801b-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="a801b-113">Настройка квоты с помощью параметров.</span><span class="sxs-lookup"><span data-stu-id="a801b-113">Customize Quota with parameters.</span></span> <span data-ttu-id="a801b-114">Значения по умолчанию для всех указанных параметров будут заданы.</span><span class="sxs-lookup"><span data-stu-id="a801b-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="a801b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a801b-115">PARAMETERS</span></span>

### <span data-ttu-id="a801b-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="a801b-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="a801b-117">Максимально допустимое количество наборов доступности.</span><span class="sxs-lookup"><span data-stu-id="a801b-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="a801b-118">-CoresCount</span></span>
<span data-ttu-id="a801b-119">Максимально допустимое число ядер.</span><span class="sxs-lookup"><span data-stu-id="a801b-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a801b-120">-DefaultProfile</span></span>
<span data-ttu-id="a801b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a801b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a801b-122">-Location</span></span>
<span data-ttu-id="a801b-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a801b-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="a801b-124">-Location1</span></span>
<span data-ttu-id="a801b-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a801b-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a801b-126">-Name</span></span>
<span data-ttu-id="a801b-127">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="a801b-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-128">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="a801b-128">-NewQuota</span></span>
<span data-ttu-id="a801b-129">Хранит сведения о квотах, которые используются для управления выделением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a801b-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="a801b-130">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NEWQUOTA и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a801b-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="a801b-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="a801b-132">Максимально допустимое количество управляемых дисков и моментальных снимков типа Premium.</span><span class="sxs-lookup"><span data-stu-id="a801b-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="a801b-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="a801b-134">Максимально допустимое количество управляемых дисков и снимков типа "Стандартный".</span><span class="sxs-lookup"><span data-stu-id="a801b-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a801b-135">-SubscriptionId</span></span>
<span data-ttu-id="a801b-136">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a801b-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a801b-137">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a801b-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="a801b-138">-VirtualMachineCount</span></span>
<span data-ttu-id="a801b-139">Максимально допустимое количество виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a801b-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="a801b-140">-VMScaleSetCount</span></span>
<span data-ttu-id="a801b-141">Максимальное количество допустимых наборов шкал.</span><span class="sxs-lookup"><span data-stu-id="a801b-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a801b-142">-Confirm</span></span>
<span data-ttu-id="a801b-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a801b-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a801b-144">-WhatIf</span></span>
<span data-ttu-id="a801b-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a801b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a801b-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a801b-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a801b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a801b-147">CommonParameters</span></span>
<span data-ttu-id="a801b-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a801b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a801b-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a801b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a801b-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a801b-150">INPUTS</span></span>

### <span data-ttu-id="a801b-151">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="a801b-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="a801b-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a801b-152">OUTPUTS</span></span>

### <span data-ttu-id="a801b-153">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="a801b-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="a801b-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="a801b-154">NOTES</span></span>

<span data-ttu-id="a801b-155">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a801b-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a801b-156">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a801b-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a801b-157">NEWQUOTA <IQuota> : удерживает вычислительные квоты, которые используются для управления выделением ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a801b-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="a801b-158">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a801b-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a801b-159">`[AvailabilitySetCount <Int32?>]`: Максимально допустимое количество наборов доступности.</span><span class="sxs-lookup"><span data-stu-id="a801b-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="a801b-160">`[CoresLimit <Int32?>]`: Максимально допустимое число ядер.</span><span class="sxs-lookup"><span data-stu-id="a801b-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="a801b-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Максимальное количество управляемых дисков и снимков типа Premium разрешено.</span><span class="sxs-lookup"><span data-stu-id="a801b-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="a801b-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Максимально допустимое количество управляемых дисков и снимков типа "Стандартный".</span><span class="sxs-lookup"><span data-stu-id="a801b-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="a801b-163">`[VMScaleSetCount <Int32?>]`: Максимальное количество допустимых наборов шкал.</span><span class="sxs-lookup"><span data-stu-id="a801b-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="a801b-164">`[VirtualMachineCount <Int32?>]`: Максимально допустимое количество виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a801b-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="a801b-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a801b-165">RELATED LINKS</span></span>
