---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564683"
---
# <span data-ttu-id="be60e-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="be60e-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="be60e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be60e-102">SYNOPSIS</span></span>
<span data-ttu-id="be60e-103">Выполнить команду на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="be60e-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be60e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be60e-104">SYNTAX</span></span>

### <span data-ttu-id="be60e-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be60e-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be60e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="be60e-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be60e-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="be60e-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be60e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be60e-108">DESCRIPTION</span></span>
<span data-ttu-id="be60e-109">Вызовите команду выполнить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="be60e-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="be60e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be60e-110">EXAMPLES</span></span>

### <span data-ttu-id="be60e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be60e-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="be60e-112">Вызов команды Run для RunPowerShellScript с переопределением сценария "sample.ps1" и параметров в виртуальной машине "vmname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="be60e-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="be60e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be60e-113">PARAMETERS</span></span>

### <span data-ttu-id="be60e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be60e-114">-AsJob</span></span>
<span data-ttu-id="be60e-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="be60e-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="be60e-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="be60e-116">-CommandId</span></span>
<span data-ttu-id="be60e-117">Идентификатор команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="be60e-117">The run command id.</span></span>

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

### <span data-ttu-id="be60e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be60e-118">-DefaultProfile</span></span>
<span data-ttu-id="be60e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be60e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be60e-120">-Параметр</span><span class="sxs-lookup"><span data-stu-id="be60e-120">-Parameter</span></span>
<span data-ttu-id="be60e-121">Параметры команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="be60e-121">The run command parameters.</span></span>

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

### <span data-ttu-id="be60e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be60e-122">-ResourceGroupName</span></span>
<span data-ttu-id="be60e-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be60e-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be60e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be60e-124">-ResourceId</span></span>
<span data-ttu-id="be60e-125">Идентификатор ресурса для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="be60e-125">The resource id for the VM</span></span>

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

### <span data-ttu-id="be60e-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="be60e-126">-ScriptPath</span></span>
<span data-ttu-id="be60e-127">Путь выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="be60e-127">Path of the script to be executed.</span></span>  <span data-ttu-id="be60e-128">При задании этого значения заданный сценарий переопределяет сценарий по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="be60e-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="be60e-129">-VM</span><span class="sxs-lookup"><span data-stu-id="be60e-129">-VM</span></span>
<span data-ttu-id="be60e-130">Объект виртуальной машины PS.</span><span class="sxs-lookup"><span data-stu-id="be60e-130">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="be60e-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="be60e-131">-VMName</span></span>
<span data-ttu-id="be60e-132">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="be60e-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be60e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be60e-133">-Confirm</span></span>
<span data-ttu-id="be60e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be60e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be60e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be60e-135">-WhatIf</span></span>
<span data-ttu-id="be60e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be60e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be60e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be60e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be60e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be60e-138">CommonParameters</span></span>
<span data-ttu-id="be60e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be60e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be60e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be60e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be60e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be60e-141">INPUTS</span></span>

### <span data-ttu-id="be60e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="be60e-142">System.String</span></span>

### <span data-ttu-id="be60e-143">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="be60e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="be60e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be60e-144">OUTPUTS</span></span>

### <span data-ttu-id="be60e-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="be60e-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="be60e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="be60e-146">NOTES</span></span>

## <span data-ttu-id="be60e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be60e-147">RELATED LINKS</span></span>
