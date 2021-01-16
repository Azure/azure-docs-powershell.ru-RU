---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393967"
---
# <span data-ttu-id="a01b0-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="a01b0-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="a01b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01b0-102">SYNOPSIS</span></span>
<span data-ttu-id="a01b0-103">Команда "Выполнить" на виртуальной машине (scale Set VM).</span><span class="sxs-lookup"><span data-stu-id="a01b0-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="a01b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a01b0-104">SYNTAX</span></span>

### <span data-ttu-id="a01b0-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a01b0-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a01b0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a01b0-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a01b0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a01b0-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01b0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a01b0-108">DESCRIPTION</span></span>
<span data-ttu-id="a01b0-109">Вызов команды запуска на виртуальной машине (scale Set VM).</span><span class="sxs-lookup"><span data-stu-id="a01b0-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="a01b0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a01b0-110">EXAMPLES</span></span>

### <span data-ttu-id="a01b0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a01b0-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="a01b0-112">Вызвать команду запуска RunPowerShellScript, переопределив сценарий sample.ps1 и параметры на ID '0' VM в наборе виртуальной машинной шкалы vmssname в группе ресурсов 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="a01b0-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="a01b0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a01b0-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="a01b0-114">Вызвать команду запуска RunPowerShellScript, переопределив сценарий sample.ps1 и параметры на ID '0' VM в наборе виртуальной машинной шкалы vmssname в группе ресурсов 'rgname'.</span><span class="sxs-lookup"><span data-stu-id="a01b0-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="a01b0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a01b0-115">PARAMETERS</span></span>

### <span data-ttu-id="a01b0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a01b0-116">-AsJob</span></span>
<span data-ttu-id="a01b0-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a01b0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a01b0-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="a01b0-118">-CommandId</span></span>
<span data-ttu-id="a01b0-119">ИД команды запуска.</span><span class="sxs-lookup"><span data-stu-id="a01b0-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01b0-120">-DefaultProfile</span></span>
<span data-ttu-id="a01b0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a01b0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a01b0-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a01b0-122">-InstanceId</span></span>
<span data-ttu-id="a01b0-123">The instance ID of the virtual machine scale set VM.</span><span class="sxs-lookup"><span data-stu-id="a01b0-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01b0-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a01b0-124">-Parameter</span></span>
<span data-ttu-id="a01b0-125">Параметры команды запуска.</span><span class="sxs-lookup"><span data-stu-id="a01b0-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a01b0-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a01b0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a01b0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a01b0-128">-ResourceId</span></span>
<span data-ttu-id="a01b0-129">ИД ресурса для набора виртуальных машин (VM)</span><span class="sxs-lookup"><span data-stu-id="a01b0-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="a01b0-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="a01b0-130">-ScriptPath</span></span>
<span data-ttu-id="a01b0-131">Путь к сценарию, который нужно выполнять.</span><span class="sxs-lookup"><span data-stu-id="a01b0-131">Path of the script to be executed.</span></span>  <span data-ttu-id="a01b0-132">Если задано это значение, сценарий, заданный по умолчанию для команды, переопределит его.</span><span class="sxs-lookup"><span data-stu-id="a01b0-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01b0-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a01b0-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="a01b0-134">Объект VM в наборе виртуальных машин PS.</span><span class="sxs-lookup"><span data-stu-id="a01b0-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a01b0-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a01b0-135">-VMScaleSetName</span></span>
<span data-ttu-id="a01b0-136">Имя набора виртуальной машины (VM).</span><span class="sxs-lookup"><span data-stu-id="a01b0-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="a01b0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a01b0-137">-Confirm</span></span>
<span data-ttu-id="a01b0-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a01b0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a01b0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01b0-139">-WhatIf</span></span>
<span data-ttu-id="a01b0-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a01b0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01b0-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a01b0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a01b0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01b0-142">CommonParameters</span></span>
<span data-ttu-id="a01b0-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a01b0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01b0-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a01b0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01b0-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a01b0-145">INPUTS</span></span>

### <span data-ttu-id="a01b0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="a01b0-146">System.String</span></span>

### <span data-ttu-id="a01b0-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a01b0-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="a01b0-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a01b0-148">OUTPUTS</span></span>

### <span data-ttu-id="a01b0-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="a01b0-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="a01b0-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a01b0-150">NOTES</span></span>

## <span data-ttu-id="a01b0-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a01b0-151">RELATED LINKS</span></span>
