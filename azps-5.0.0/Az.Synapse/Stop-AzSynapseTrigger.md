---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246599"
---
# <span data-ttu-id="13e66-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="13e66-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="13e66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13e66-102">SYNOPSIS</span></span>
<span data-ttu-id="13e66-103">Остановка триггера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="13e66-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="13e66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13e66-104">SYNTAX</span></span>

### <span data-ttu-id="13e66-105">StopByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13e66-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13e66-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="13e66-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13e66-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="13e66-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13e66-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13e66-108">DESCRIPTION</span></span>
<span data-ttu-id="13e66-109">Командлет **Stop-AzSynapseTrigger** останавливает выполнение триггера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="13e66-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="13e66-110">Если триггер находится в состоянии "начато", этот командлет останавливает срабатывание триггера и больше не вызывает конвейеры.</span><span class="sxs-lookup"><span data-stu-id="13e66-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="13e66-111">Если триггер уже находится в состоянии "остановлено", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="13e66-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="13e66-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13e66-112">EXAMPLES</span></span>

### <span data-ttu-id="13e66-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13e66-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="13e66-114">Остановка триггера под названием ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="13e66-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="13e66-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="13e66-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="13e66-116">Остановка триггера под названием ContosoTrigger в рабочей области ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="13e66-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="13e66-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="13e66-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="13e66-118">Остановка триггера под названием ContosoTrigger в рабочей области ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="13e66-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="13e66-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13e66-119">PARAMETERS</span></span>

### <span data-ttu-id="13e66-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13e66-120">-AsJob</span></span>
<span data-ttu-id="13e66-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="13e66-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13e66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e66-122">-DefaultProfile</span></span>
<span data-ttu-id="13e66-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13e66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e66-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13e66-124">-InputObject</span></span>
<span data-ttu-id="13e66-125">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="13e66-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13e66-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13e66-126">-Name</span></span>
<span data-ttu-id="13e66-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="13e66-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e66-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13e66-128">-PassThru</span></span>
<span data-ttu-id="13e66-129">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="13e66-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="13e66-130">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="13e66-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="13e66-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13e66-131">-WorkspaceName</span></span>
<span data-ttu-id="13e66-132">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="13e66-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e66-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="13e66-133">-WorkspaceObject</span></span>
<span data-ttu-id="13e66-134">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="13e66-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13e66-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13e66-135">-Confirm</span></span>
<span data-ttu-id="13e66-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13e66-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e66-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e66-137">-WhatIf</span></span>
<span data-ttu-id="13e66-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13e66-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13e66-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13e66-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e66-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e66-140">CommonParameters</span></span>
<span data-ttu-id="13e66-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13e66-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e66-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13e66-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e66-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13e66-143">INPUTS</span></span>

### <span data-ttu-id="13e66-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="13e66-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="13e66-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="13e66-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="13e66-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13e66-146">OUTPUTS</span></span>

### <span data-ttu-id="13e66-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13e66-147">System.Boolean</span></span>

## <span data-ttu-id="13e66-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="13e66-148">NOTES</span></span>

## <span data-ttu-id="13e66-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13e66-149">RELATED LINKS</span></span>
