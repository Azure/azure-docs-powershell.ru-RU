---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: ea8b069be4b153e6e4ca295a917e1c3e81629094
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914218"
---
# <span data-ttu-id="5a74e-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5a74e-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="5a74e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a74e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a74e-103">Удаление диска с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a74e-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a74e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a74e-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a74e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a74e-105">DESCRIPTION</span></span>
<span data-ttu-id="5a74e-106">Командлет **Remove-AzureRmVMDataDisk** удаляет диск с данными из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5a74e-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="5a74e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a74e-107">EXAMPLES</span></span>

### <span data-ttu-id="5a74e-108">Пример 1: удаление диска с данными из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5a74e-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="5a74e-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="5a74e-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="5a74e-110">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5a74e-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="5a74e-111">Вторая команда удаляет диск данных с именем Disk3 из виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5a74e-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="5a74e-112">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5a74e-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="5a74e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a74e-113">PARAMETERS</span></span>

### <span data-ttu-id="5a74e-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="5a74e-114">-DataDiskNames</span></span>
<span data-ttu-id="5a74e-115">Задает имена одного или нескольких дисков данных, которые удаляют этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a74e-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5a74e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a74e-116">-DefaultProfile</span></span>
<span data-ttu-id="5a74e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a74e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a74e-118">-VM</span><span class="sxs-lookup"><span data-stu-id="5a74e-118">-VM</span></span>
<span data-ttu-id="5a74e-119">Указывает локальный объект виртуальной машины, из которого нужно удалить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="5a74e-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="5a74e-120">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a74e-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="5a74e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a74e-121">-Confirm</span></span>
<span data-ttu-id="5a74e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a74e-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="5a74e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a74e-123">-WhatIf</span></span>
<span data-ttu-id="5a74e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a74e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a74e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a74e-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="5a74e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a74e-126">CommonParameters</span></span>
<span data-ttu-id="5a74e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a74e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a74e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a74e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a74e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a74e-129">INPUTS</span></span>

### <span data-ttu-id="5a74e-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5a74e-130">PSVirtualMachine</span></span>
<span data-ttu-id="5a74e-131">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5a74e-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="5a74e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a74e-132">OUTPUTS</span></span>

### <span data-ttu-id="5a74e-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5a74e-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5a74e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a74e-134">NOTES</span></span>

## <span data-ttu-id="5a74e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a74e-135">RELATED LINKS</span></span>

[<span data-ttu-id="5a74e-136">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5a74e-136">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="5a74e-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a74e-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


