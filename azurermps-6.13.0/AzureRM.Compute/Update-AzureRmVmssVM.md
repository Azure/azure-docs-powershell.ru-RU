---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssVM.md
ms.openlocfilehash: 3003387b0d989d01231e7be549727ebc88158723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734156"
---
# <span data-ttu-id="3575f-101">Update-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="3575f-101">Update-AzureRmVmssVM</span></span>

## <span data-ttu-id="3575f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3575f-102">SYNOPSIS</span></span>
<span data-ttu-id="3575f-103">Обновляет состояние виртуальной машины Vmss.</span><span class="sxs-lookup"><span data-stu-id="3575f-103">Updates the state of a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3575f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3575f-104">SYNTAX</span></span>

### <span data-ttu-id="3575f-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3575f-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3575f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3575f-106">ResourceIdParameter</span></span>
```
Update-AzureRmVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3575f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3575f-107">ObjectParameter</span></span>
```
Update-AzureRmVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3575f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3575f-108">DESCRIPTION</span></span>
<span data-ttu-id="3575f-109">Обновляет состояние виртуальной машины Vmss.</span><span class="sxs-lookup"><span data-stu-id="3575f-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="3575f-110">Сейчас единственным разрешенным обновлением является добавление диска управляемого данных.</span><span class="sxs-lookup"><span data-stu-id="3575f-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="3575f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3575f-111">EXAMPLES</span></span>

### <span data-ttu-id="3575f-112">Пример 1: Добавление управляемого диска с данными к виртуальной машине Vmss с помощью New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3575f-112">Example 1: Add a managed data disk to a Vmss VM using New-AzureRmVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="3575f-113">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="3575f-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="3575f-114">Следующая команда создает дисковый объект данных с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="3575f-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="3575f-115">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3575f-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="3575f-116">Последняя команда обновляет виртуальную машину Vmss, добавляя новый диск с данными.</span><span class="sxs-lookup"><span data-stu-id="3575f-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="3575f-117">Пример 2: Добавление управляемого диска с данными к виртуальной машине Vmss с помощью Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3575f-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzureRmVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="3575f-118">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="3575f-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="3575f-119">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3575f-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="3575f-120">Следующая команда добавляет управляемый диск к виртуальной машине Vmss, хранящейся локально в $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="3575f-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="3575f-121">Последняя команда обновляет виртуальную машину Vmss с помощью добавленного диска данных.</span><span class="sxs-lookup"><span data-stu-id="3575f-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="3575f-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3575f-122">PARAMETERS</span></span>

### <span data-ttu-id="3575f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3575f-123">-AsJob</span></span>
<span data-ttu-id="3575f-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3575f-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-125">-Диск</span><span class="sxs-lookup"><span data-stu-id="3575f-125">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3575f-126">-DefaultProfile</span></span>
<span data-ttu-id="3575f-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3575f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3575f-128">-InstanceId</span></span>
<span data-ttu-id="3575f-129">Указывает идентификатор экземпляра виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="3575f-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3575f-130">-ResourceGroupName</span></span>
<span data-ttu-id="3575f-131">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="3575f-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3575f-132">-ResourceId</span></span>
<span data-ttu-id="3575f-133">Идентификатор ресурса для виртуальной машины с установленным параметром "виртуальная машина"</span><span class="sxs-lookup"><span data-stu-id="3575f-133">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-134">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="3575f-134">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="3575f-135">Виртуальный объект ВИРТУАЛЬНОЙ машины, установленный на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="3575f-135">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3575f-136">-VMScaleSetName</span></span>
<span data-ttu-id="3575f-137">Имя набора шкал виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="3575f-137">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3575f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3575f-138">-Confirm</span></span>
<span data-ttu-id="3575f-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3575f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3575f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3575f-140">-WhatIf</span></span>
<span data-ttu-id="3575f-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3575f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3575f-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3575f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3575f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3575f-143">CommonParameters</span></span>
<span data-ttu-id="3575f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3575f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3575f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3575f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3575f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3575f-146">INPUTS</span></span>

### <span data-ttu-id="3575f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3575f-147">System.String</span></span>

### <span data-ttu-id="3575f-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="3575f-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>
<span data-ttu-id="3575f-149">Параметры: Disk (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3575f-149">Parameters: DataDisk (ByValue)</span></span>

### <span data-ttu-id="3575f-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="3575f-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>
<span data-ttu-id="3575f-151">Параметры: VirtualMachineScaleSetVM (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3575f-151">Parameters: VirtualMachineScaleSetVM (ByValue)</span></span>

## <span data-ttu-id="3575f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3575f-152">OUTPUTS</span></span>

### <span data-ttu-id="3575f-153">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="3575f-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="3575f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="3575f-154">NOTES</span></span>

## <span data-ttu-id="3575f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3575f-155">RELATED LINKS</span></span>
