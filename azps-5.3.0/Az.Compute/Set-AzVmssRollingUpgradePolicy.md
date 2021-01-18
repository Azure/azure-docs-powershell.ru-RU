---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519439"
---
# <span data-ttu-id="dd880-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="dd880-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="dd880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd880-102">SYNOPSIS</span></span>
<span data-ttu-id="dd880-103">Задает свойства политики обновления для развертыванию VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd880-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="dd880-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd880-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd880-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd880-105">DESCRIPTION</span></span>
<span data-ttu-id="dd880-106">Задает свойства политики обновления для развертыванию VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd880-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="dd880-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd880-107">EXAMPLES</span></span>

### <span data-ttu-id="dd880-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd880-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="dd880-109">Эта команда задает 40 процентов для MaxBatchInstance, 35 процентов для MaxUnhealthyInstance, 30 процентов для MaxUnhealthyUpgradedInstance и 30 второго времени приостановки пакетов для локального объекта VMSS $vmss.</span><span class="sxs-lookup"><span data-stu-id="dd880-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="dd880-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd880-110">PARAMETERS</span></span>

### <span data-ttu-id="dd880-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd880-111">-DefaultProfile</span></span>
<span data-ttu-id="dd880-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd880-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd880-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="dd880-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="dd880-114">Максимальный процент всех экземпляров виртуальных машин, которые будут одновременно обновлены путем пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="dd880-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="dd880-115">Поскольку это максимально неработоспособные экземпляры в предыдущих или будущих пакетах, процент экземпляров в пакете может снизиться, чтобы обеспечить более высокую надежность.</span><span class="sxs-lookup"><span data-stu-id="dd880-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="dd880-116">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="dd880-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="dd880-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="dd880-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="dd880-118">Максимальный процент от общего числа экземпляров виртуальной машины в наборе, которые могут одновременно неработоспособно работать либо в результате обновления, либо из-за неработоспособного состояния виртуальной машины проверяется, пока не будет установлено обновление.</span><span class="sxs-lookup"><span data-stu-id="dd880-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="dd880-119">Это ограничение будет проверено перед запуском любого пакета.</span><span class="sxs-lookup"><span data-stu-id="dd880-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="dd880-120">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="dd880-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="dd880-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="dd880-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="dd880-122">Максимальный процент обновленных экземпляров виртуальной машины, которые могут быть признаны неработоспособными.</span><span class="sxs-lookup"><span data-stu-id="dd880-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="dd880-123">Эта проверка будет происходить после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="dd880-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="dd880-124">Если это процентное соотношение будет превышено, будут обновлены все изменения.</span><span class="sxs-lookup"><span data-stu-id="dd880-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="dd880-125">Если значение не указано, задано значение 20.</span><span class="sxs-lookup"><span data-stu-id="dd880-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="dd880-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="dd880-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="dd880-127">Время ожидания между завершением обновления всех виртуальных машин одним пакетом и началом следующего.</span><span class="sxs-lookup"><span data-stu-id="dd880-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="dd880-128">Длительность должна быть указана в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="dd880-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="dd880-129">Значение по умолчанию — 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="dd880-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="dd880-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd880-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="dd880-131">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="dd880-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="dd880-132">Для создания объекта New-AzVmssConfig можно использовать New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="dd880-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="dd880-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd880-133">-Confirm</span></span>
<span data-ttu-id="dd880-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dd880-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd880-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd880-135">-WhatIf</span></span>
<span data-ttu-id="dd880-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd880-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd880-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dd880-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd880-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd880-138">CommonParameters</span></span>
<span data-ttu-id="dd880-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd880-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd880-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd880-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd880-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd880-141">INPUTS</span></span>

### <span data-ttu-id="dd880-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd880-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="dd880-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dd880-143">System.Int32</span></span>

### <span data-ttu-id="dd880-144">System.String</span><span class="sxs-lookup"><span data-stu-id="dd880-144">System.String</span></span>

## <span data-ttu-id="dd880-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd880-145">OUTPUTS</span></span>

### <span data-ttu-id="dd880-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="dd880-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dd880-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd880-147">NOTES</span></span>

## <span data-ttu-id="dd880-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd880-148">RELATED LINKS</span></span>
