---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509070"
---
# <span data-ttu-id="15281-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="15281-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="15281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15281-102">SYNOPSIS</span></span>
<span data-ttu-id="15281-103">Обновление вручную по доменам платформы для обновления виртуальных машин в наборе виртуальной машинной структуры службы.</span><span class="sxs-lookup"><span data-stu-id="15281-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="15281-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="15281-104">SYNTAX</span></span>

### <span data-ttu-id="15281-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15281-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15281-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="15281-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15281-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="15281-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15281-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15281-108">DESCRIPTION</span></span>
<span data-ttu-id="15281-109">Принудительное обновление платформы вручную по окту домена для обновления виртуальных машин в наборе виртуальной машинной структуры обслуживания.</span><span class="sxs-lookup"><span data-stu-id="15281-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="15281-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="15281-110">EXAMPLES</span></span>

### <span data-ttu-id="15281-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15281-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="15281-112">Эта команда заставляет обновление материала службы ходить в обл. 0 для набора масштаба виртуальной машины, заданного с помощью имени группы ресурсов и имени набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="15281-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="15281-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15281-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="15281-114">Эта команда обновит материал службы и обновит версию на 1 для набора виртуальных машин, заданного объектом набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="15281-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="15281-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="15281-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="15281-116">Эта команда заставляет обновление материала службы ходить в обл. 2 для набора масштаба виртуальной машины, заданного с помощью ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="15281-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="15281-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15281-117">PARAMETERS</span></span>

### <span data-ttu-id="15281-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15281-118">-AsJob</span></span>
<span data-ttu-id="15281-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="15281-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15281-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15281-120">-DefaultProfile</span></span>
<span data-ttu-id="15281-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15281-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15281-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="15281-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="15281-123">Домен обновления платформы, для которого запрашивается восстановление вручную.</span><span class="sxs-lookup"><span data-stu-id="15281-123">The platform update domain for which a manual recovery walk is requested.</span></span>

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

### <span data-ttu-id="15281-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15281-124">-ResourceGroupName</span></span>
<span data-ttu-id="15281-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15281-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="15281-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15281-126">-ResourceId</span></span>
<span data-ttu-id="15281-127">ИД ресурса для набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15281-127">The resource id for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="15281-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15281-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="15281-129">Объект набора локальной виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="15281-129">Local virtual machine scale set object</span></span>

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

### <span data-ttu-id="15281-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="15281-130">-VMScaleSetName</span></span>
<span data-ttu-id="15281-131">Имя набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="15281-131">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="15281-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15281-132">-Confirm</span></span>
<span data-ttu-id="15281-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="15281-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15281-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15281-134">-WhatIf</span></span>
<span data-ttu-id="15281-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15281-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15281-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="15281-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15281-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15281-137">CommonParameters</span></span>
<span data-ttu-id="15281-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15281-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15281-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15281-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15281-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15281-140">INPUTS</span></span>

### <span data-ttu-id="15281-141">System.String</span><span class="sxs-lookup"><span data-stu-id="15281-141">System.String</span></span>

### <span data-ttu-id="15281-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="15281-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="15281-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="15281-143">OUTPUTS</span></span>

### <span data-ttu-id="15281-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryResponse</span><span class="sxs-lookup"><span data-stu-id="15281-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="15281-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="15281-145">NOTES</span></span>

## <span data-ttu-id="15281-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15281-146">RELATED LINKS</span></span>