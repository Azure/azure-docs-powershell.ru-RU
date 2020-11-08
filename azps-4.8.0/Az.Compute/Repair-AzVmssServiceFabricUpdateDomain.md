---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235640"
---
# <span data-ttu-id="8a769-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8a769-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="8a769-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a769-102">SYNOPSIS</span></span>
<span data-ttu-id="8a769-103">Руководство по домену обновление платформы вручную для обновления виртуальных машин в наборе масштабирования виртуальных машин фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="8a769-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="8a769-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a769-104">SYNTAX</span></span>

### <span data-ttu-id="8a769-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a769-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a769-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8a769-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a769-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8a769-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a769-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a769-108">DESCRIPTION</span></span>
<span data-ttu-id="8a769-109">Принудительное обновление платформы вручную. Пошаговое руководство по обновлению виртуальных машин в наборе масштабов виртуальных машин фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="8a769-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="8a769-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a769-110">EXAMPLES</span></span>

### <span data-ttu-id="8a769-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a769-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="8a769-112">Эта команда обеспечивает принудительное обновление структуры Service Fabric для UD 0 для наборов масштабов виртуальных машин, заданных именем группы ресурсов и именем для задания масштаба.</span><span class="sxs-lookup"><span data-stu-id="8a769-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="8a769-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8a769-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="8a769-114">Эта команда задает для UD 1 анализ служб Service Fabric для настройки масштабирования виртуальных машин, заданной объектом Set масштабирования ВМ.</span><span class="sxs-lookup"><span data-stu-id="8a769-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="8a769-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8a769-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="8a769-116">Эта команда принудительно задает обновление структуры Service Fabric для UD 2 для наборов масштабирования виртуальных машин, заданных идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="8a769-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="8a769-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a769-117">PARAMETERS</span></span>

### <span data-ttu-id="8a769-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a769-118">-AsJob</span></span>
<span data-ttu-id="8a769-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8a769-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a769-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a769-120">-DefaultProfile</span></span>
<span data-ttu-id="8a769-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a769-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a769-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8a769-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="8a769-123">Домен обновления платформы, для которого запрашивается ручной анализ восстановления.</span><span class="sxs-lookup"><span data-stu-id="8a769-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a769-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a769-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a769-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a769-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a769-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a769-126">-ResourceId</span></span>
<span data-ttu-id="8a769-127">Идентификатор ресурса для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8a769-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a769-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a769-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a769-129">Объект установки масштаба локальной виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8a769-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a769-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8a769-130">-VMScaleSetName</span></span>
<span data-ttu-id="8a769-131">Имя набора шкал виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8a769-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a769-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a769-132">-Confirm</span></span>
<span data-ttu-id="8a769-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a769-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a769-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a769-134">-WhatIf</span></span>
<span data-ttu-id="8a769-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a769-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a769-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a769-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a769-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a769-137">CommonParameters</span></span>
<span data-ttu-id="8a769-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a769-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a769-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a769-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a769-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a769-140">INPUTS</span></span>

### <span data-ttu-id="8a769-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8a769-141">System.String</span></span>

### <span data-ttu-id="8a769-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a769-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a769-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a769-143">OUTPUTS</span></span>

### <span data-ttu-id="8a769-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="8a769-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="8a769-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a769-145">NOTES</span></span>

## <span data-ttu-id="8a769-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a769-146">RELATED LINKS</span></span>
