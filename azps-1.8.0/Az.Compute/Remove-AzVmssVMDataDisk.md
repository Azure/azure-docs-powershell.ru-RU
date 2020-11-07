---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 998001d931ba30c560aabd15318359d5e37baccb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731266"
---
# <span data-ttu-id="0d6dd-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0d6dd-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="0d6dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6dd-103">Удаление диска с данными из виртуальной машины, установленной на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="0d6dd-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="0d6dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d6dd-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d6dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0d6dd-106">Командлет **Remove-AzVmssVMDataDisk** удаляет диск с данными из виртуальной машины с набором масштабирования VM.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="0d6dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="0d6dd-108">Пример 1: удаление диска с данными из множества виртуальных машин на основе масштабирования</span><span class="sxs-lookup"><span data-stu-id="0d6dd-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="0d6dd-109">Первая команда getsan существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="0d6dd-110">Вторая команда удаляет LUN диска данных 0 из виртуальной машины, хранящейся в $VmssVM последнюю команду обновляет виртуальную машину Vmss с удаленным диском с данными.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="0d6dd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d6dd-111">PARAMETERS</span></span>

### <span data-ttu-id="0d6dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d6dd-112">-DefaultProfile</span></span>
<span data-ttu-id="0d6dd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d6dd-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="0d6dd-114">-Lun</span></span>
<span data-ttu-id="0d6dd-115">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="0d6dd-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0d6dd-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="0d6dd-117">Профиль виртуальной машины для задания масштаба виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="0d6dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6dd-118">CommonParameters</span></span>
<span data-ttu-id="0d6dd-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6dd-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d6dd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6dd-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d6dd-121">INPUTS</span></span>

### <span data-ttu-id="0d6dd-122">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0d6dd-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="0d6dd-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d6dd-123">OUTPUTS</span></span>

### <span data-ttu-id="0d6dd-124">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0d6dd-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="0d6dd-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d6dd-125">NOTES</span></span>

## <span data-ttu-id="0d6dd-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d6dd-126">RELATED LINKS</span></span>
