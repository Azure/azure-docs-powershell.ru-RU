---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397228"
---
# <span data-ttu-id="c484e-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="c484e-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="c484e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c484e-102">SYNOPSIS</span></span>
<span data-ttu-id="c484e-103">Сведения о запуске конвейера.</span><span class="sxs-lookup"><span data-stu-id="c484e-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="c484e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c484e-104">SYNTAX</span></span>

### <span data-ttu-id="c484e-105">GetByNameAndId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c484e-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c484e-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="c484e-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c484e-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="c484e-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c484e-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="c484e-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c484e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c484e-109">DESCRIPTION</span></span>
<span data-ttu-id="c484e-110">Команда **Get-AzSynapsePipelineRun** возвращает сведения о запуске для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="c484e-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="c484e-111">Если задан PipelineRunId, в нем будут показаны сведения о запуске с этим ИД.</span><span class="sxs-lookup"><span data-stu-id="c484e-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="c484e-112">Если значение PipelineRunId не указано, в нем будут показаны сведения обо всех запусках для каналов, которые произошли между значениями RunStartedAfter и RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="c484e-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="c484e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c484e-113">EXAMPLES</span></span>

### <span data-ttu-id="c484e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c484e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="c484e-115">Эта команда получает сведения о запуске конвейера с помощью ИД "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="c484e-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="c484e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c484e-116">PARAMETERS</span></span>

### <span data-ttu-id="c484e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c484e-117">-DefaultProfile</span></span>
<span data-ttu-id="c484e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c484e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c484e-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="c484e-119">-PipelineName</span></span>
<span data-ttu-id="c484e-120">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="c484e-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c484e-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c484e-121">-PipelineRunId</span></span>
<span data-ttu-id="c484e-122">Идентификатор запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="c484e-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c484e-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c484e-123">-RunStartedAfter</span></span>
<span data-ttu-id="c484e-124">Время, в течение или после которого событие было обновлено в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c484e-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c484e-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c484e-125">-RunStartedBefore</span></span>
<span data-ttu-id="c484e-126">Время, в течение или до которого событие запуска обновлялось в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c484e-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c484e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c484e-127">-WorkspaceName</span></span>
<span data-ttu-id="c484e-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c484e-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c484e-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c484e-129">-WorkspaceObject</span></span>
<span data-ttu-id="c484e-130">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c484e-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c484e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c484e-131">CommonParameters</span></span>
<span data-ttu-id="c484e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c484e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c484e-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c484e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c484e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c484e-134">INPUTS</span></span>

### <span data-ttu-id="c484e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c484e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c484e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c484e-136">OUTPUTS</span></span>

### <span data-ttu-id="c484e-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="c484e-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="c484e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c484e-138">NOTES</span></span>

## <span data-ttu-id="c484e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c484e-139">RELATED LINKS</span></span>
