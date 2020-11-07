---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: bc24cab117a3ada64c4e64118b4b9b86ebffef55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721616"
---
# <span data-ttu-id="38c1a-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="38c1a-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="38c1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="38c1a-103">Обновляет состояние виртуальной машины Vmss.</span><span class="sxs-lookup"><span data-stu-id="38c1a-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="38c1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38c1a-104">SYNTAX</span></span>

### <span data-ttu-id="38c1a-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38c1a-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c1a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="38c1a-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c1a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="38c1a-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c1a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="38c1a-109">Обновляет состояние виртуальной машины Vmss.</span><span class="sxs-lookup"><span data-stu-id="38c1a-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="38c1a-110">Сейчас единственным разрешенным обновлением является добавление диска управляемого данных.</span><span class="sxs-lookup"><span data-stu-id="38c1a-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="38c1a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38c1a-111">EXAMPLES</span></span>

### <span data-ttu-id="38c1a-112">Пример 1: Добавление управляемого диска с данными к виртуальной машине Vmss с помощью New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="38c1a-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="38c1a-113">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="38c1a-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="38c1a-114">Следующая команда создает дисковый объект данных с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="38c1a-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="38c1a-115">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="38c1a-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="38c1a-116">Последняя команда обновляет виртуальную машину Vmss, добавляя новый диск с данными.</span><span class="sxs-lookup"><span data-stu-id="38c1a-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="38c1a-117">Пример 2: Добавление управляемого диска с данными к виртуальной машине Vmss с помощью Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="38c1a-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="38c1a-118">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="38c1a-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="38c1a-119">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="38c1a-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="38c1a-120">Следующая команда добавляет управляемый диск к виртуальной машине Vmss, хранящейся локально в $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="38c1a-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="38c1a-121">Последняя команда обновляет виртуальную машину Vmss с помощью добавленного диска данных.</span><span class="sxs-lookup"><span data-stu-id="38c1a-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="38c1a-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38c1a-122">PARAMETERS</span></span>

### <span data-ttu-id="38c1a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38c1a-123">-AsJob</span></span>
<span data-ttu-id="38c1a-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="38c1a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c1a-125">-Диск</span><span class="sxs-lookup"><span data-stu-id="38c1a-125">-DataDisk</span></span>

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

### <span data-ttu-id="38c1a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c1a-126">-DefaultProfile</span></span>
<span data-ttu-id="38c1a-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38c1a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c1a-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="38c1a-128">-InstanceId</span></span>
<span data-ttu-id="38c1a-129">Указывает идентификатор экземпляра виртуальной машины VMSS.</span><span class="sxs-lookup"><span data-stu-id="38c1a-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c1a-130">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="38c1a-130">-ProtectFromScaleIn</span></span>
<span data-ttu-id="38c1a-131">Указывает на то, что при выполнении операции масштабирования не следует учитывать возможность удаления ВИРТУАЛЬНОЙ машины, установленной в виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="38c1a-131">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c1a-132">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="38c1a-132">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="38c1a-133">Указывает на то, что обновления модели или действия (включая масштабирование), инициированные в VMSS, не должны применяться к виртуальной машине VMSS.</span><span class="sxs-lookup"><span data-stu-id="38c1a-133">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c1a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c1a-134">-ResourceGroupName</span></span>
<span data-ttu-id="38c1a-135">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="38c1a-135">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c1a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c1a-136">-ResourceId</span></span>
<span data-ttu-id="38c1a-137">Идентификатор ресурса для виртуальной машины с установленным параметром "виртуальная машина"</span><span class="sxs-lookup"><span data-stu-id="38c1a-137">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="38c1a-138">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="38c1a-138">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="38c1a-139">Виртуальный объект ВИРТУАЛЬНОЙ машины, установленный на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="38c1a-139">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="38c1a-140">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="38c1a-140">-VMScaleSetName</span></span>
<span data-ttu-id="38c1a-141">Имя набора шкал виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="38c1a-141">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c1a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38c1a-142">-Confirm</span></span>
<span data-ttu-id="38c1a-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38c1a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c1a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c1a-144">-WhatIf</span></span>
<span data-ttu-id="38c1a-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38c1a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c1a-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38c1a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c1a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c1a-147">CommonParameters</span></span>
<span data-ttu-id="38c1a-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38c1a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c1a-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38c1a-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c1a-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38c1a-150">INPUTS</span></span>

### <span data-ttu-id="38c1a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="38c1a-151">System.String</span></span>

### <span data-ttu-id="38c1a-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="38c1a-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="38c1a-153">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="38c1a-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="38c1a-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38c1a-154">OUTPUTS</span></span>

### <span data-ttu-id="38c1a-155">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="38c1a-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="38c1a-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="38c1a-156">NOTES</span></span>

## <span data-ttu-id="38c1a-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38c1a-157">RELATED LINKS</span></span>
