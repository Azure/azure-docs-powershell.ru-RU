---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915365"
---
# <span data-ttu-id="dfa65-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dfa65-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="dfa65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfa65-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa65-103">Изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dfa65-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfa65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfa65-104">SYNTAX</span></span>

### <span data-ttu-id="dfa65-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="dfa65-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfa65-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="dfa65-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa65-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfa65-107">DESCRIPTION</span></span>
<span data-ttu-id="dfa65-108">Командлет **Set-AzureRmVMDataDisk** изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dfa65-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="dfa65-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfa65-109">EXAMPLES</span></span>

### <span data-ttu-id="dfa65-110">Пример 1: изменение режима кэширования на диске с данными</span><span class="sxs-lookup"><span data-stu-id="dfa65-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="dfa65-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="dfa65-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="dfa65-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="dfa65-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="dfa65-113">Вторая команда изменяет режим кэширования для диска данных с именем DataDisk01 на виртуальной машине в $VM.</span><span class="sxs-lookup"><span data-stu-id="dfa65-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="dfa65-114">Команда передает результат в командлет Update-AzureRmVM, который реализует изменения.</span><span class="sxs-lookup"><span data-stu-id="dfa65-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="dfa65-115">Изменение режима наведения денежных средств приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dfa65-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="dfa65-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfa65-116">PARAMETERS</span></span>

### <span data-ttu-id="dfa65-117">-Caching</span><span class="sxs-lookup"><span data-stu-id="dfa65-117">-Caching</span></span>
<span data-ttu-id="dfa65-118">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="dfa65-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="dfa65-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dfa65-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfa65-120">Чтения</span><span class="sxs-lookup"><span data-stu-id="dfa65-120">ReadOnly</span></span>
- <span data-ttu-id="dfa65-121">Операцию</span><span class="sxs-lookup"><span data-stu-id="dfa65-121">ReadWrite</span></span>

<span data-ttu-id="dfa65-122">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="dfa65-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="dfa65-123">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dfa65-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="dfa65-124">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="dfa65-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="dfa65-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa65-125">-DefaultProfile</span></span>
<span data-ttu-id="dfa65-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfa65-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa65-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="dfa65-127">-DiskSizeInGB</span></span>
<span data-ttu-id="dfa65-128">Задает размер (в гигабайтах) для диска данных.</span><span class="sxs-lookup"><span data-stu-id="dfa65-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="dfa65-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="dfa65-129">-Lun</span></span>
<span data-ttu-id="dfa65-130">Задает логический номер устройства (LUN) диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dfa65-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dfa65-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dfa65-131">-Name</span></span>
<span data-ttu-id="dfa65-132">Указывает имя диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dfa65-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dfa65-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dfa65-133">-StorageAccountType</span></span>
<span data-ttu-id="dfa65-134">Тип учетной записи управляемого диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dfa65-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa65-135">-VM</span><span class="sxs-lookup"><span data-stu-id="dfa65-135">-VM</span></span>
<span data-ttu-id="dfa65-136">Указывает виртуальную машину, для которой этот командлет изменяет диск данных.</span><span class="sxs-lookup"><span data-stu-id="dfa65-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="dfa65-137">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="dfa65-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="dfa65-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dfa65-138">-WriteAccelerator</span></span>
<span data-ttu-id="dfa65-139">Указывает, следует ли включить или отключить WriteAccelerator на диске с данными.</span><span class="sxs-lookup"><span data-stu-id="dfa65-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa65-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa65-140">CommonParameters</span></span>
<span data-ttu-id="dfa65-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfa65-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa65-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa65-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa65-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfa65-143">INPUTS</span></span>

### <span data-ttu-id="dfa65-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dfa65-144">PSVirtualMachine</span></span>
<span data-ttu-id="dfa65-145">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dfa65-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="dfa65-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfa65-146">OUTPUTS</span></span>

### <span data-ttu-id="dfa65-147">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dfa65-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dfa65-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfa65-148">NOTES</span></span>

## <span data-ttu-id="dfa65-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfa65-149">RELATED LINKS</span></span>

[<span data-ttu-id="dfa65-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dfa65-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="dfa65-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="dfa65-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


