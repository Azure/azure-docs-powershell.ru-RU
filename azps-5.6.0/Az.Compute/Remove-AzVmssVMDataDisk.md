---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971443"
---
# <span data-ttu-id="5f75f-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5f75f-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="5f75f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f75f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f75f-103">Удаляет диск данных из набора виртуальных машин (VM)</span><span class="sxs-lookup"><span data-stu-id="5f75f-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="5f75f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f75f-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f75f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f75f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f75f-106">**Cmdlet Remove-AzVmssVMDataDisk** удаляет диск данных из набора VM-шкалы</span><span class="sxs-lookup"><span data-stu-id="5f75f-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="5f75f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f75f-107">EXAMPLES</span></span>

### <span data-ttu-id="5f75f-108">Пример 1. Удаление диска данных из набора VM-шкал</span><span class="sxs-lookup"><span data-stu-id="5f75f-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="5f75f-109">Первая команда получает существующий VMS-модем, заданный именем группы ресурсов, именем и именем экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5f75f-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="5f75f-110">Вторая команда удаляет диск данных lun 0 из набора VM-шкал, хранимого в $VmssVM Последняя команда обновляет VMSs VM со снятым диском данных.</span><span class="sxs-lookup"><span data-stu-id="5f75f-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="5f75f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f75f-111">PARAMETERS</span></span>

### <span data-ttu-id="5f75f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f75f-112">-DefaultProfile</span></span>
<span data-ttu-id="5f75f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f75f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f75f-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="5f75f-114">-Lun</span></span>
<span data-ttu-id="5f75f-115">Определяет логическую единицу диска.</span><span class="sxs-lookup"><span data-stu-id="5f75f-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="5f75f-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5f75f-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="5f75f-117">Профиль виртуальной машины настроен в VM-профиле.</span><span class="sxs-lookup"><span data-stu-id="5f75f-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="5f75f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f75f-118">CommonParameters</span></span>
<span data-ttu-id="5f75f-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f75f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f75f-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f75f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f75f-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f75f-121">INPUTS</span></span>

### <span data-ttu-id="5f75f-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5f75f-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="5f75f-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f75f-123">OUTPUTS</span></span>

### <span data-ttu-id="5f75f-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5f75f-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="5f75f-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f75f-125">NOTES</span></span>

## <span data-ttu-id="5f75f-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f75f-126">RELATED LINKS</span></span>
