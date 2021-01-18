---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519496"
---
# <span data-ttu-id="531e0-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="531e0-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="531e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531e0-102">SYNOPSIS</span></span>
<span data-ttu-id="531e0-103">Удаляет диск данных из набора виртуальных машин (VM)</span><span class="sxs-lookup"><span data-stu-id="531e0-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="531e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="531e0-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="531e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="531e0-105">DESCRIPTION</span></span>
<span data-ttu-id="531e0-106">**Cmdlet Remove-AzVmssVMDataDisk** удаляет диск данных из набора VM-шкалы</span><span class="sxs-lookup"><span data-stu-id="531e0-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="531e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="531e0-107">EXAMPLES</span></span>

### <span data-ttu-id="531e0-108">Пример 1. Удаление диска данных из набора VM-шкал</span><span class="sxs-lookup"><span data-stu-id="531e0-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="531e0-109">Первая команда получает существующее VMS-решение, заданное именем группы ресурсов, именем вим-за именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="531e0-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="531e0-110">Вторая команда удаляет диск данных lun 0 из VM-шкалы, храняной в $VmssVM Последняя команда обновляет VMSs VM со снятым диском данных.</span><span class="sxs-lookup"><span data-stu-id="531e0-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="531e0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="531e0-111">PARAMETERS</span></span>

### <span data-ttu-id="531e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531e0-112">-DefaultProfile</span></span>
<span data-ttu-id="531e0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="531e0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="531e0-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="531e0-114">-Lun</span></span>
<span data-ttu-id="531e0-115">Определяет логическую единицу диска.</span><span class="sxs-lookup"><span data-stu-id="531e0-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="531e0-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="531e0-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="531e0-117">Профиль виртуальной машины настроен в VM-профиле.</span><span class="sxs-lookup"><span data-stu-id="531e0-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="531e0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531e0-118">CommonParameters</span></span>
<span data-ttu-id="531e0-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531e0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531e0-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="531e0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531e0-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="531e0-121">INPUTS</span></span>

### <span data-ttu-id="531e0-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="531e0-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="531e0-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="531e0-123">OUTPUTS</span></span>

### <span data-ttu-id="531e0-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="531e0-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="531e0-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="531e0-125">NOTES</span></span>

## <span data-ttu-id="531e0-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="531e0-126">RELATED LINKS</span></span>
