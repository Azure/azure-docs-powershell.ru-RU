---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231377"
---
# <span data-ttu-id="9711a-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="9711a-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="9711a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9711a-102">SYNOPSIS</span></span>
<span data-ttu-id="9711a-103">Остановка триггера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9711a-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="9711a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9711a-104">SYNTAX</span></span>

### <span data-ttu-id="9711a-105">StopByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9711a-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9711a-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="9711a-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9711a-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="9711a-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9711a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9711a-108">DESCRIPTION</span></span>
<span data-ttu-id="9711a-109">В рабочей области триггер **Stop-AzSynapseTrigger** останавливает триггер.</span><span class="sxs-lookup"><span data-stu-id="9711a-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="9711a-110">Если триггер находится в состоянии "Запущено", то триггер останавливается и перестает вызывать конвейеры.</span><span class="sxs-lookup"><span data-stu-id="9711a-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="9711a-111">Если триггер уже находится в состоянии "Остановлено", этот cmdlet не влияет.</span><span class="sxs-lookup"><span data-stu-id="9711a-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="9711a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9711a-112">EXAMPLES</span></span>

### <span data-ttu-id="9711a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9711a-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="9711a-114">Остановка триггера ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9711a-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9711a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9711a-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="9711a-116">Запуск триггера ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="9711a-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="9711a-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9711a-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="9711a-118">Остановка триггера ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="9711a-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="9711a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9711a-119">PARAMETERS</span></span>

### <span data-ttu-id="9711a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9711a-120">-AsJob</span></span>
<span data-ttu-id="9711a-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9711a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9711a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9711a-122">-DefaultProfile</span></span>
<span data-ttu-id="9711a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9711a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9711a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9711a-124">-InputObject</span></span>
<span data-ttu-id="9711a-125">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="9711a-125">The trigger object.</span></span>

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

### <span data-ttu-id="9711a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9711a-126">-Name</span></span>
<span data-ttu-id="9711a-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="9711a-127">The trigger name.</span></span>

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

### <span data-ttu-id="9711a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9711a-128">-PassThru</span></span>
<span data-ttu-id="9711a-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9711a-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9711a-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="9711a-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9711a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9711a-131">-WorkspaceName</span></span>
<span data-ttu-id="9711a-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="9711a-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9711a-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9711a-133">-WorkspaceObject</span></span>
<span data-ttu-id="9711a-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="9711a-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9711a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9711a-135">-Confirm</span></span>
<span data-ttu-id="9711a-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9711a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9711a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9711a-137">-WhatIf</span></span>
<span data-ttu-id="9711a-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9711a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9711a-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9711a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9711a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9711a-140">CommonParameters</span></span>
<span data-ttu-id="9711a-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9711a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9711a-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9711a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9711a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9711a-143">INPUTS</span></span>

### <span data-ttu-id="9711a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9711a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9711a-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="9711a-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="9711a-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9711a-146">OUTPUTS</span></span>

### <span data-ttu-id="9711a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9711a-147">System.Boolean</span></span>

## <span data-ttu-id="9711a-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9711a-148">NOTES</span></span>

## <span data-ttu-id="9711a-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9711a-149">RELATED LINKS</span></span>
