---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 2402591c6c388dbe7c1c6b24a1beb2b298012d4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570096"
---
# <span data-ttu-id="a6e77-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="a6e77-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="a6e77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6e77-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e77-103">Выполнить команду на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a6e77-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6e77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6e77-104">SYNTAX</span></span>

### <span data-ttu-id="a6e77-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6e77-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6e77-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="a6e77-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e77-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6e77-107">DESCRIPTION</span></span>
<span data-ttu-id="a6e77-108">Вызовите команду выполнить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a6e77-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="a6e77-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6e77-109">EXAMPLES</span></span>

### <span data-ttu-id="a6e77-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6e77-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="a6e77-111">Вызов команды Run для RunPowerShellScript с переопределением сценария "sample.ps1" и параметров в виртуальной машине "vmname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="a6e77-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="a6e77-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6e77-112">PARAMETERS</span></span>

### <span data-ttu-id="a6e77-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="a6e77-113">-CommandId</span></span>
<span data-ttu-id="a6e77-114">Идентификатор команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="a6e77-114">The run command id.</span></span>

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

### <span data-ttu-id="a6e77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e77-115">-DefaultProfile</span></span>
<span data-ttu-id="a6e77-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6e77-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6e77-117">-Параметр</span><span class="sxs-lookup"><span data-stu-id="a6e77-117">-Parameter</span></span>
<span data-ttu-id="a6e77-118">Параметры команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="a6e77-118">The run command parameters.</span></span>

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

### <span data-ttu-id="a6e77-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e77-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6e77-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6e77-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6e77-121">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="a6e77-121">-ScriptPath</span></span>
<span data-ttu-id="a6e77-122">Путь выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="a6e77-122">Path of the script to be executed.</span></span>  <span data-ttu-id="a6e77-123">При задании этого значения заданный сценарий переопределяет сценарий по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="a6e77-123">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="a6e77-124">-VM</span><span class="sxs-lookup"><span data-stu-id="a6e77-124">-VM</span></span>
<span data-ttu-id="a6e77-125">Объект виртуальной машины PS.</span><span class="sxs-lookup"><span data-stu-id="a6e77-125">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="a6e77-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="a6e77-126">-VMName</span></span>
<span data-ttu-id="a6e77-127">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a6e77-127">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="a6e77-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6e77-128">-Confirm</span></span>
<span data-ttu-id="a6e77-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6e77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e77-130">-WhatIf</span></span>
<span data-ttu-id="a6e77-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6e77-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6e77-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6e77-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e77-133">CommonParameters</span></span>
<span data-ttu-id="a6e77-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6e77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e77-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6e77-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e77-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6e77-136">INPUTS</span></span>

### <span data-ttu-id="a6e77-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a6e77-137">System.String</span></span>
<span data-ttu-id="a6e77-138">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6e77-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a6e77-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6e77-139">OUTPUTS</span></span>

### <span data-ttu-id="a6e77-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="a6e77-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="a6e77-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6e77-141">NOTES</span></span>

## <span data-ttu-id="a6e77-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6e77-142">RELATED LINKS</span></span>

