---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229025"
---
# <span data-ttu-id="2622f-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="2622f-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="2622f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2622f-102">SYNOPSIS</span></span>
<span data-ttu-id="2622f-103">Обновляет состояние VMS-оборудования.</span><span class="sxs-lookup"><span data-stu-id="2622f-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="2622f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2622f-104">SYNTAX</span></span>

### <span data-ttu-id="2622f-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2622f-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2622f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2622f-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2622f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2622f-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2622f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2622f-108">DESCRIPTION</span></span>
<span data-ttu-id="2622f-109">Обновляет состояние VMS-оборудования.</span><span class="sxs-lookup"><span data-stu-id="2622f-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="2622f-110">На данный момент единственным разрешенным обновлением является добавление управляемого диска данных.</span><span class="sxs-lookup"><span data-stu-id="2622f-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="2622f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2622f-111">EXAMPLES</span></span>

### <span data-ttu-id="2622f-112">Пример 1. Добавление диска управляемых данных в VMSs VM с помощью New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2622f-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="2622f-113">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="2622f-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="2622f-114">Следующая команда создает объект на диске данных с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="2622f-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="2622f-115">Следующая команда получает существующий VMS-проект, который задается именем группы ресурсов, именем вим-замы и именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2622f-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="2622f-116">Конечная команда обновляет VMSS VM, добавляя новый диск данных.</span><span class="sxs-lookup"><span data-stu-id="2622f-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="2622f-117">Пример 2. Добавление диска управляемых данных в VMSs VM с помощью Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2622f-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="2622f-118">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="2622f-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="2622f-119">Следующая команда получает существующий VMS-проект, который задается именем группы ресурсов, именем вим-замы и именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2622f-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="2622f-120">Следующая команда добавляет управляемый диск в VMSs VM, которые хранятся в $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="2622f-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="2622f-121">Конечная команда обновляет VMSs VM с добавленным диском данных.</span><span class="sxs-lookup"><span data-stu-id="2622f-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="2622f-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2622f-122">Example 3</span></span>

<span data-ttu-id="2622f-123">Обновляет состояние VMS-оборудования.</span><span class="sxs-lookup"><span data-stu-id="2622f-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="2622f-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2622f-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="2622f-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2622f-125">PARAMETERS</span></span>

### <span data-ttu-id="2622f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2622f-126">-AsJob</span></span>
<span data-ttu-id="2622f-127">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2622f-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2622f-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="2622f-128">-DataDisk</span></span>

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

### <span data-ttu-id="2622f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2622f-129">-DefaultProfile</span></span>
<span data-ttu-id="2622f-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2622f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2622f-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2622f-131">-InstanceId</span></span>
<span data-ttu-id="2622f-132">Указывает ИД экземпляра VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="2622f-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="2622f-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="2622f-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="2622f-134">Указывает на то, что набор виртуальных машин (VM) не следует рассматривать для удаления во время масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2622f-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="2622f-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="2622f-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="2622f-136">Указывает на то, что обновления модели или действия (включая масштаб) в VMSS не должны применяться к VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="2622f-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="2622f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2622f-137">-ResourceGroupName</span></span>
<span data-ttu-id="2622f-138">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="2622f-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="2622f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2622f-139">-ResourceId</span></span>
<span data-ttu-id="2622f-140">ИД ресурса для набора виртуальных машин (VM)</span><span class="sxs-lookup"><span data-stu-id="2622f-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="2622f-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2622f-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2622f-142">Набор локальных виртуальных машин для набора VM-объектов</span><span class="sxs-lookup"><span data-stu-id="2622f-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="2622f-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2622f-143">-VMScaleSetName</span></span>
<span data-ttu-id="2622f-144">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2622f-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="2622f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2622f-145">-Confirm</span></span>
<span data-ttu-id="2622f-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2622f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2622f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2622f-147">-WhatIf</span></span>
<span data-ttu-id="2622f-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2622f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2622f-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2622f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2622f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2622f-150">CommonParameters</span></span>
<span data-ttu-id="2622f-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2622f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2622f-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2622f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2622f-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2622f-153">INPUTS</span></span>

### <span data-ttu-id="2622f-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2622f-154">System.String</span></span>

### <span data-ttu-id="2622f-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="2622f-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="2622f-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2622f-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2622f-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2622f-157">OUTPUTS</span></span>

### <span data-ttu-id="2622f-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2622f-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2622f-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2622f-159">NOTES</span></span>

## <span data-ttu-id="2622f-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2622f-160">RELATED LINKS</span></span>
