---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 94773a882a4bb2d29712fff6796d34cff6254df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991959"
---
# <span data-ttu-id="da31f-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="da31f-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="da31f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da31f-102">SYNOPSIS</span></span>
<span data-ttu-id="da31f-103">Остановка триггера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="da31f-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="da31f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da31f-104">SYNTAX</span></span>

### <span data-ttu-id="da31f-105">StopByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da31f-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da31f-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="da31f-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da31f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="da31f-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da31f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da31f-108">DESCRIPTION</span></span>
<span data-ttu-id="da31f-109">В рабочей области триггер **Stop-AzSynapseTrigger** останавливает триггер.</span><span class="sxs-lookup"><span data-stu-id="da31f-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="da31f-110">Если триггер находится в состоянии "Запущено", то триггер останавливается и перестает вызывать конвейеры.</span><span class="sxs-lookup"><span data-stu-id="da31f-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="da31f-111">Если триггер уже находится в состоянии "Остановлено", этот cmdlet не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="da31f-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="da31f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da31f-112">EXAMPLES</span></span>

### <span data-ttu-id="da31f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da31f-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="da31f-114">Остановка триггера ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="da31f-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="da31f-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="da31f-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="da31f-116">Запуск триггера ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="da31f-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="da31f-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="da31f-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="da31f-118">Остановка триггера ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="da31f-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="da31f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da31f-119">PARAMETERS</span></span>

### <span data-ttu-id="da31f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da31f-120">-AsJob</span></span>
<span data-ttu-id="da31f-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="da31f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da31f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da31f-122">-DefaultProfile</span></span>
<span data-ttu-id="da31f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da31f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da31f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da31f-124">-InputObject</span></span>
<span data-ttu-id="da31f-125">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="da31f-125">The trigger object.</span></span>

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

### <span data-ttu-id="da31f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="da31f-126">-Name</span></span>
<span data-ttu-id="da31f-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="da31f-127">The trigger name.</span></span>

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

### <span data-ttu-id="da31f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da31f-128">-PassThru</span></span>
<span data-ttu-id="da31f-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da31f-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="da31f-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="da31f-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="da31f-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da31f-131">-WorkspaceName</span></span>
<span data-ttu-id="da31f-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="da31f-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="da31f-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="da31f-133">-WorkspaceObject</span></span>
<span data-ttu-id="da31f-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="da31f-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="da31f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da31f-135">-Confirm</span></span>
<span data-ttu-id="da31f-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da31f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da31f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da31f-137">-WhatIf</span></span>
<span data-ttu-id="da31f-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da31f-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da31f-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da31f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da31f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da31f-140">CommonParameters</span></span>
<span data-ttu-id="da31f-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da31f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da31f-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da31f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da31f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da31f-143">INPUTS</span></span>

### <span data-ttu-id="da31f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="da31f-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="da31f-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="da31f-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="da31f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da31f-146">OUTPUTS</span></span>

### <span data-ttu-id="da31f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da31f-147">System.Boolean</span></span>

## <span data-ttu-id="da31f-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da31f-148">NOTES</span></span>

## <span data-ttu-id="da31f-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da31f-149">RELATED LINKS</span></span>
