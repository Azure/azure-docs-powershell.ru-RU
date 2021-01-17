---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416791"
---
# <span data-ttu-id="7aa9d-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="7aa9d-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="7aa9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aa9d-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa9d-103">Вызывает конвейер, чтобы запустить его.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="7aa9d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7aa9d-104">SYNTAX</span></span>

### <span data-ttu-id="7aa9d-105">NewByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7aa9d-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa9d-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="7aa9d-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa9d-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="7aa9d-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aa9d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa9d-108">DESCRIPTION</span></span>
<span data-ttu-id="7aa9d-109">Команда **Invoke-AzSynapsePipeline** запускается в указанном канале и возвращает для этого запуска его ИД.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="7aa9d-110">Этот GUID можно передать **Get-AzSynapsePipelineRun** или **Get-AzSynapseActivityRun** для получения дополнительных сведений об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="7aa9d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7aa9d-111">EXAMPLES</span></span>

### <span data-ttu-id="7aa9d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7aa9d-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="7aa9d-113">Эта команда запускает канал ContosoPipeline в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7aa9d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7aa9d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="7aa9d-115">Эта команда запускает конвейер ContosoPipeline в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7aa9d-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7aa9d-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="7aa9d-117">Эта команда запускает конвейер ContosoPipeline в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7aa9d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aa9d-118">PARAMETERS</span></span>

### <span data-ttu-id="7aa9d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7aa9d-119">-AsJob</span></span>
<span data-ttu-id="7aa9d-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7aa9d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7aa9d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa9d-121">-DefaultProfile</span></span>
<span data-ttu-id="7aa9d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aa9d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7aa9d-123">-InputObject</span></span>
<span data-ttu-id="7aa9d-124">Сведения о запуске конвейера.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9d-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="7aa9d-125">-IsRecovery</span></span>
<span data-ttu-id="7aa9d-126">Флаг режима восстановления.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-126">Recovery mode flag.</span></span>
<span data-ttu-id="7aa9d-127">Если для режима восстановления задано истинность, указанный канал, на который указывает ссылка, запустится, и новый запуск будет сгрупп указан в том же groupId.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="7aa9d-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="7aa9d-128">-Parameter</span></span>
<span data-ttu-id="7aa9d-129">Параметры для запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="7aa9d-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="7aa9d-130">-ParameterFile</span></span>
<span data-ttu-id="7aa9d-131">Имя файла с параметрами для запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="7aa9d-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="7aa9d-132">-PipelineName</span></span>
<span data-ttu-id="7aa9d-133">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9d-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="7aa9d-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="7aa9d-135">Повторно запустится ИД конвейера.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="7aa9d-136">Если задан ид запуска, для создания нового запуска будут использоваться параметры указанного запуска.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="7aa9d-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="7aa9d-137">-StartActivityName</span></span>
<span data-ttu-id="7aa9d-138">В режиме восстановления повторное запуск будет начинаться с этого действия.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="7aa9d-139">Если не указано, будут выполниться все действия.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="7aa9d-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7aa9d-140">-WorkspaceName</span></span>
<span data-ttu-id="7aa9d-141">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9d-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7aa9d-142">-WorkspaceObject</span></span>
<span data-ttu-id="7aa9d-143">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7aa9d-144">-Confirm</span></span>
<span data-ttu-id="7aa9d-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa9d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa9d-146">-WhatIf</span></span>
<span data-ttu-id="7aa9d-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa9d-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa9d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa9d-149">CommonParameters</span></span>
<span data-ttu-id="7aa9d-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa9d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa9d-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7aa9d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa9d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7aa9d-152">INPUTS</span></span>

### <span data-ttu-id="7aa9d-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="7aa9d-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="7aa9d-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7aa9d-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7aa9d-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7aa9d-155">OUTPUTS</span></span>

### <span data-ttu-id="7aa9d-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="7aa9d-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="7aa9d-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7aa9d-157">NOTES</span></span>

## <span data-ttu-id="7aa9d-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7aa9d-158">RELATED LINKS</span></span>
