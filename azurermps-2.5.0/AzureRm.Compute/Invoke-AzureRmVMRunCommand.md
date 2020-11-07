---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
ms.openlocfilehash: 12b9b3870b5239746a8524bad9aad0f44161acd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914225"
---
# <span data-ttu-id="dc40d-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="dc40d-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="dc40d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc40d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc40d-103">Выполнить команду на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="dc40d-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc40d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc40d-104">SYNTAX</span></span>

### <span data-ttu-id="dc40d-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc40d-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc40d-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="dc40d-106">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc40d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc40d-107">DESCRIPTION</span></span>
<span data-ttu-id="dc40d-108">Вызовите команду выполнить на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="dc40d-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="dc40d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc40d-109">EXAMPLES</span></span>

### <span data-ttu-id="dc40d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc40d-110">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="dc40d-111">Вызов команды Run для RunPowerShellScript с переопределением сценария "sample.ps1" и параметров в виртуальной машине "vmname" в группе ресурсов "rgname".</span><span class="sxs-lookup"><span data-stu-id="dc40d-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="dc40d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc40d-112">PARAMETERS</span></span>

### <span data-ttu-id="dc40d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc40d-113">-AsJob</span></span>
<span data-ttu-id="dc40d-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc40d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dc40d-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="dc40d-115">-CommandId</span></span>
<span data-ttu-id="dc40d-116">Идентификатор команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="dc40d-116">The run command id.</span></span>

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

### <span data-ttu-id="dc40d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc40d-117">-DefaultProfile</span></span>
<span data-ttu-id="dc40d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc40d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc40d-119">-Параметр</span><span class="sxs-lookup"><span data-stu-id="dc40d-119">-Parameter</span></span>
<span data-ttu-id="dc40d-120">Параметры команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="dc40d-120">The run command parameters.</span></span>

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

### <span data-ttu-id="dc40d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc40d-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc40d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc40d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc40d-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="dc40d-123">-ScriptPath</span></span>
<span data-ttu-id="dc40d-124">Путь выполняемого сценария.</span><span class="sxs-lookup"><span data-stu-id="dc40d-124">Path of the script to be executed.</span></span>  <span data-ttu-id="dc40d-125">При задании этого значения заданный сценарий переопределяет сценарий по умолчанию для команды.</span><span class="sxs-lookup"><span data-stu-id="dc40d-125">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="dc40d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="dc40d-126">-VM</span></span>
<span data-ttu-id="dc40d-127">Объект виртуальной машины PS.</span><span class="sxs-lookup"><span data-stu-id="dc40d-127">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="dc40d-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="dc40d-128">-VMName</span></span>
<span data-ttu-id="dc40d-129">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dc40d-129">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="dc40d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc40d-130">-Confirm</span></span>
<span data-ttu-id="dc40d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc40d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc40d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc40d-132">-WhatIf</span></span>
<span data-ttu-id="dc40d-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc40d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc40d-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc40d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc40d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc40d-135">CommonParameters</span></span>
<span data-ttu-id="dc40d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc40d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc40d-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc40d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc40d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc40d-138">INPUTS</span></span>

### <span data-ttu-id="dc40d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc40d-139">System.String</span></span>
<span data-ttu-id="dc40d-140">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dc40d-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dc40d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc40d-141">OUTPUTS</span></span>

### <span data-ttu-id="dc40d-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="dc40d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="dc40d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc40d-143">NOTES</span></span>

## <span data-ttu-id="dc40d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc40d-144">RELATED LINKS</span></span>

