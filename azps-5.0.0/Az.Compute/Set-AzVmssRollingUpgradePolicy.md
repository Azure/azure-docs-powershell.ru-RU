---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311969"
---
# <span data-ttu-id="78268-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="78268-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="78268-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78268-102">SYNOPSIS</span></span>
<span data-ttu-id="78268-103">Задает свойства политики чередующегося обновления VMSS.</span><span class="sxs-lookup"><span data-stu-id="78268-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="78268-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78268-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78268-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78268-105">DESCRIPTION</span></span>
<span data-ttu-id="78268-106">Задает свойства политики чередующегося обновления VMSS.</span><span class="sxs-lookup"><span data-stu-id="78268-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="78268-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78268-107">EXAMPLES</span></span>

### <span data-ttu-id="78268-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78268-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="78268-109">Эта команда задает 40 процента для MaxBatchInstance, 35 процента для MaxUnhealthyInstance, 30 процентов для MaxUnhealthyUpgradedInstance и 30% времени паузы между пакетами для VMSS локального объекта $vmss.</span><span class="sxs-lookup"><span data-stu-id="78268-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="78268-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78268-110">PARAMETERS</span></span>

### <span data-ttu-id="78268-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78268-111">-DefaultProfile</span></span>
<span data-ttu-id="78268-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78268-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78268-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="78268-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="78268-114">Максимальное количество экземпляров виртуальных машин, которые будут одновременно обновлены с помощью чередующегося обновления в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="78268-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="78268-115">Так как это максимальное количество неработоспособных экземпляров в предыдущих или будущих пакетах, может снизиться доля экземпляров в пакете для обеспечения более высокой надежности.</span><span class="sxs-lookup"><span data-stu-id="78268-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="78268-116">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="78268-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="78268-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="78268-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="78268-118">Максимальный процент общего количества экземпляров виртуальных машин в наборе масштабов, которые могут быть одновременными, либо в результате обновления, либо при обнаружении неработоспособности с помощью проверок работоспособности виртуальной машины перед прерыванием чередующегося обновления.</span><span class="sxs-lookup"><span data-stu-id="78268-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="78268-119">Это ограничение будет проверяться перед запуском какого – либо пакета.</span><span class="sxs-lookup"><span data-stu-id="78268-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="78268-120">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="78268-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="78268-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="78268-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="78268-122">Максимальный процент обновленных экземпляров виртуальных машин, которые могут быть обнаружены в неработоспособном состоянии.</span><span class="sxs-lookup"><span data-stu-id="78268-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="78268-123">Эта проверка произойдет после обновления каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="78268-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="78268-124">Если это процентное значение превышено, чередующееся обновление прерывается.</span><span class="sxs-lookup"><span data-stu-id="78268-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="78268-125">Если значение не задано, оно равно 20.</span><span class="sxs-lookup"><span data-stu-id="78268-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="78268-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="78268-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="78268-127">Время ожидания между выполнением обновления для всех виртуальных машин в одном пакете и запуском следующего пакета.</span><span class="sxs-lookup"><span data-stu-id="78268-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="78268-128">Длительность времени следует указывать в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="78268-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="78268-129">Значением по умолчанию является 0 секунд (PT0S).</span><span class="sxs-lookup"><span data-stu-id="78268-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="78268-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78268-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="78268-131">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="78268-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="78268-132">Для создания объекта можно использовать командлет New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="78268-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="78268-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78268-133">-Confirm</span></span>
<span data-ttu-id="78268-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78268-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78268-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78268-135">-WhatIf</span></span>
<span data-ttu-id="78268-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78268-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78268-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78268-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78268-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78268-138">CommonParameters</span></span>
<span data-ttu-id="78268-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78268-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78268-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78268-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78268-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78268-141">INPUTS</span></span>

### <span data-ttu-id="78268-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78268-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="78268-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="78268-143">System.Int32</span></span>

### <span data-ttu-id="78268-144">System. String</span><span class="sxs-lookup"><span data-stu-id="78268-144">System.String</span></span>

## <span data-ttu-id="78268-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78268-145">OUTPUTS</span></span>

### <span data-ttu-id="78268-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78268-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="78268-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="78268-147">NOTES</span></span>

## <span data-ttu-id="78268-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78268-148">RELATED LINKS</span></span>
