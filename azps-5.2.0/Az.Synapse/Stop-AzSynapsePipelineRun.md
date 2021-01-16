---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410244"
---
# <span data-ttu-id="a31f2-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="a31f2-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="a31f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a31f2-103">Остановка запуска конвейера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a31f2-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="a31f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a31f2-104">SYNTAX</span></span>

### <span data-ttu-id="a31f2-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a31f2-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a31f2-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a31f2-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a31f2-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a31f2-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a31f2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a31f2-108">DESCRIPTION</span></span>
<span data-ttu-id="a31f2-109">С **помощью cmdlet Stop-AzSynapsePipelineRun** можно остановить запуск конвейера в рабочей области, заданной с кодом запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="a31f2-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="a31f2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a31f2-110">EXAMPLES</span></span>

### <span data-ttu-id="a31f2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a31f2-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="a31f2-112">Эта команда останавливает работу конвейера с помощью id b9730a13-aa12-4926-a8b3-8e3a974ab0bd в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a31f2-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a31f2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a31f2-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="a31f2-114">Эта команда останавливает работу конвейера с помощью id b9730a13-aa12-4926-a8b3-8e3a974ab0bd в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="a31f2-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a31f2-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a31f2-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="a31f2-116">Эта команда останавливает работу конвейера с помощью id b9730a13-aa12-4926-a8b3-8e3a974ab0bd в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="a31f2-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a31f2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a31f2-117">PARAMETERS</span></span>

### <span data-ttu-id="a31f2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a31f2-118">-AsJob</span></span>
<span data-ttu-id="a31f2-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a31f2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a31f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31f2-120">-DefaultProfile</span></span>
<span data-ttu-id="a31f2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a31f2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a31f2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a31f2-122">-InputObject</span></span>
<span data-ttu-id="a31f2-123">Сведения о запуске конвейера.</span><span class="sxs-lookup"><span data-stu-id="a31f2-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31f2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a31f2-124">-PassThru</span></span>
<span data-ttu-id="a31f2-125">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a31f2-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a31f2-126">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="a31f2-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a31f2-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a31f2-127">-PipelineRunId</span></span>
<span data-ttu-id="a31f2-128">Идентификатор запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="a31f2-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31f2-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a31f2-129">-WorkspaceName</span></span>
<span data-ttu-id="a31f2-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a31f2-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a31f2-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a31f2-131">-WorkspaceObject</span></span>
<span data-ttu-id="a31f2-132">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a31f2-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a31f2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a31f2-133">-Confirm</span></span>
<span data-ttu-id="a31f2-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a31f2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31f2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31f2-135">-WhatIf</span></span>
<span data-ttu-id="a31f2-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a31f2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a31f2-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a31f2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31f2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31f2-138">CommonParameters</span></span>
<span data-ttu-id="a31f2-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31f2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31f2-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a31f2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31f2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a31f2-141">INPUTS</span></span>

### <span data-ttu-id="a31f2-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a31f2-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a31f2-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="a31f2-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="a31f2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a31f2-144">OUTPUTS</span></span>

### <span data-ttu-id="a31f2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a31f2-145">System.Boolean</span></span>

## <span data-ttu-id="a31f2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a31f2-146">NOTES</span></span>

## <span data-ttu-id="a31f2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a31f2-147">RELATED LINKS</span></span>