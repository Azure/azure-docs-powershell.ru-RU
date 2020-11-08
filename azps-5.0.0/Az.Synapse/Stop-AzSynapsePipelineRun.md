---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246600"
---
# <span data-ttu-id="047db-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="047db-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="047db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="047db-102">SYNOPSIS</span></span>
<span data-ttu-id="047db-103">Останавливает выполнение конвейера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="047db-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="047db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="047db-104">SYNTAX</span></span>

### <span data-ttu-id="047db-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="047db-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="047db-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="047db-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="047db-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="047db-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="047db-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="047db-108">DESCRIPTION</span></span>
<span data-ttu-id="047db-109">Командлет **Stop-AzSynapsePipelineRun** останавливает выполнение конвейера в рабочей области, ЗАданной идентификатором запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="047db-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="047db-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="047db-110">EXAMPLES</span></span>

### <span data-ttu-id="047db-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="047db-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="047db-112">Эта команда останавливает конвейер с ИД b9730a13-AA12-4926-a8b3-8e3a974ab0bd в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="047db-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="047db-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="047db-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="047db-114">Эта команда останавливает процесс конвейера с идентификатором b9730a13-AA12-4926-a8b3-8e3a974ab0bd в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="047db-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="047db-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="047db-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="047db-116">Эта команда останавливает процесс конвейера с идентификатором b9730a13-AA12-4926-a8b3-8e3a974ab0bd в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="047db-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="047db-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="047db-117">PARAMETERS</span></span>

### <span data-ttu-id="047db-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="047db-118">-AsJob</span></span>
<span data-ttu-id="047db-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="047db-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="047db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047db-120">-DefaultProfile</span></span>
<span data-ttu-id="047db-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="047db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="047db-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="047db-122">-InputObject</span></span>
<span data-ttu-id="047db-123">Сведения о выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="047db-123">The information about the pipeline run.</span></span>

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

### <span data-ttu-id="047db-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="047db-124">-PassThru</span></span>
<span data-ttu-id="047db-125">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="047db-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="047db-126">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="047db-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="047db-127">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="047db-127">-PipelineRunId</span></span>
<span data-ttu-id="047db-128">Идентификатор выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="047db-128">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="047db-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="047db-129">-WorkspaceName</span></span>
<span data-ttu-id="047db-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="047db-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="047db-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="047db-131">-WorkspaceObject</span></span>
<span data-ttu-id="047db-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="047db-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="047db-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="047db-133">-Confirm</span></span>
<span data-ttu-id="047db-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="047db-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="047db-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="047db-135">-WhatIf</span></span>
<span data-ttu-id="047db-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="047db-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="047db-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="047db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="047db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047db-138">CommonParameters</span></span>
<span data-ttu-id="047db-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="047db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047db-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="047db-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047db-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="047db-141">INPUTS</span></span>

### <span data-ttu-id="047db-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="047db-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="047db-143">Microsoft. Azure. Commands. Synapse. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="047db-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="047db-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="047db-144">OUTPUTS</span></span>

### <span data-ttu-id="047db-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="047db-145">System.Boolean</span></span>

## <span data-ttu-id="047db-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="047db-146">NOTES</span></span>

## <span data-ttu-id="047db-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="047db-147">RELATED LINKS</span></span>
