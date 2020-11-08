---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077476"
---
# <span data-ttu-id="d3170-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d3170-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="d3170-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3170-102">SYNOPSIS</span></span>
<span data-ttu-id="d3170-103">Вызывает конвейер, чтобы запустить его для запуска.</span><span class="sxs-lookup"><span data-stu-id="d3170-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="d3170-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3170-104">SYNTAX</span></span>

### <span data-ttu-id="d3170-105">NewByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3170-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3170-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="d3170-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3170-107">NewByObject</span><span class="sxs-lookup"><span data-stu-id="d3170-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3170-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3170-108">DESCRIPTION</span></span>
<span data-ttu-id="d3170-109">Команда **Invoke-AzSynapsePipeline** запускает выполнение в указанном конвейере и возвращает идентификатор для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="d3170-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="d3170-110">Этот GUID можно передать в **Get-AzSynapsePipelineRun** или **Get-AzSynapseActivityRun** , чтобы получить дополнительные сведения об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="d3170-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="d3170-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3170-111">EXAMPLES</span></span>

### <span data-ttu-id="d3170-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d3170-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="d3170-113">Эта команда запускает выполнение для конвейера с именем ContosoPipeline в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d3170-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d3170-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d3170-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="d3170-115">Эта команда запускает выполнение для конвейера с именем ContosoPipeline в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3170-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d3170-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d3170-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="d3170-117">Эта команда запускает выполнение для конвейера с именем ContosoPipeline в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3170-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d3170-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3170-118">PARAMETERS</span></span>

### <span data-ttu-id="d3170-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3170-119">-AsJob</span></span>
<span data-ttu-id="d3170-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d3170-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3170-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3170-121">-DefaultProfile</span></span>
<span data-ttu-id="d3170-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3170-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3170-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3170-123">-InputObject</span></span>
<span data-ttu-id="d3170-124">Сведения о выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3170-124">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="d3170-125">-NORECOVERY</span><span class="sxs-lookup"><span data-stu-id="d3170-125">-IsRecovery</span></span>
<span data-ttu-id="d3170-126">Флаг режима восстановления.</span><span class="sxs-lookup"><span data-stu-id="d3170-126">Recovery mode flag.</span></span>
<span data-ttu-id="d3170-127">Если для режима восстановления установлено значение true, выполнение указанного конвейера, на который указывает ссылка, и новый прогон будут сгруппированы в том же элементе groupId.</span><span class="sxs-lookup"><span data-stu-id="d3170-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="d3170-128">-Параметр</span><span class="sxs-lookup"><span data-stu-id="d3170-128">-Parameter</span></span>
<span data-ttu-id="d3170-129">Параметры для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3170-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="d3170-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="d3170-130">-ParameterFile</span></span>
<span data-ttu-id="d3170-131">Имя файла с параметрами для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3170-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="d3170-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d3170-132">-PipelineName</span></span>
<span data-ttu-id="d3170-133">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3170-133">The pipeline name.</span></span>

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

### <span data-ttu-id="d3170-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d3170-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="d3170-135">Идентификатор запускаемого конвейера для повторного выполнения.</span><span class="sxs-lookup"><span data-stu-id="d3170-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="d3170-136">Если указан идентификатор запуска, для создания нового запуска будут использоваться параметры указанного запуска.</span><span class="sxs-lookup"><span data-stu-id="d3170-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="d3170-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="d3170-137">-StartActivityName</span></span>
<span data-ttu-id="d3170-138">В режиме восстановления повторный запуск начнется с этого действия.</span><span class="sxs-lookup"><span data-stu-id="d3170-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="d3170-139">Если не указано, будут запущены все действия.</span><span class="sxs-lookup"><span data-stu-id="d3170-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="d3170-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3170-140">-WorkspaceName</span></span>
<span data-ttu-id="d3170-141">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d3170-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d3170-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d3170-142">-WorkspaceObject</span></span>
<span data-ttu-id="d3170-143">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d3170-143">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d3170-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3170-144">-Confirm</span></span>
<span data-ttu-id="d3170-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3170-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3170-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3170-146">-WhatIf</span></span>
<span data-ttu-id="d3170-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3170-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3170-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3170-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3170-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3170-149">CommonParameters</span></span>
<span data-ttu-id="d3170-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3170-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3170-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3170-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3170-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3170-152">INPUTS</span></span>

### <span data-ttu-id="d3170-153">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="d3170-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="d3170-154">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3170-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d3170-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3170-155">OUTPUTS</span></span>

### <span data-ttu-id="d3170-156">Microsoft. Azure. Commands. Synapse. Models. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="d3170-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="d3170-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3170-157">NOTES</span></span>

## <span data-ttu-id="d3170-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3170-158">RELATED LINKS</span></span>
