---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246793"
---
# <span data-ttu-id="2a067-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2a067-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="2a067-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a067-102">SYNOPSIS</span></span>
<span data-ttu-id="2a067-103">Команда "выполнить" на виртуальной машине с установленным параметром "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="2a067-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2a067-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a067-104">SYNTAX</span></span>

### <span data-ttu-id="2a067-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a067-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a067-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="2a067-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a067-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="2a067-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a067-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a067-108">DESCRIPTION</span></span>
<span data-ttu-id="2a067-109">Вызовите команду выполнить на виртуальной машине с набором виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2a067-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="2a067-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a067-110">EXAMPLES</span></span>

### <span data-ttu-id="2a067-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a067-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2a067-112">Вызовите команду Run из RunPowerShellScript, переопределив сценарий "sample.ps1" и параметры на ВИРТУАЛЬНОЙ машине идентификатора "0" в наборе масштаба виртуальной машины "vmssname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="2a067-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="2a067-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2a067-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="2a067-114">Вызовите команду Run из RunPowerShellScript, переопределив сценарий "sample.ps1" и параметры на ВИРТУАЛЬНОЙ машине идентификатора "0" в наборе масштаба виртуальной машины "vmssname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="2a067-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="2a067-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a067-115">PARAMETERS</span></span>

### <span data-ttu-id="2a067-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a067-116">-AsJob</span></span>
<span data-ttu-id="2a067-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a067-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a067-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="2a067-118">-CommandId</span></span>
<span data-ttu-id="2a067-119">Идентификатор команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="2a067-119">The run command id.</span></span>

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

### <span data-ttu-id="2a067-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a067-120">-DefaultProfile</span></span>
<span data-ttu-id="2a067-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a067-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a067-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2a067-122">-InstanceId</span></span>
<span data-ttu-id="2a067-123">Идентификатор экземпляра для набора виртуальных машин масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2a067-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="2a067-124">-Параметр</span><span class="sxs-lookup"><span data-stu-id="2a067-124">-Parameter</span></span>
<span data-ttu-id="2a067-125">Параметры команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="2a067-125">The run command parameters.</span></span>

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

### <span data-ttu-id="2a067-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a067-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a067-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a067-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2a067-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a067-128">-ResourceId</span></span>
<span data-ttu-id="2a067-129">Идентификатор ресурса для виртуальной машины с установленным параметром "виртуальная машина"</span><span class="sxs-lookup"><span data-stu-id="2a067-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="2a067-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="2a067-130">-ScriptPath</span></span>
<span data-ttu-id="2a067-131">Путь выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="2a067-131">Path of the script to be executed.</span></span>  <span data-ttu-id="2a067-132">При задании этого значения заданный сценарий переопределяет сценарий по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="2a067-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="2a067-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2a067-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="2a067-134">Объект ВИРТУАЛЬНОЙ машины с установленным параметром "виртуальная машина" в PS.</span><span class="sxs-lookup"><span data-stu-id="2a067-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="2a067-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2a067-135">-VMScaleSetName</span></span>
<span data-ttu-id="2a067-136">Имя виртуальной машины в наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2a067-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="2a067-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a067-137">-Confirm</span></span>
<span data-ttu-id="2a067-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a067-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a067-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a067-139">-WhatIf</span></span>
<span data-ttu-id="2a067-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a067-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a067-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a067-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a067-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a067-142">CommonParameters</span></span>
<span data-ttu-id="2a067-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a067-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a067-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a067-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a067-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a067-145">INPUTS</span></span>

### <span data-ttu-id="2a067-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2a067-146">System.String</span></span>

### <span data-ttu-id="2a067-147">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="2a067-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="2a067-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a067-148">OUTPUTS</span></span>

### <span data-ttu-id="2a067-149">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="2a067-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="2a067-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a067-150">NOTES</span></span>

## <span data-ttu-id="2a067-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a067-151">RELATED LINKS</span></span>