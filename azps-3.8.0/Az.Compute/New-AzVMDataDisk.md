---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 7f67b8b6ff287a98fc505cb63c3a6eda90f46ef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065912"
---
# <span data-ttu-id="4bd98-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bd98-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="4bd98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bd98-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd98-103">Создание объекта диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="4bd98-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="4bd98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bd98-104">SYNTAX</span></span>

### <span data-ttu-id="4bd98-105">NormalDiskParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4bd98-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd98-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4bd98-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bd98-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bd98-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd98-108">Командлет **New-AzVMDataDisk** создает объект диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="4bd98-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="4bd98-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bd98-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd98-110">Пример 1: Добавление управляемого диска с данными к виртуальной машине Vmss.</span><span class="sxs-lookup"><span data-stu-id="4bd98-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="4bd98-111">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="4bd98-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="4bd98-112">Следующая команда создает дисковый объект данных с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="4bd98-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="4bd98-113">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4bd98-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="4bd98-114">Последняя команда обновляет виртуальную машину Vmss, добавляя новый диск с данными.</span><span class="sxs-lookup"><span data-stu-id="4bd98-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="4bd98-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bd98-115">PARAMETERS</span></span>

### <span data-ttu-id="4bd98-116">-Caching</span><span class="sxs-lookup"><span data-stu-id="4bd98-116">-Caching</span></span>
<span data-ttu-id="4bd98-117">Кэширование диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="4bd98-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4bd98-118">-CreateOption</span></span>
<span data-ttu-id="4bd98-119">Параметр создания диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="4bd98-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd98-120">-DefaultProfile</span></span>
<span data-ttu-id="4bd98-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd98-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd98-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="4bd98-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="4bd98-123">Идентификатор комплекта шифрования диска, управляемого виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="4bd98-123">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="4bd98-124">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4bd98-124">-DiskSizeInGB</span></span>
<span data-ttu-id="4bd98-125">Размер диска данных виртуальной машины в ГБ.</span><span class="sxs-lookup"><span data-stu-id="4bd98-125">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="4bd98-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="4bd98-126">-Lun</span></span>
<span data-ttu-id="4bd98-127">LUN диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-127">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="4bd98-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="4bd98-128">-ManagedDiskId</span></span>
<span data-ttu-id="4bd98-129">Идентификатор управляемого диска для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-129">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="4bd98-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4bd98-130">-Name</span></span>
<span data-ttu-id="4bd98-131">Имя диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-131">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="4bd98-132">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="4bd98-132">-SourceImageUri</span></span>
<span data-ttu-id="4bd98-133">URI исходного образа диска операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-133">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="4bd98-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4bd98-134">-StorageAccountType</span></span>
<span data-ttu-id="4bd98-135">Тип учетной записи управляемого диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-135">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="4bd98-136">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4bd98-136">-VhdUri</span></span>
<span data-ttu-id="4bd98-137">URI виртуального жесткого диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bd98-137">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="4bd98-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4bd98-138">-WriteAccelerator</span></span>
<span data-ttu-id="4bd98-139">Указывает, следует ли включить или отключить WriteAccelerator на диске с управляемыми данными.</span><span class="sxs-lookup"><span data-stu-id="4bd98-139">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="4bd98-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd98-140">CommonParameters</span></span>
<span data-ttu-id="4bd98-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bd98-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd98-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bd98-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd98-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bd98-143">INPUTS</span></span>

### <span data-ttu-id="4bd98-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4bd98-144">System.Int32</span></span>

### <span data-ttu-id="4bd98-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4bd98-145">System.String</span></span>

### <span data-ttu-id="4bd98-146">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="4bd98-146">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="4bd98-147">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4bd98-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4bd98-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bd98-148">OUTPUTS</span></span>

### <span data-ttu-id="4bd98-149">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bd98-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="4bd98-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bd98-150">NOTES</span></span>

## <span data-ttu-id="4bd98-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bd98-151">RELATED LINKS</span></span>
