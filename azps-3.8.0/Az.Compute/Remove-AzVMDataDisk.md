---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066576"
---
# <span data-ttu-id="86f85-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86f85-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="86f85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86f85-102">SYNOPSIS</span></span>
<span data-ttu-id="86f85-103">Удаление диска с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86f85-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="86f85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86f85-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f85-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f85-105">DESCRIPTION</span></span>
<span data-ttu-id="86f85-106">Командлет **Remove-AzVMDataDisk** удаляет диск с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86f85-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="86f85-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86f85-107">EXAMPLES</span></span>

### <span data-ttu-id="86f85-108">Пример 1: удаление диска с данными из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="86f85-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="86f85-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="86f85-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="86f85-110">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="86f85-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="86f85-111">Вторая команда удаляет диск данных с именем Disk3 из виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="86f85-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="86f85-112">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="86f85-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="86f85-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86f85-113">PARAMETERS</span></span>

### <span data-ttu-id="86f85-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="86f85-114">-DataDiskNames</span></span>
<span data-ttu-id="86f85-115">Задает имена одного или нескольких дисков данных, которые удаляют этот командлет.</span><span class="sxs-lookup"><span data-stu-id="86f85-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f85-116">-DefaultProfile</span></span>
<span data-ttu-id="86f85-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86f85-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f85-118">-VM</span><span class="sxs-lookup"><span data-stu-id="86f85-118">-VM</span></span>
<span data-ttu-id="86f85-119">Указывает локальный объект виртуальной машины, из которого нужно удалить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="86f85-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="86f85-120">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="86f85-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="86f85-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86f85-121">-Confirm</span></span>
<span data-ttu-id="86f85-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86f85-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f85-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f85-123">-WhatIf</span></span>
<span data-ttu-id="86f85-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86f85-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86f85-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86f85-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f85-126">CommonParameters</span></span>
<span data-ttu-id="86f85-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86f85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f85-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86f85-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f85-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86f85-129">INPUTS</span></span>

### <span data-ttu-id="86f85-130">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="86f85-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="86f85-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f85-131">OUTPUTS</span></span>

### <span data-ttu-id="86f85-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="86f85-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="86f85-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="86f85-133">NOTES</span></span>

## <span data-ttu-id="86f85-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86f85-134">RELATED LINKS</span></span>

[<span data-ttu-id="86f85-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="86f85-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="86f85-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="86f85-136">Get-AzVM</span></span>](./Get-AzVM.md)


