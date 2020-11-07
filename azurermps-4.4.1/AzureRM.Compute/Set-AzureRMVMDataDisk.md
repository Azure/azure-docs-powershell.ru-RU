---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 3bc870be1628f5fbf22042155e6a889dbdaadc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732063"
---
# <span data-ttu-id="0e496-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e496-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0e496-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e496-102">SYNOPSIS</span></span>
<span data-ttu-id="0e496-103">Изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e496-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e496-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e496-104">SYNTAX</span></span>

### <span data-ttu-id="0e496-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="0e496-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e496-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="0e496-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e496-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e496-107">DESCRIPTION</span></span>
<span data-ttu-id="0e496-108">Командлет **Set-AzureRmVMDataDisk** изменяет свойства диска данных виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e496-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0e496-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e496-109">EXAMPLES</span></span>

### <span data-ttu-id="0e496-110">Пример 1: изменение режима кэширования на диске с данными</span><span class="sxs-lookup"><span data-stu-id="0e496-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="0e496-111">Первая команда получает виртуальную машину с именем ContosoVM07 с помощью **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="0e496-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="0e496-112">Команда сохраняет его в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="0e496-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="0e496-113">Вторая команда изменяет режим кэширования для диска данных с именем DataDisk01 на виртуальной машине в $VM.</span><span class="sxs-lookup"><span data-stu-id="0e496-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="0e496-114">Команда передает результат в командлет Update-AzureRmVM, который реализует изменения.</span><span class="sxs-lookup"><span data-stu-id="0e496-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="0e496-115">Изменение режима наведения денежных средств приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e496-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="0e496-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e496-116">PARAMETERS</span></span>

### <span data-ttu-id="0e496-117">-Caching</span><span class="sxs-lookup"><span data-stu-id="0e496-117">-Caching</span></span>
<span data-ttu-id="0e496-118">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="0e496-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0e496-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0e496-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e496-120">Чтения</span><span class="sxs-lookup"><span data-stu-id="0e496-120">ReadOnly</span></span>
- <span data-ttu-id="0e496-121">Операцию</span><span class="sxs-lookup"><span data-stu-id="0e496-121">ReadWrite</span></span>

<span data-ttu-id="0e496-122">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0e496-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="0e496-123">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e496-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="0e496-124">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="0e496-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="0e496-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e496-125">-DefaultProfile</span></span>
<span data-ttu-id="0e496-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e496-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e496-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0e496-127">-DiskSizeInGB</span></span>
<span data-ttu-id="0e496-128">Задает размер (в гигабайтах) для диска данных.</span><span class="sxs-lookup"><span data-stu-id="0e496-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="0e496-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="0e496-129">-Lun</span></span>
<span data-ttu-id="0e496-130">Задает логический номер устройства (LUN) диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0e496-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e496-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e496-131">-Name</span></span>
<span data-ttu-id="0e496-132">Указывает имя диска данных, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0e496-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0e496-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0e496-133">-StorageAccountType</span></span>
<span data-ttu-id="0e496-134">Тип учетной записи управляемого диска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e496-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e496-135">-VM</span><span class="sxs-lookup"><span data-stu-id="0e496-135">-VM</span></span>
<span data-ttu-id="0e496-136">Указывает виртуальную машину, для которой этот командлет изменяет диск данных.</span><span class="sxs-lookup"><span data-stu-id="0e496-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="0e496-137">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="0e496-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="0e496-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e496-138">CommonParameters</span></span>
<span data-ttu-id="0e496-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e496-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e496-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e496-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e496-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e496-141">INPUTS</span></span>

## <span data-ttu-id="0e496-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e496-142">OUTPUTS</span></span>

## <span data-ttu-id="0e496-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e496-143">NOTES</span></span>

## <span data-ttu-id="0e496-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e496-144">RELATED LINKS</span></span>

[<span data-ttu-id="0e496-145">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0e496-145">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0e496-146">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0e496-146">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


