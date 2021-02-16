---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229097"
---
# <span data-ttu-id="60a92-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="60a92-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="60a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60a92-102">SYNOPSIS</span></span>
<span data-ttu-id="60a92-103">Запустите команду на VM.</span><span class="sxs-lookup"><span data-stu-id="60a92-103">Run a command on the VM.</span></span>

## <span data-ttu-id="60a92-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60a92-104">SYNTAX</span></span>

### <span data-ttu-id="60a92-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60a92-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a92-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="60a92-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a92-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="60a92-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60a92-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60a92-108">DESCRIPTION</span></span>
<span data-ttu-id="60a92-109">Вызвать команду запуска на VM.</span><span class="sxs-lookup"><span data-stu-id="60a92-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="60a92-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60a92-110">EXAMPLES</span></span>

### <span data-ttu-id="60a92-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60a92-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="60a92-112">Вызов команды запуска RunPowerShellScript с переопределение сценария "sample.ps1" и параметров в VM "vmname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="60a92-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="60a92-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60a92-113">PARAMETERS</span></span>

### <span data-ttu-id="60a92-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60a92-114">-AsJob</span></span>
<span data-ttu-id="60a92-115">Запустите его в фоновом режиме и верните объект задания для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="60a92-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="60a92-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="60a92-116">-CommandId</span></span>
<span data-ttu-id="60a92-117">ИД команды "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="60a92-117">The run command ID.</span></span>

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

### <span data-ttu-id="60a92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a92-118">-DefaultProfile</span></span>
<span data-ttu-id="60a92-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60a92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a92-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="60a92-120">-Parameter</span></span>
<span data-ttu-id="60a92-121">Параметры команды запуска.</span><span class="sxs-lookup"><span data-stu-id="60a92-121">The run command parameters.</span></span>

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

### <span data-ttu-id="60a92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a92-122">-ResourceGroupName</span></span>
<span data-ttu-id="60a92-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60a92-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="60a92-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60a92-124">-ResourceId</span></span>
<span data-ttu-id="60a92-125">ИД ресурса для VM.</span><span class="sxs-lookup"><span data-stu-id="60a92-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="60a92-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="60a92-126">-ScriptPath</span></span>
<span data-ttu-id="60a92-127">Путь к сценарию, который нужно выполнять.</span><span class="sxs-lookup"><span data-stu-id="60a92-127">Path of the script to be executed.</span></span>  <span data-ttu-id="60a92-128">Если задано это значение, сценарий, заданный по умолчанию для команды, переопределит его.</span><span class="sxs-lookup"><span data-stu-id="60a92-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="60a92-129">-VM</span><span class="sxs-lookup"><span data-stu-id="60a92-129">-VM</span></span>
<span data-ttu-id="60a92-130">Объект виртуальной машины PS.</span><span class="sxs-lookup"><span data-stu-id="60a92-130">The PS virtual machine object.</span></span>

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

### <span data-ttu-id="60a92-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="60a92-131">-VMName</span></span>
<span data-ttu-id="60a92-132">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="60a92-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="60a92-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60a92-133">-Confirm</span></span>
<span data-ttu-id="60a92-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="60a92-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a92-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a92-135">-WhatIf</span></span>
<span data-ttu-id="60a92-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a92-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a92-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="60a92-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a92-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a92-138">CommonParameters</span></span>
<span data-ttu-id="60a92-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a92-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a92-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60a92-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a92-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60a92-141">INPUTS</span></span>

### <span data-ttu-id="60a92-142">System.String</span><span class="sxs-lookup"><span data-stu-id="60a92-142">System.String</span></span>

### <span data-ttu-id="60a92-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="60a92-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="60a92-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60a92-144">OUTPUTS</span></span>

### <span data-ttu-id="60a92-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="60a92-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="60a92-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60a92-146">NOTES</span></span>

## <span data-ttu-id="60a92-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60a92-147">RELATED LINKS</span></span>
