---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245610"
---
# <span data-ttu-id="59526-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="59526-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="59526-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59526-102">SYNOPSIS</span></span>
<span data-ttu-id="59526-103">Удаление диска с данными из виртуальной машины, установленной на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="59526-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="59526-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59526-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59526-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59526-105">DESCRIPTION</span></span>
<span data-ttu-id="59526-106">Командлет **Remove-AzVmssVMDataDisk** удаляет диск с данными из виртуальной машины с набором масштабирования VM.</span><span class="sxs-lookup"><span data-stu-id="59526-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="59526-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59526-107">EXAMPLES</span></span>

### <span data-ttu-id="59526-108">Пример 1: удаление диска с данными из множества виртуальных машин на основе масштабирования</span><span class="sxs-lookup"><span data-stu-id="59526-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="59526-109">Первая команда getsan существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="59526-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="59526-110">Вторая команда удаляет LUN диска данных 0 из виртуальной машины, хранящейся в $VmssVM последнюю команду обновляет виртуальную машину Vmss с удаленным диском с данными.</span><span class="sxs-lookup"><span data-stu-id="59526-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="59526-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59526-111">PARAMETERS</span></span>

### <span data-ttu-id="59526-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59526-112">-DefaultProfile</span></span>
<span data-ttu-id="59526-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59526-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59526-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="59526-114">-Lun</span></span>
<span data-ttu-id="59526-115">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="59526-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59526-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="59526-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="59526-117">Профиль виртуальной машины для задания масштаба виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="59526-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59526-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59526-118">CommonParameters</span></span>
<span data-ttu-id="59526-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59526-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59526-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59526-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59526-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59526-121">INPUTS</span></span>

### <span data-ttu-id="59526-122">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="59526-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="59526-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59526-123">OUTPUTS</span></span>

### <span data-ttu-id="59526-124">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="59526-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="59526-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="59526-125">NOTES</span></span>

## <span data-ttu-id="59526-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59526-126">RELATED LINKS</span></span>
