---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409980"
---
# <span data-ttu-id="e4731-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="e4731-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="e4731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4731-102">SYNOPSIS</span></span>
<span data-ttu-id="e4731-103">Задает состояние службы единения для VMSS.</span><span class="sxs-lookup"><span data-stu-id="e4731-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="e4731-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4731-104">SYNTAX</span></span>

### <span data-ttu-id="e4731-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4731-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4731-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e4731-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4731-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e4731-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4731-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4731-108">DESCRIPTION</span></span>
<span data-ttu-id="e4731-109">Задает состояние службы единения для VMSS.</span><span class="sxs-lookup"><span data-stu-id="e4731-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="e4731-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4731-110">EXAMPLES</span></span>

### <span data-ttu-id="e4731-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4731-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="e4731-112">Эта команда приостанавливать службу автоматического восстановления на VMSS "vmss1" в группе ресурсов "rg".</span><span class="sxs-lookup"><span data-stu-id="e4731-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="e4731-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e4731-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="e4731-114">Эта команда возобновляет работу службы автоматического восстановления на VMSS "vmss1" в группе ресурсов "rg".</span><span class="sxs-lookup"><span data-stu-id="e4731-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="e4731-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4731-115">PARAMETERS</span></span>

### <span data-ttu-id="e4731-116">-Action</span><span class="sxs-lookup"><span data-stu-id="e4731-116">-Action</span></span>
<span data-ttu-id="e4731-117">Выполняемые действия.</span><span class="sxs-lookup"><span data-stu-id="e4731-117">The action to be performed.</span></span>  <span data-ttu-id="e4731-118">Возможные значения: Resume (Возобновить), Suspend (Приостановить).</span><span class="sxs-lookup"><span data-stu-id="e4731-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4731-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4731-119">-AsJob</span></span>
<span data-ttu-id="e4731-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e4731-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4731-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4731-121">-DefaultProfile</span></span>
<span data-ttu-id="e4731-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4731-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4731-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4731-123">-InputObject</span></span>
<span data-ttu-id="e4731-124">Локальный объект набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4731-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e4731-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4731-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4731-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4731-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e4731-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4731-127">-ResourceId</span></span>
<span data-ttu-id="e4731-128">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="e4731-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="e4731-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4731-129">-ServiceName</span></span>
<span data-ttu-id="e4731-130">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="e4731-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4731-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e4731-131">-VMScaleSetName</span></span>
<span data-ttu-id="e4731-132">Имя набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4731-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e4731-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4731-133">-Confirm</span></span>
<span data-ttu-id="e4731-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4731-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4731-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4731-135">-WhatIf</span></span>
<span data-ttu-id="e4731-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4731-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4731-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e4731-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4731-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4731-138">CommonParameters</span></span>
<span data-ttu-id="e4731-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4731-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4731-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4731-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4731-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4731-141">INPUTS</span></span>

### <span data-ttu-id="e4731-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e4731-142">System.String</span></span>

### <span data-ttu-id="e4731-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="e4731-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e4731-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4731-144">OUTPUTS</span></span>

### <span data-ttu-id="e4731-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e4731-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e4731-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4731-146">NOTES</span></span>

## <span data-ttu-id="e4731-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4731-147">RELATED LINKS</span></span>
