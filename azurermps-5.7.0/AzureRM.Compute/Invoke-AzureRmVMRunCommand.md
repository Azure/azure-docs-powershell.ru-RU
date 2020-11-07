---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 7d3c27ad8dacb288aeb0d15235aacc48405b8a6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734472"
---
# <span data-ttu-id="0e6e5-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="0e6e5-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="0e6e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6e5-103">Выполнить команду на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e6e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e6e5-104">SYNTAX</span></span>

### <span data-ttu-id="0e6e5-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e6e5-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e6e5-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="0e6e5-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e6e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e6e5-107">DESCRIPTION</span></span>
<span data-ttu-id="0e6e5-108">Вызовите команду выполнить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="0e6e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e6e5-109">EXAMPLES</span></span>

### <span data-ttu-id="0e6e5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e6e5-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="0e6e5-111">Вызов команды Run для RunPowerShellScript с переопределением сценария "sample.ps1" и параметров в виртуальной машине "vmname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="0e6e5-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="0e6e5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e6e5-112">PARAMETERS</span></span>

### <span data-ttu-id="0e6e5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e6e5-113">-AsJob</span></span>
<span data-ttu-id="0e6e5-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="0e6e5-115">-CommandId</span></span>
<span data-ttu-id="0e6e5-116">Идентификатор команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="0e6e5-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6e5-117">-DefaultProfile</span></span>
<span data-ttu-id="0e6e5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-119">-Параметр</span><span class="sxs-lookup"><span data-stu-id="0e6e5-119">-Parameter</span></span>
<span data-ttu-id="0e6e5-120">Параметры команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="0e6e5-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e6e5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="0e6e5-123">-ScriptPath</span></span>
<span data-ttu-id="0e6e5-124">Путь выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-124">Path of the script to be executed.</span></span>  <span data-ttu-id="0e6e5-125">При задании этого значения заданный сценарий переопределяет сценарий по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-126">-VM</span><span class="sxs-lookup"><span data-stu-id="0e6e5-126">-VM</span></span>
<span data-ttu-id="0e6e5-127">Объект виртуальной машины PS.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e6e5-128">-VMName</span></span>
<span data-ttu-id="0e6e5-129">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e6e5-130">-Confirm</span></span>
<span data-ttu-id="0e6e5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e6e5-132">-WhatIf</span></span>
<span data-ttu-id="0e6e5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e6e5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e6e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6e5-135">CommonParameters</span></span>
<span data-ttu-id="0e6e5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e6e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6e5-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e6e5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6e5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e6e5-138">INPUTS</span></span>

### <span data-ttu-id="0e6e5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0e6e5-139">System.String</span></span>
<span data-ttu-id="0e6e5-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0e6e5-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0e6e5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e6e5-141">OUTPUTS</span></span>

### <span data-ttu-id="0e6e5-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="0e6e5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="0e6e5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e6e5-143">NOTES</span></span>

## <span data-ttu-id="0e6e5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e6e5-144">RELATED LINKS</span></span>
