---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235648"
---
# <span data-ttu-id="28068-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="28068-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="28068-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28068-102">SYNOPSIS</span></span>
<span data-ttu-id="28068-103">Выполнение команды на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="28068-103">Run a command on the VM.</span></span>

## <span data-ttu-id="28068-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28068-104">SYNTAX</span></span>

### <span data-ttu-id="28068-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28068-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28068-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="28068-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28068-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="28068-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28068-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28068-108">DESCRIPTION</span></span>
<span data-ttu-id="28068-109">Вызовите команду выполнить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="28068-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="28068-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28068-110">EXAMPLES</span></span>

### <span data-ttu-id="28068-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28068-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="28068-112">Вызов команды Run для RunPowerShellScript с переопределением сценария "sample.ps1" и параметров в виртуальной машине "vmname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="28068-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="28068-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28068-113">PARAMETERS</span></span>

### <span data-ttu-id="28068-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28068-114">-AsJob</span></span>
<span data-ttu-id="28068-115">Запустите командлет в фоновом режиме и верните объект задания, чтобы отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="28068-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="28068-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="28068-116">-CommandId</span></span>
<span data-ttu-id="28068-117">Идентификатор команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="28068-117">The run command ID.</span></span>

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

### <span data-ttu-id="28068-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28068-118">-DefaultProfile</span></span>
<span data-ttu-id="28068-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28068-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28068-120">-Параметр</span><span class="sxs-lookup"><span data-stu-id="28068-120">-Parameter</span></span>
<span data-ttu-id="28068-121">Параметры команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="28068-121">The run command parameters.</span></span>

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

### <span data-ttu-id="28068-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28068-122">-ResourceGroupName</span></span>
<span data-ttu-id="28068-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28068-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="28068-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28068-124">-ResourceId</span></span>
<span data-ttu-id="28068-125">Идентификатор ресурса для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28068-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="28068-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="28068-126">-ScriptPath</span></span>
<span data-ttu-id="28068-127">Путь выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="28068-127">Path of the script to be executed.</span></span>  <span data-ttu-id="28068-128">При задании этого значения заданный сценарий переопределяет сценарий по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="28068-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="28068-129">-VM</span><span class="sxs-lookup"><span data-stu-id="28068-129">-VM</span></span>
<span data-ttu-id="28068-130">Объект виртуальной машины PS.</span><span class="sxs-lookup"><span data-stu-id="28068-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28068-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="28068-131">-VMName</span></span>
<span data-ttu-id="28068-132">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="28068-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="28068-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28068-133">-Confirm</span></span>
<span data-ttu-id="28068-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28068-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28068-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28068-135">-WhatIf</span></span>
<span data-ttu-id="28068-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28068-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28068-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28068-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28068-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28068-138">CommonParameters</span></span>
<span data-ttu-id="28068-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28068-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28068-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28068-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28068-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28068-141">INPUTS</span></span>

### <span data-ttu-id="28068-142">System. String</span><span class="sxs-lookup"><span data-stu-id="28068-142">System.String</span></span>

### <span data-ttu-id="28068-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="28068-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="28068-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28068-144">OUTPUTS</span></span>

### <span data-ttu-id="28068-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="28068-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="28068-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="28068-146">NOTES</span></span>

## <span data-ttu-id="28068-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28068-147">RELATED LINKS</span></span>
