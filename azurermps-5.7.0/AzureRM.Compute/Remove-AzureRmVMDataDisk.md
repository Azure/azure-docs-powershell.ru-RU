---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732544"
---
# <span data-ttu-id="5a605-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5a605-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="5a605-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a605-102">SYNOPSIS</span></span>
<span data-ttu-id="5a605-103">Удаление диска с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a605-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a605-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a605-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a605-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a605-105">DESCRIPTION</span></span>
<span data-ttu-id="5a605-106">Командлет **Remove-AzureRmVMDataDisk** удаляет диск с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a605-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="5a605-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a605-107">EXAMPLES</span></span>

### <span data-ttu-id="5a605-108">Пример 1: удаление диска с данными из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5a605-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="5a605-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="5a605-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="5a605-110">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5a605-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="5a605-111">Вторая команда удаляет диск данных с именем Disk3 из виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5a605-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="5a605-112">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5a605-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="5a605-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a605-113">PARAMETERS</span></span>

### <span data-ttu-id="5a605-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="5a605-114">-DataDiskNames</span></span>
<span data-ttu-id="5a605-115">Задает имена одного или нескольких дисков данных, которые удаляют этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a605-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a605-116">-VM</span><span class="sxs-lookup"><span data-stu-id="5a605-116">-VM</span></span>
<span data-ttu-id="5a605-117">Указывает локальный объект виртуальной машины, из которого нужно удалить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="5a605-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="5a605-118">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a605-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="5a605-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a605-119">-Confirm</span></span>
<span data-ttu-id="5a605-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a605-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a605-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a605-121">-WhatIf</span></span>
<span data-ttu-id="5a605-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a605-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a605-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a605-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a605-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a605-124">CommonParameters</span></span>
<span data-ttu-id="5a605-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a605-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a605-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a605-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a605-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a605-127">INPUTS</span></span>

### <span data-ttu-id="5a605-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="5a605-128">None</span></span>
<span data-ttu-id="5a605-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5a605-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a605-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a605-130">OUTPUTS</span></span>

## <span data-ttu-id="5a605-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a605-131">NOTES</span></span>

## <span data-ttu-id="5a605-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a605-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a605-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5a605-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="5a605-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a605-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


