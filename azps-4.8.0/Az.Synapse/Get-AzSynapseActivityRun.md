---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235703"
---
# <span data-ttu-id="32eb3-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="32eb3-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="32eb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="32eb3-103">Возвращает сведения о действиях, выполняемых при выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="32eb3-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="32eb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32eb3-104">SYNTAX</span></span>

### <span data-ttu-id="32eb3-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32eb3-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32eb3-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="32eb3-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32eb3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32eb3-107">DESCRIPTION</span></span>
<span data-ttu-id="32eb3-108">Командлет **Get-AzSynapseActivityRun** получает сведения о запусках в рабочей области для указанного конвейера, который произошел в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="32eb3-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="32eb3-109">Кроме того, можно задать фильтры для имени действия и состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="32eb3-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="32eb3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32eb3-110">EXAMPLES</span></span>

### <span data-ttu-id="32eb3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32eb3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="32eb3-112">Эта команда получает сведения обо всех действиях, выполняемых в конвейере с именем ContosoPipeline Run с ИДЕНТИФИКАТОРом "f288712d-fb08-4cb8-96ef-82d3b9b30621", который находится между "2018-09-01T21:00" и "2018-09-30T21:00".</span><span class="sxs-lookup"><span data-stu-id="32eb3-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="32eb3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32eb3-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="32eb3-114">Эта команда получает сведения обо всех действиях, выполняемых в конвейере с именем ContosoPipeline Run с ИДЕНТИФИКАТОРом "f288712d-fb08-4cb8-96ef-82d3b9b30621", который находится между "2018-09-01T21:00" и "2018-09-30T21:00" через конвейер.</span><span class="sxs-lookup"><span data-stu-id="32eb3-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="32eb3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32eb3-115">PARAMETERS</span></span>

### <span data-ttu-id="32eb3-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="32eb3-116">-ActivityName</span></span>
<span data-ttu-id="32eb3-117">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="32eb3-117">The name of the activity.</span></span>

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

### <span data-ttu-id="32eb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eb3-118">-DefaultProfile</span></span>
<span data-ttu-id="32eb3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32eb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32eb3-120">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="32eb3-120">-PipelineName</span></span>
<span data-ttu-id="32eb3-121">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="32eb3-121">The pipeline name.</span></span>

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

### <span data-ttu-id="32eb3-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="32eb3-122">-PipelineRunId</span></span>
<span data-ttu-id="32eb3-123">Идентификатор выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="32eb3-123">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="32eb3-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="32eb3-124">-RunStartedAfter</span></span>
<span data-ttu-id="32eb3-125">Время, в течение или после которого событие "выполнение" было Обновлено в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="32eb3-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32eb3-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="32eb3-126">-RunStartedBefore</span></span>
<span data-ttu-id="32eb3-127">Время, в течение которого событие запуска было Обновлено в формате ISO 8601, или до него.</span><span class="sxs-lookup"><span data-stu-id="32eb3-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32eb3-128">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="32eb3-128">-Status</span></span>
<span data-ttu-id="32eb3-129">Состояние выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="32eb3-129">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="32eb3-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="32eb3-130">-WorkspaceName</span></span>
<span data-ttu-id="32eb3-131">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="32eb3-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32eb3-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="32eb3-132">-WorkspaceObject</span></span>
<span data-ttu-id="32eb3-133">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="32eb3-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32eb3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eb3-134">CommonParameters</span></span>
<span data-ttu-id="32eb3-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32eb3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32eb3-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32eb3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eb3-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32eb3-137">INPUTS</span></span>

### <span data-ttu-id="32eb3-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="32eb3-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="32eb3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32eb3-139">OUTPUTS</span></span>

### <span data-ttu-id="32eb3-140">Microsoft. Azure. Commands. Synapse. Models. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="32eb3-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="32eb3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="32eb3-141">NOTES</span></span>

## <span data-ttu-id="32eb3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32eb3-142">RELATED LINKS</span></span>
