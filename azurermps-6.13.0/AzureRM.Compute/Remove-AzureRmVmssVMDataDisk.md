---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: 5c82c2dfb852cd6c3d397b34e90d9a611ff0efaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568942"
---
# <span data-ttu-id="eafe7-101">Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="eafe7-101">Remove-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="eafe7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eafe7-102">SYNOPSIS</span></span>
<span data-ttu-id="eafe7-103">Удаление диска с данными из виртуальной машины, установленной на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="eafe7-103">Removes a data disk from a virtual machine scale set VM</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafe7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eafe7-104">SYNTAX</span></span>

```
Remove-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafe7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafe7-105">DESCRIPTION</span></span>
<span data-ttu-id="eafe7-106">Командлет **Remove-AzureRmVmssVMDataDisk** удаляет диск с данными из виртуальной машины с набором масштабирования VM.</span><span class="sxs-lookup"><span data-stu-id="eafe7-106">The **Remove-AzureRmVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="eafe7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eafe7-107">EXAMPLES</span></span>

### <span data-ttu-id="eafe7-108">Пример 1: удаление диска с данными из множества виртуальных машин на основе масштабирования</span><span class="sxs-lookup"><span data-stu-id="eafe7-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzureRmVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="eafe7-109">Первая команда getsan существующую виртуальную машину Vmss, заданную именем группы ресурсов, именем Vmss и ИДЕНТИФИКАТОРом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="eafe7-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="eafe7-110">Вторая команда удаляет LUN диска данных 0 из виртуальной машины, хранящейся в $VmssVM последнюю команду обновляет виртуальную машину Vmss с удаленным диском с данными.</span><span class="sxs-lookup"><span data-stu-id="eafe7-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="eafe7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eafe7-111">PARAMETERS</span></span>

### <span data-ttu-id="eafe7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafe7-112">-DefaultProfile</span></span>
<span data-ttu-id="eafe7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eafe7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eafe7-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="eafe7-114">-Lun</span></span>
<span data-ttu-id="eafe7-115">Задает логический номер устройства для диска.</span><span class="sxs-lookup"><span data-stu-id="eafe7-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="eafe7-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eafe7-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="eafe7-117">Профиль виртуальной машины для задания масштаба виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="eafe7-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eafe7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafe7-118">CommonParameters</span></span>
<span data-ttu-id="eafe7-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eafe7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafe7-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafe7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafe7-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eafe7-121">INPUTS</span></span>

### <span data-ttu-id="eafe7-122">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eafe7-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="eafe7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafe7-123">OUTPUTS</span></span>

### <span data-ttu-id="eafe7-124">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eafe7-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="eafe7-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="eafe7-125">NOTES</span></span>

## <span data-ttu-id="eafe7-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eafe7-126">RELATED LINKS</span></span>
