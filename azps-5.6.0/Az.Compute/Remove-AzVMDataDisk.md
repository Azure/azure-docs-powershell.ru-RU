---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 72ccf9994b303e9e191594f32bb2aa23f0abd9ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983288"
---
# <span data-ttu-id="dcfc3-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dcfc3-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="dcfc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfc3-103">Удаляет диск данных с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="dcfc3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dcfc3-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcfc3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcfc3-105">DESCRIPTION</span></span>
<span data-ttu-id="dcfc3-106">Для удаления диска данных с виртуальной машины будет удаляется диск данных **AzVMDataDisk.**</span><span class="sxs-lookup"><span data-stu-id="dcfc3-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="dcfc3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dcfc3-107">EXAMPLES</span></span>

### <span data-ttu-id="dcfc3-108">Пример 1. Удаление диска данных с виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="dcfc3-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="dcfc3-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью **командлета Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="dcfc3-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="dcfc3-110">Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dcfc3-111">Вторая команда удаляет диск данных с именем "Диск3" из виртуальной машины, $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="dcfc3-112">Последняя команда обновляет состояние виртуальной машины, которая хранится в $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="dcfc3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcfc3-113">PARAMETERS</span></span>

### <span data-ttu-id="dcfc3-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="dcfc3-114">-DataDiskNames</span></span>
<span data-ttu-id="dcfc3-115">Определяет имена одного или несколько дисков данных, которые удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dcfc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfc3-116">-DefaultProfile</span></span>
<span data-ttu-id="dcfc3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcfc3-118">-VM</span><span class="sxs-lookup"><span data-stu-id="dcfc3-118">-VM</span></span>
<span data-ttu-id="dcfc3-119">Определяет объект локальной виртуальной машины, из которого нужно удалить диск данных.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="dcfc3-120">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="dcfc3-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="dcfc3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcfc3-121">-Confirm</span></span>
<span data-ttu-id="dcfc3-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcfc3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcfc3-123">-WhatIf</span></span>
<span data-ttu-id="dcfc3-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcfc3-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcfc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfc3-126">CommonParameters</span></span>
<span data-ttu-id="dcfc3-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcfc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfc3-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcfc3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfc3-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcfc3-129">INPUTS</span></span>

### <span data-ttu-id="dcfc3-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="dcfc3-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dcfc3-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcfc3-131">OUTPUTS</span></span>

### <span data-ttu-id="dcfc3-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="dcfc3-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dcfc3-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dcfc3-133">NOTES</span></span>

## <span data-ttu-id="dcfc3-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcfc3-134">RELATED LINKS</span></span>

[<span data-ttu-id="dcfc3-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dcfc3-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="dcfc3-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dcfc3-136">Get-AzVM</span></span>](./Get-AzVM.md)


