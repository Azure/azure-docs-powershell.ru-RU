---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566217"
---
# <span data-ttu-id="09858-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="09858-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="09858-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09858-102">SYNOPSIS</span></span>
<span data-ttu-id="09858-103">Изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09858-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09858-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09858-104">SYNTAX</span></span>

### <span data-ttu-id="09858-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="09858-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="09858-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="09858-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="09858-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09858-107">DESCRIPTION</span></span>
<span data-ttu-id="09858-108">Командлет **Set-AzureRmVMDataDisk** изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09858-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="09858-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09858-109">EXAMPLES</span></span>

### <span data-ttu-id="09858-110">Пример 1: изменение режима кэширования на диске с данными</span><span class="sxs-lookup"><span data-stu-id="09858-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="09858-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="09858-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="09858-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="09858-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="09858-113">Вторая команда изменяет режим кэширования для диска данных с именем DataDisk01 на виртуальной машине в $VM.</span><span class="sxs-lookup"><span data-stu-id="09858-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="09858-114">Команда передает результат в командлет Update-AzureRmVM, который реализует изменения.</span><span class="sxs-lookup"><span data-stu-id="09858-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="09858-115">Изменение режима кэширования приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09858-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="09858-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09858-116">PARAMETERS</span></span>

### <span data-ttu-id="09858-117">-Caching</span><span class="sxs-lookup"><span data-stu-id="09858-117">-Caching</span></span>
<span data-ttu-id="09858-118">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="09858-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="09858-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="09858-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09858-120">Чтения</span><span class="sxs-lookup"><span data-stu-id="09858-120">ReadOnly</span></span>
- <span data-ttu-id="09858-121">Операцию</span><span class="sxs-lookup"><span data-stu-id="09858-121">ReadWrite</span></span>

<span data-ttu-id="09858-122">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="09858-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="09858-123">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="09858-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="09858-124">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="09858-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09858-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="09858-125">-DiskSizeInGB</span></span>
<span data-ttu-id="09858-126">Задает размер (в гигабайтах) для диска данных.</span><span class="sxs-lookup"><span data-stu-id="09858-126">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09858-127">-LUN</span><span class="sxs-lookup"><span data-stu-id="09858-127">-Lun</span></span>
<span data-ttu-id="09858-128">Задает логический номер устройства (LUN) диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="09858-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09858-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="09858-129">-Name</span></span>
<span data-ttu-id="09858-130">Указывает имя диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="09858-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09858-131">-VM</span><span class="sxs-lookup"><span data-stu-id="09858-131">-VM</span></span>
<span data-ttu-id="09858-132">Указывает виртуальную машину, для которой этот командлет изменяет диск данных.</span><span class="sxs-lookup"><span data-stu-id="09858-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="09858-133">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="09858-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09858-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09858-134">CommonParameters</span></span>
<span data-ttu-id="09858-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09858-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09858-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09858-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09858-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09858-137">INPUTS</span></span>

### <span data-ttu-id="09858-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="09858-138">None</span></span>
<span data-ttu-id="09858-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="09858-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09858-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09858-140">OUTPUTS</span></span>

## <span data-ttu-id="09858-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="09858-141">NOTES</span></span>

## <span data-ttu-id="09858-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09858-142">RELATED LINKS</span></span>

[<span data-ttu-id="09858-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="09858-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="09858-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="09858-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


