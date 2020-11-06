---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMDataDisk.md
ms.openlocfilehash: 6eb86e0c2ddb8c5e3a46cf10f98bcea52ba03dd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566544"
---
# <span data-ttu-id="f744e-101">New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f744e-101">New-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="f744e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f744e-102">SYNOPSIS</span></span>
<span data-ttu-id="f744e-103">Создание объекта диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="f744e-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f744e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f744e-104">SYNTAX</span></span>

### <span data-ttu-id="f744e-105">NormalDiskParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f744e-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f744e-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f744e-106">ManagedDiskParameterSetName</span></span>
```
New-AzureRmVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f744e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f744e-107">DESCRIPTION</span></span>
<span data-ttu-id="f744e-108">Командлет **New-AzureRmVMDataDisk** создает объект диска локальных данных для виртуальной машины или Vmss ВМ.</span><span class="sxs-lookup"><span data-stu-id="f744e-108">The **New-AzureRmVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="f744e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f744e-109">EXAMPLES</span></span>

### <span data-ttu-id="f744e-110">Пример 1: Добавление управляемого диска с данными к виртуальной машине Vmss.</span><span class="sxs-lookup"><span data-stu-id="f744e-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="f744e-111">Первая команда получает существующий управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="f744e-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="f744e-112">Следующая команда создает дисковый объект данных с управляемым диском.</span><span class="sxs-lookup"><span data-stu-id="f744e-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="f744e-113">Следующая команда возвращает существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f744e-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f744e-114">Последняя команда обновляет виртуальную машину Vmss, добавляя новый диск с данными.</span><span class="sxs-lookup"><span data-stu-id="f744e-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="f744e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f744e-115">PARAMETERS</span></span>

### <span data-ttu-id="f744e-116">-Caching</span><span class="sxs-lookup"><span data-stu-id="f744e-116">-Caching</span></span>
<span data-ttu-id="f744e-117">Кэширование диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="f744e-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f744e-118">-CreateOption</span></span>
<span data-ttu-id="f744e-119">Параметр создания диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="f744e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f744e-120">-DefaultProfile</span></span>
<span data-ttu-id="f744e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f744e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f744e-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="f744e-122">-DiskSizeInGB</span></span>
<span data-ttu-id="f744e-123">Размер диска данных виртуальной машины в ГБ.</span><span class="sxs-lookup"><span data-stu-id="f744e-123">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="f744e-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="f744e-124">-Lun</span></span>
<span data-ttu-id="f744e-125">LUN диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-125">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="f744e-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f744e-126">-ManagedDiskId</span></span>
<span data-ttu-id="f744e-127">Идентификатор управляемого диска для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-127">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="f744e-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f744e-128">-Name</span></span>
<span data-ttu-id="f744e-129">Имя диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="f744e-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="f744e-130">-SourceImageUri</span></span>
<span data-ttu-id="f744e-131">URI исходного образа диска операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-131">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="f744e-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f744e-132">-StorageAccountType</span></span>
<span data-ttu-id="f744e-133">Тип учетной записи управляемого диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="f744e-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="f744e-134">-VhdUri</span></span>
<span data-ttu-id="f744e-135">URI виртуального жесткого диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f744e-135">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="f744e-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="f744e-136">-WriteAccelerator</span></span>
<span data-ttu-id="f744e-137">Указывает, следует ли включить или отключить WriteAccelerator на диске с управляемыми данными.</span><span class="sxs-lookup"><span data-stu-id="f744e-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="f744e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f744e-138">CommonParameters</span></span>
<span data-ttu-id="f744e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f744e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f744e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f744e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f744e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f744e-141">INPUTS</span></span>

### <span data-ttu-id="f744e-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f744e-142">System.Int32</span></span>

### <span data-ttu-id="f744e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f744e-143">System.String</span></span>

### <span data-ttu-id="f744e-144">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="f744e-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="f744e-145">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f744e-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f744e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f744e-146">OUTPUTS</span></span>

### <span data-ttu-id="f744e-147">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="f744e-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="f744e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f744e-148">NOTES</span></span>

## <span data-ttu-id="f744e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f744e-149">RELATED LINKS</span></span>
