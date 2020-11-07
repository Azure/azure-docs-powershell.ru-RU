---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 3529ca1d26504558036f3496c9bc75ec10e666ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911414"
---
# <span data-ttu-id="1af6e-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1af6e-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="1af6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1af6e-102">SYNOPSIS</span></span>
<span data-ttu-id="1af6e-103">Удаление диска с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1af6e-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="1af6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1af6e-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af6e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af6e-105">DESCRIPTION</span></span>
<span data-ttu-id="1af6e-106">Командлет **Remove-AzVMDataDisk** удаляет диск с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1af6e-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="1af6e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1af6e-107">EXAMPLES</span></span>

### <span data-ttu-id="1af6e-108">Пример 1: удаление диска с данными из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1af6e-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="1af6e-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="1af6e-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="1af6e-110">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1af6e-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="1af6e-111">Вторая команда удаляет диск данных с именем Disk3 из виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="1af6e-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="1af6e-112">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1af6e-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="1af6e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1af6e-113">PARAMETERS</span></span>

### <span data-ttu-id="1af6e-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="1af6e-114">-DataDiskNames</span></span>
<span data-ttu-id="1af6e-115">Задает имена одного или нескольких дисков данных, которые удаляют этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1af6e-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1af6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af6e-116">-DefaultProfile</span></span>
<span data-ttu-id="1af6e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af6e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af6e-118">-VM</span><span class="sxs-lookup"><span data-stu-id="1af6e-118">-VM</span></span>
<span data-ttu-id="1af6e-119">Указывает локальный объект виртуальной машины, из которого нужно удалить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="1af6e-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="1af6e-120">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="1af6e-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1af6e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1af6e-121">-Confirm</span></span>
<span data-ttu-id="1af6e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1af6e-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="1af6e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af6e-123">-WhatIf</span></span>
<span data-ttu-id="1af6e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1af6e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1af6e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1af6e-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="1af6e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af6e-126">CommonParameters</span></span>
<span data-ttu-id="1af6e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1af6e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af6e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af6e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af6e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1af6e-129">INPUTS</span></span>

### <span data-ttu-id="1af6e-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1af6e-130">PSVirtualMachine</span></span>
<span data-ttu-id="1af6e-131">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1af6e-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="1af6e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af6e-132">OUTPUTS</span></span>

### <span data-ttu-id="1af6e-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1af6e-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1af6e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1af6e-134">NOTES</span></span>

## <span data-ttu-id="1af6e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af6e-135">RELATED LINKS</span></span>

[<span data-ttu-id="1af6e-136">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1af6e-136">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="1af6e-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1af6e-137">Get-AzVM</span></span>](./Get-AzVM.md)


