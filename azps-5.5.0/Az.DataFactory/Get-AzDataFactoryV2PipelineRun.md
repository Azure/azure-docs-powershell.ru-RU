---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232932"
---
# <span data-ttu-id="362e7-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="362e7-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="362e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="362e7-102">SYNOPSIS</span></span>
<span data-ttu-id="362e7-103">Сведения о запуске конвейера.</span><span class="sxs-lookup"><span data-stu-id="362e7-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="362e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="362e7-104">SYNTAX</span></span>

### <span data-ttu-id="362e7-105">ByFactoryNameByRunId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="362e7-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="362e7-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="362e7-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="362e7-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="362e7-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="362e7-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="362e7-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="362e7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="362e7-109">DESCRIPTION</span></span>
<span data-ttu-id="362e7-110">Команда **Get-AzDataFactoryV2PipelineRun** возвращает сведения о запуске для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="362e7-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="362e7-111">Если задан PipelineRunId, в нем будут показаны сведения о запуске с этим ИД.</span><span class="sxs-lookup"><span data-stu-id="362e7-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="362e7-112">Если значение PipelineRunId не указано, в нем высвечены все запускы для каналов, которые произошли между значениями LastUpdatedAfter и LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="362e7-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="362e7-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="362e7-113">EXAMPLES</span></span>

### <span data-ttu-id="362e7-114">Пример 1. Получить сведения о запуске конвейера</span><span class="sxs-lookup"><span data-stu-id="362e7-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

<span data-ttu-id="362e7-115">Эта команда получает сведения о запуске конвейера с помощью ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="362e7-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="362e7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="362e7-116">PARAMETERS</span></span>

### <span data-ttu-id="362e7-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="362e7-117">-DataFactory</span></span>
<span data-ttu-id="362e7-118">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="362e7-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="362e7-119">-DataFactoryName</span></span>
<span data-ttu-id="362e7-120">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="362e7-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362e7-121">-DefaultProfile</span></span>
<span data-ttu-id="362e7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="362e7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="362e7-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="362e7-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="362e7-124">Время, в которое или после запуска конвейера обновлялся формат ISO8601.</span><span class="sxs-lookup"><span data-stu-id="362e7-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="362e7-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="362e7-126">Время, в которое или до начала запуска конвейера обновлялся формат ISO8601.</span><span class="sxs-lookup"><span data-stu-id="362e7-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="362e7-127">-PipelineName</span></span>
<span data-ttu-id="362e7-128">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="362e7-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="362e7-129">-PipelineRunId</span></span>
<span data-ttu-id="362e7-130">Run ID of the pipeline.</span><span class="sxs-lookup"><span data-stu-id="362e7-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="362e7-131">-ResourceGroupName</span></span>
<span data-ttu-id="362e7-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="362e7-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="362e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362e7-133">CommonParameters</span></span>
<span data-ttu-id="362e7-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362e7-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="362e7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362e7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="362e7-136">INPUTS</span></span>

### <span data-ttu-id="362e7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="362e7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="362e7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="362e7-138">System.String</span></span>

## <span data-ttu-id="362e7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="362e7-139">OUTPUTS</span></span>

### <span data-ttu-id="362e7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="362e7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="362e7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="362e7-141">NOTES</span></span>

## <span data-ttu-id="362e7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="362e7-142">RELATED LINKS</span></span>

[<span data-ttu-id="362e7-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="362e7-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="362e7-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="362e7-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

