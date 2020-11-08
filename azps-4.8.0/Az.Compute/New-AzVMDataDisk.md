---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079120"
---
# <span data-ttu-id="118f6-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="118f6-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="118f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="118f6-102">SYNOPSIS</span></span>
<span data-ttu-id="118f6-103">Создание объекта диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="118f6-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="118f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="118f6-104">SYNTAX</span></span>

### <span data-ttu-id="118f6-105">NormalDiskParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="118f6-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="118f6-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="118f6-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="118f6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="118f6-107">DESCRIPTION</span></span>
<span data-ttu-id="118f6-108">Командлет **New-AzVMDataDisk** создает объект диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="118f6-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="118f6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="118f6-109">EXAMPLES</span></span>

### <span data-ttu-id="118f6-110">Пример 1: Добавление управляемого диска с данными к виртуальной машине Vmss.</span><span class="sxs-lookup"><span data-stu-id="118f6-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="118f6-111">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="118f6-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="118f6-112">Следующая команда создает дисковый объект данных с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="118f6-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="118f6-113">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="118f6-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="118f6-114">Последняя команда обновляет виртуальную машину Vmss, добавляя новый диск с данными.</span><span class="sxs-lookup"><span data-stu-id="118f6-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="118f6-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="118f6-115">Example 2</span></span>

<span data-ttu-id="118f6-116">Создание объекта диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="118f6-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="118f6-117">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="118f6-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="118f6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="118f6-118">PARAMETERS</span></span>

### <span data-ttu-id="118f6-119">-Caching</span><span class="sxs-lookup"><span data-stu-id="118f6-119">-Caching</span></span>
<span data-ttu-id="118f6-120">Кэширование диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="118f6-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="118f6-121">-CreateOption</span></span>
<span data-ttu-id="118f6-122">Параметр создания диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-122">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="118f6-123">-DefaultProfile</span></span>
<span data-ttu-id="118f6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="118f6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="118f6-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="118f6-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="118f6-126">Идентификатор комплекта шифрования диска, управляемого виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="118f6-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="118f6-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="118f6-127">-DiskSizeInGB</span></span>
<span data-ttu-id="118f6-128">Размер диска данных виртуальной машины в ГБ.</span><span class="sxs-lookup"><span data-stu-id="118f6-128">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="118f6-129">-Lun</span></span>
<span data-ttu-id="118f6-130">LUN диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-130">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="118f6-131">-ManagedDiskId</span></span>
<span data-ttu-id="118f6-132">Идентификатор управляемого диска для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-132">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="118f6-133">-Name</span></span>
<span data-ttu-id="118f6-134">Имя диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="118f6-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="118f6-135">-SourceImageUri</span></span>
<span data-ttu-id="118f6-136">URI исходного образа диска операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-136">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="118f6-137">-StorageAccountType</span></span>
<span data-ttu-id="118f6-138">Тип учетной записи управляемого диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-138">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="118f6-139">-VhdUri</span></span>
<span data-ttu-id="118f6-140">URI виртуального жесткого диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="118f6-140">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="118f6-141">-WriteAccelerator</span></span>
<span data-ttu-id="118f6-142">Указывает, следует ли включить или отключить WriteAccelerator на диске с управляемыми данными.</span><span class="sxs-lookup"><span data-stu-id="118f6-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="118f6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="118f6-143">CommonParameters</span></span>
<span data-ttu-id="118f6-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="118f6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="118f6-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="118f6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="118f6-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="118f6-146">INPUTS</span></span>

### <span data-ttu-id="118f6-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="118f6-147">System.Int32</span></span>

### <span data-ttu-id="118f6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="118f6-148">System.String</span></span>

### <span data-ttu-id="118f6-149">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="118f6-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="118f6-150">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="118f6-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="118f6-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="118f6-151">OUTPUTS</span></span>

### <span data-ttu-id="118f6-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="118f6-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="118f6-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="118f6-153">NOTES</span></span>

## <span data-ttu-id="118f6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="118f6-154">RELATED LINKS</span></span>