---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075360"
---
# <span data-ttu-id="a721f-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="a721f-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="a721f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a721f-102">SYNOPSIS</span></span>


## <span data-ttu-id="a721f-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a721f-103">SYNTAX</span></span>

### <span data-ttu-id="a721f-104">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a721f-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a721f-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a721f-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a721f-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="a721f-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="a721f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a721f-107">DESCRIPTION</span></span>
<span data-ttu-id="a721f-108">Обновление вычислительной квоты</span><span class="sxs-lookup"><span data-stu-id="a721f-108">Update a Compute Quota</span></span>

## <span data-ttu-id="a721f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a721f-109">EXAMPLES</span></span>

### <span data-ttu-id="a721f-110">Пример 1: Настройка свойств существующей вычислительной квоты</span><span class="sxs-lookup"><span data-stu-id="a721f-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="a721f-111">Задайте параметры, указанные в командной строке.</span><span class="sxs-lookup"><span data-stu-id="a721f-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="a721f-112">По умолчанию для всех параметров не установлено значение 0</span><span class="sxs-lookup"><span data-stu-id="a721f-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="a721f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a721f-113">PARAMETERS</span></span>

### <span data-ttu-id="a721f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a721f-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="a721f-115">-NewQuota</span><span class="sxs-lookup"><span data-stu-id="a721f-115">-NewQuota</span></span>
<span data-ttu-id="a721f-116">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NEWQUOTA и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a721f-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a721f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a721f-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="a721f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a721f-118">-Confirm</span></span>
<span data-ttu-id="a721f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a721f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a721f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a721f-120">-WhatIf</span></span>
<span data-ttu-id="a721f-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a721f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a721f-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a721f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a721f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a721f-123">CommonParameters</span></span>
<span data-ttu-id="a721f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a721f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a721f-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a721f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a721f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a721f-126">INPUTS</span></span>

### <span data-ttu-id="a721f-127">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="a721f-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="a721f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a721f-128">OUTPUTS</span></span>

### <span data-ttu-id="a721f-129">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="a721f-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="a721f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a721f-130">NOTES</span></span>

<span data-ttu-id="a721f-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a721f-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a721f-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a721f-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a721f-133">NEWQUOTA <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="a721f-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="a721f-134">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a721f-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a721f-135">`[AvailabilitySetCount <Int32?>]`: Максимально допустимое количество наборов доступности.</span><span class="sxs-lookup"><span data-stu-id="a721f-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="a721f-136">`[CoresLimit <Int32?>]`: Максимально допустимое число ядер.</span><span class="sxs-lookup"><span data-stu-id="a721f-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="a721f-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Максимальное количество управляемых дисков и снимков типа Premium разрешено.</span><span class="sxs-lookup"><span data-stu-id="a721f-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="a721f-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Максимально допустимое количество управляемых дисков и снимков типа "Стандартный".</span><span class="sxs-lookup"><span data-stu-id="a721f-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="a721f-139">`[VMScaleSetCount <Int32?>]`: Максимальное количество допустимых наборов шкал.</span><span class="sxs-lookup"><span data-stu-id="a721f-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="a721f-140">`[VirtualMachineCount <Int32?>]`: Максимально допустимое количество виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a721f-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="a721f-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a721f-141">RELATED LINKS</span></span>

