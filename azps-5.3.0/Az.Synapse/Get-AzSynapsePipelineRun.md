---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505563"
---
# <span data-ttu-id="d41c0-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="d41c0-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="d41c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d41c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d41c0-103">Сведения о запуске конвейера.</span><span class="sxs-lookup"><span data-stu-id="d41c0-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="d41c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d41c0-104">SYNTAX</span></span>

### <span data-ttu-id="d41c0-105">GetByNameAndId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d41c0-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d41c0-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="d41c0-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d41c0-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="d41c0-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d41c0-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="d41c0-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d41c0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d41c0-109">DESCRIPTION</span></span>
<span data-ttu-id="d41c0-110">Команда **Get-AzSynapsePipelineRun** возвращает сведения о запуске для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="d41c0-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="d41c0-111">Если задан PipelineRunId, в нем будут показаны сведения о запуске с этим ИД.</span><span class="sxs-lookup"><span data-stu-id="d41c0-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="d41c0-112">Если значение PipelineRunId не указано, в нем будут показаны сведения обо всех запусках для каналов, которые произошли между значениями RunStartedAfter и RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="d41c0-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="d41c0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d41c0-113">EXAMPLES</span></span>

### <span data-ttu-id="d41c0-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d41c0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="d41c0-115">Эта команда получает сведения о запуске конвейера с помощью ИД "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="d41c0-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="d41c0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d41c0-116">PARAMETERS</span></span>

### <span data-ttu-id="d41c0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41c0-117">-DefaultProfile</span></span>
<span data-ttu-id="d41c0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d41c0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d41c0-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d41c0-119">-PipelineName</span></span>
<span data-ttu-id="d41c0-120">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="d41c0-120">The pipeline name.</span></span>

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

### <span data-ttu-id="d41c0-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d41c0-121">-PipelineRunId</span></span>
<span data-ttu-id="d41c0-122">Идентификатор запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="d41c0-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="d41c0-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="d41c0-123">-RunStartedAfter</span></span>
<span data-ttu-id="d41c0-124">Время, в течение или после которого событие запуска обновлялось в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="d41c0-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d41c0-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="d41c0-125">-RunStartedBefore</span></span>
<span data-ttu-id="d41c0-126">Время, в течение или до которого событие запуска обновлялось в формате ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="d41c0-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="d41c0-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d41c0-127">-WorkspaceName</span></span>
<span data-ttu-id="d41c0-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d41c0-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d41c0-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d41c0-129">-WorkspaceObject</span></span>
<span data-ttu-id="d41c0-130">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d41c0-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d41c0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41c0-131">CommonParameters</span></span>
<span data-ttu-id="d41c0-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41c0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41c0-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d41c0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41c0-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d41c0-134">INPUTS</span></span>

### <span data-ttu-id="d41c0-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d41c0-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d41c0-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d41c0-136">OUTPUTS</span></span>

### <span data-ttu-id="d41c0-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="d41c0-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="d41c0-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d41c0-138">NOTES</span></span>

## <span data-ttu-id="d41c0-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d41c0-139">RELATED LINKS</span></span>
