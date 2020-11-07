---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 16c15838b07ab2589f5590128f5d948ae3cd6be0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721688"
---
# <span data-ttu-id="2ff33-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2ff33-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="2ff33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ff33-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff33-103">Изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2ff33-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="2ff33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ff33-104">SYNTAX</span></span>

### <span data-ttu-id="2ff33-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="2ff33-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ff33-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="2ff33-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ff33-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ff33-107">DESCRIPTION</span></span>
<span data-ttu-id="2ff33-108">Командлет **Set-AzVMDataDisk** изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2ff33-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="2ff33-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ff33-109">EXAMPLES</span></span>

### <span data-ttu-id="2ff33-110">Пример 1: изменение режима кэширования на диске с данными</span><span class="sxs-lookup"><span data-stu-id="2ff33-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="2ff33-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="2ff33-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="2ff33-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="2ff33-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="2ff33-113">Вторая команда изменяет режим кэширования для диска данных с именем DataDisk01 на виртуальной машине в $VM.</span><span class="sxs-lookup"><span data-stu-id="2ff33-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="2ff33-114">Команда передает результат в командлет Update-AzVM, который реализует изменения.</span><span class="sxs-lookup"><span data-stu-id="2ff33-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="2ff33-115">Изменение режима наведения денежных средств приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2ff33-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="2ff33-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ff33-116">PARAMETERS</span></span>

### <span data-ttu-id="2ff33-117">-Caching</span><span class="sxs-lookup"><span data-stu-id="2ff33-117">-Caching</span></span>
<span data-ttu-id="2ff33-118">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="2ff33-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="2ff33-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2ff33-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ff33-120">Чтения</span><span class="sxs-lookup"><span data-stu-id="2ff33-120">ReadOnly</span></span>
- <span data-ttu-id="2ff33-121">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2ff33-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="2ff33-122">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2ff33-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="2ff33-123">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="2ff33-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff33-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff33-124">-DefaultProfile</span></span>
<span data-ttu-id="2ff33-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff33-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ff33-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="2ff33-126">-DiskSizeInGB</span></span>
<span data-ttu-id="2ff33-127">Задает размер (в гигабайтах) для диска данных.</span><span class="sxs-lookup"><span data-stu-id="2ff33-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff33-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="2ff33-128">-Lun</span></span>
<span data-ttu-id="2ff33-129">Задает логический номер устройства (LUN) диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2ff33-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff33-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ff33-130">-Name</span></span>
<span data-ttu-id="2ff33-131">Указывает имя диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2ff33-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff33-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2ff33-132">-StorageAccountType</span></span>
<span data-ttu-id="2ff33-133">Тип учетной записи управляемого диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2ff33-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="2ff33-134">-VM</span><span class="sxs-lookup"><span data-stu-id="2ff33-134">-VM</span></span>
<span data-ttu-id="2ff33-135">Указывает виртуальную машину, для которой этот командлет изменяет диск данных.</span><span class="sxs-lookup"><span data-stu-id="2ff33-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="2ff33-136">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2ff33-136">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff33-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2ff33-137">-WriteAccelerator</span></span>
<span data-ttu-id="2ff33-138">Указывает, следует ли включить или отключить WriteAccelerator на диске с данными.</span><span class="sxs-lookup"><span data-stu-id="2ff33-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="2ff33-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff33-139">CommonParameters</span></span>
<span data-ttu-id="2ff33-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ff33-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff33-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ff33-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff33-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ff33-142">INPUTS</span></span>

### <span data-ttu-id="2ff33-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2ff33-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2ff33-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2ff33-144">System.String</span></span>

### <span data-ttu-id="2ff33-145">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ff33-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2ff33-146">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. Model. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, культура =" нейтрально ", PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2ff33-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="2ff33-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ff33-147">OUTPUTS</span></span>

### <span data-ttu-id="2ff33-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2ff33-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2ff33-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ff33-149">NOTES</span></span>

## <span data-ttu-id="2ff33-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ff33-150">RELATED LINKS</span></span>

[<span data-ttu-id="2ff33-151">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2ff33-151">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2ff33-152">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2ff33-152">Update-AzVM</span></span>](./Update-AzVM.md)


