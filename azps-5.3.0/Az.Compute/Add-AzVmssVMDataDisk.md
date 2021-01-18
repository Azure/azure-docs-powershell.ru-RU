---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519655"
---
# <span data-ttu-id="e4e5a-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e4e5a-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="e4e5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e5a-103">Добавляет диск данных в VMSs VM.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="e4e5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4e5a-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4e5a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e5a-106">**Cmdlet Add-AzVmssVMDataDisk** добавляет диск данных в VMSs VM.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="e4e5a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4e5a-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e5a-108">Пример 1. Добавление диска управляемых данных в VMSS-модем.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="e4e5a-109">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="e4e5a-110">Следующая команда получает существующий VMS-проект, который задается именем группы ресурсов, именем вим-замы и именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e4e5a-111">Следующая команда добавляет управляемый диск в VMSs VM, которые хранятся в $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="e4e5a-112">Конечная команда обновляет VMSs VM с добавленным диском данных.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="e4e5a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4e5a-113">PARAMETERS</span></span>

### <span data-ttu-id="e4e5a-114">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="e4e5a-114">-Caching</span></span>
<span data-ttu-id="e4e5a-115">Определяет режим кэшации диска.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="e4e5a-116">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="e4e5a-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4e5a-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e4e5a-117">ReadOnly</span></span>
- <span data-ttu-id="e4e5a-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4e5a-118">ReadWrite</span></span>
- <span data-ttu-id="e4e5a-119">Значением по умолчанию не является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="e4e5a-120">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="e4e5a-121">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e4e5a-122">-CreateOption</span></span>
<span data-ttu-id="e4e5a-123">Указывает, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="e4e5a-124">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="e4e5a-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4e5a-125">Вложите.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-125">Attach.</span></span>
<span data-ttu-id="e4e5a-126">Укажите этот параметр, чтобы создать виртуальную машину на специализированном диске.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e4e5a-127">При указании этого параметра не укажите параметр *SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="e4e5a-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e4e5a-128">Для *того* чтобы указать платформе Azure расположение виртуального жесткого диска (VHD), который нужно прикрепить в качестве диска данных к виртуальной машине, достаточно знать VHDUri.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="e4e5a-129">"Пустая".</span><span class="sxs-lookup"><span data-stu-id="e4e5a-129">Empty.</span></span>
<span data-ttu-id="e4e5a-130">Укажите это, чтобы создать пустой диск данных.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="e4e5a-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-131">FromImage.</span></span>
<span data-ttu-id="e4e5a-132">Укажите этот параметр, чтобы создать виртуальную машину на общем изображении или диске.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="e4e5a-133">При указании этого параметра необходимо также указать параметр *SourceImageUri,* чтобы указать платформе Azure расположение VHD, который нужно прикрепить как диск данных.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="e4e5a-134">Параметр *VhdUri* используется в качестве расположения, определяющих, где будет храниться VHD-диск данных при его использования виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e5a-135">-DefaultProfile</span></span>
<span data-ttu-id="e4e5a-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4e5a-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e4e5a-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e4e5a-138">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e4e5a-139">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-139">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e4e5a-140">-DiskSizeInGB</span></span>
<span data-ttu-id="e4e5a-141">Определяет размер (в гигабайтах) пустого диска, который нужно прикрепить к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="e4e5a-142">-Lun</span></span>
<span data-ttu-id="e4e5a-143">Определяет логический номер единицы (LUN) для диска данных.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e4e5a-144">-ManagedDiskId</span></span>
<span data-ttu-id="e4e5a-145">Определяет ИД управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e4e5a-146">-StorageAccountType</span></span>
<span data-ttu-id="e4e5a-147">Определяет тип учетной записи хранения управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-147">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e4e5a-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e4e5a-149">Определяет локальный масштаб виртуальной машины, для которого нужно добавить диск данных.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="e4e5a-150">Для получения объекта VM-объекта в масштабе виртуальной машины можно использовать **cmdlet Get-AzVmssVM.**</span><span class="sxs-lookup"><span data-stu-id="e4e5a-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4e5a-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e4e5a-151">-WriteAccelerator</span></span>
<span data-ttu-id="e4e5a-152">Указывает, следует ли включить или отключить WriteAccelerator на диске управляемых данных.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="e4e5a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e5a-153">CommonParameters</span></span>
<span data-ttu-id="e4e5a-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e5a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e5a-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4e5a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e5a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4e5a-156">INPUTS</span></span>

### <span data-ttu-id="e4e5a-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e4e5a-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="e4e5a-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e4e5a-158">System.Int32</span></span>

### <span data-ttu-id="e4e5a-159">System.String</span><span class="sxs-lookup"><span data-stu-id="e4e5a-159">System.String</span></span>

### <span data-ttu-id="e4e5a-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="e4e5a-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="e4e5a-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4e5a-161">OUTPUTS</span></span>

### <span data-ttu-id="e4e5a-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e4e5a-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e4e5a-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4e5a-163">NOTES</span></span>

## <span data-ttu-id="e4e5a-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4e5a-164">RELATED LINKS</span></span>
