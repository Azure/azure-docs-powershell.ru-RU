---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958883"
---
# <span data-ttu-id="bf979-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="bf979-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="bf979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf979-102">SYNOPSIS</span></span>
<span data-ttu-id="bf979-103">Задает свойства политики обновления для развертываемого обновления VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf979-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="bf979-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf979-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf979-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf979-105">DESCRIPTION</span></span>
<span data-ttu-id="bf979-106">Задает свойства политики обновления для развертываемого обновления VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf979-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="bf979-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf979-107">EXAMPLES</span></span>

### <span data-ttu-id="bf979-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf979-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="bf979-109">Эта команда задает 40 процентов для MaxBatchInstance, 35 процентов для MaxUnhealthyInstance, 30 процентов для MaxUnhealthyUpgradedInstance и 30 второго времени приостановки пакетов для локального объекта VMSS $vmss.</span><span class="sxs-lookup"><span data-stu-id="bf979-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="bf979-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf979-110">PARAMETERS</span></span>

### <span data-ttu-id="bf979-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf979-111">-DefaultProfile</span></span>
<span data-ttu-id="bf979-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf979-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf979-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="bf979-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="bf979-114">Максимальный процент всех экземпляров виртуальных машин, которые будут одновременно обновлены путем пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="bf979-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="bf979-115">Поскольку это максимально неработоспособные экземпляры в предыдущих или будущих пакетах, процент экземпляров в пакете может уменьшиться, чтобы обеспечить более высокую надежность.</span><span class="sxs-lookup"><span data-stu-id="bf979-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="bf979-116">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="bf979-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="bf979-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="bf979-118">Максимальный процент от общего числа экземпляров виртуальной машины в наборе, которые могут быть одновременно неработоспособными в результате обновления или из-за неработоспособного состояния с помощью проверки состояния виртуальной машины перед обновлением.</span><span class="sxs-lookup"><span data-stu-id="bf979-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="bf979-119">Это ограничение будет проверено перед запуском любого пакета.</span><span class="sxs-lookup"><span data-stu-id="bf979-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="bf979-120">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="bf979-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="bf979-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="bf979-122">Максимальный процент обновленных экземпляров виртуальной машины, которые могут быть признаны неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="bf979-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="bf979-123">Эта проверка будет происходить после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="bf979-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="bf979-124">Если это процентное соотношение будет превышено, будут обновлены все изменения.</span><span class="sxs-lookup"><span data-stu-id="bf979-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="bf979-125">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="bf979-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="bf979-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="bf979-127">Время ожидания между завершением обновления всех виртуальных машин одним пакетом и началом следующего.</span><span class="sxs-lookup"><span data-stu-id="bf979-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="bf979-128">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="bf979-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="bf979-129">Значение по умолчанию — 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="bf979-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf979-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bf979-131">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="bf979-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="bf979-132">Для создания объекта New-AzVmssConfig можно использовать New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="bf979-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf979-133">-Confirm</span></span>
<span data-ttu-id="bf979-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf979-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf979-135">-WhatIf</span></span>
<span data-ttu-id="bf979-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf979-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf979-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bf979-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf979-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf979-138">CommonParameters</span></span>
<span data-ttu-id="bf979-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf979-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf979-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf979-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf979-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf979-141">INPUTS</span></span>

### <span data-ttu-id="bf979-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf979-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bf979-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bf979-143">System.Int32</span></span>

### <span data-ttu-id="bf979-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bf979-144">System.String</span></span>

## <span data-ttu-id="bf979-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf979-145">OUTPUTS</span></span>

### <span data-ttu-id="bf979-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf979-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bf979-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf979-147">NOTES</span></span>

## <span data-ttu-id="bf979-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf979-148">RELATED LINKS</span></span>
