---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078456"
---
# <span data-ttu-id="44c1d-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="44c1d-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="44c1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="44c1d-103">Добавляет диск с данными в виртуальную машину Vmss.</span><span class="sxs-lookup"><span data-stu-id="44c1d-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="44c1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44c1d-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44c1d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c1d-105">DESCRIPTION</span></span>
<span data-ttu-id="44c1d-106">Командлет **Add-AzVmssVMDataDisk** добавляет диск данных в виртуальную машину Vmss.</span><span class="sxs-lookup"><span data-stu-id="44c1d-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="44c1d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44c1d-107">EXAMPLES</span></span>

### <span data-ttu-id="44c1d-108">Пример 1: Добавление управляемого диска с данными к виртуальной машине Vmss.</span><span class="sxs-lookup"><span data-stu-id="44c1d-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="44c1d-109">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="44c1d-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="44c1d-110">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44c1d-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="44c1d-111">Следующая команда добавляет управляемый диск к виртуальной машине Vmss, хранящейся локально в $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="44c1d-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="44c1d-112">Последняя команда обновляет виртуальную машину Vmss с помощью добавленного диска данных.</span><span class="sxs-lookup"><span data-stu-id="44c1d-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="44c1d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44c1d-113">PARAMETERS</span></span>

### <span data-ttu-id="44c1d-114">-Caching</span><span class="sxs-lookup"><span data-stu-id="44c1d-114">-Caching</span></span>
<span data-ttu-id="44c1d-115">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="44c1d-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="44c1d-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44c1d-117">Чтения</span><span class="sxs-lookup"><span data-stu-id="44c1d-117">ReadOnly</span></span>
- <span data-ttu-id="44c1d-118">Операцию</span><span class="sxs-lookup"><span data-stu-id="44c1d-118">ReadWrite</span></span>
- <span data-ttu-id="44c1d-119">Отсутствует значение по умолчанию: ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="44c1d-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="44c1d-120">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="44c1d-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="44c1d-121">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="44c1d-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="44c1d-122">-CreateOption</span></span>
<span data-ttu-id="44c1d-123">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="44c1d-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="44c1d-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="44c1d-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44c1d-125">Подключает.</span><span class="sxs-lookup"><span data-stu-id="44c1d-125">Attach.</span></span>
<span data-ttu-id="44c1d-126">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="44c1d-127">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="44c1d-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="44c1d-128">*VhdUri* — это все, что необходимо для того, чтобы указать платформе Azure расположение виртуального жесткого диска (VHD) для присоединения в качестве диска данных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="44c1d-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="44c1d-129">Очистку.</span><span class="sxs-lookup"><span data-stu-id="44c1d-129">Empty.</span></span>
<span data-ttu-id="44c1d-130">Укажите этот объект, чтобы создать пустой диск с данными.</span><span class="sxs-lookup"><span data-stu-id="44c1d-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="44c1d-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="44c1d-131">FromImage.</span></span>
<span data-ttu-id="44c1d-132">Укажите этот параметр, чтобы создать виртуальную машину на основе обобщенного образа или диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="44c1d-133">При указании этого параметра необходимо указать параметр *SourceImageUri* , чтобы сообщить платформе Azure о том, что расположение виртуального жесткого диска будет прикрепляться в качестве диска данных.</span><span class="sxs-lookup"><span data-stu-id="44c1d-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="44c1d-134">Параметр *VhdUri* используется в качестве расположения, которое определяет, где будет храниться диск данных, когда он используется виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="44c1d-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="44c1d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c1d-135">-DefaultProfile</span></span>
<span data-ttu-id="44c1d-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44c1d-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44c1d-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="44c1d-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="44c1d-138">Указывает идентификатор ресурса набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="44c1d-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="44c1d-139">Это может быть указано только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="44c1d-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="44c1d-140">-DiskSizeInGB</span></span>
<span data-ttu-id="44c1d-141">Задает размер пустого диска (в гигабайтах), который нужно прикрепить к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="44c1d-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="44c1d-142">-LUN</span><span class="sxs-lookup"><span data-stu-id="44c1d-142">-Lun</span></span>
<span data-ttu-id="44c1d-143">Задает логический номер устройства (LUN) для диска с данными.</span><span class="sxs-lookup"><span data-stu-id="44c1d-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="44c1d-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="44c1d-144">-ManagedDiskId</span></span>
<span data-ttu-id="44c1d-145">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="44c1d-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="44c1d-146">-StorageAccountType</span></span>
<span data-ttu-id="44c1d-147">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="44c1d-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="44c1d-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="44c1d-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="44c1d-149">Указывает локальный объект ВИРТУАЛЬНОЙ машины, на который нужно добавить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="44c1d-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="44c1d-150">Вы можете использовать командлет **Get-AzVmssVM** , чтобы получить объект ВМ для задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="44c1d-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="44c1d-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="44c1d-151">-WriteAccelerator</span></span>
<span data-ttu-id="44c1d-152">Указывает, следует ли включить или отключить WriteAccelerator на диске с управляемыми данными.</span><span class="sxs-lookup"><span data-stu-id="44c1d-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="44c1d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c1d-153">CommonParameters</span></span>
<span data-ttu-id="44c1d-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44c1d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c1d-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44c1d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c1d-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44c1d-156">INPUTS</span></span>

### <span data-ttu-id="44c1d-157">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="44c1d-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="44c1d-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44c1d-158">System.Int32</span></span>

### <span data-ttu-id="44c1d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="44c1d-159">System.String</span></span>

### <span data-ttu-id="44c1d-160">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="44c1d-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="44c1d-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c1d-161">OUTPUTS</span></span>

### <span data-ttu-id="44c1d-162">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="44c1d-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="44c1d-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="44c1d-163">NOTES</span></span>

## <span data-ttu-id="44c1d-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44c1d-164">RELATED LINKS</span></span>
