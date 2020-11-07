---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 2acfb9a0ebbbaef2fee92ef521d10c1c17fa5e48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721518"
---
# <span data-ttu-id="f28aa-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f28aa-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="f28aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f28aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f28aa-103">Получает сведения о выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="f28aa-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="f28aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f28aa-104">SYNTAX</span></span>

### <span data-ttu-id="f28aa-105">ByFactoryNameByRunId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f28aa-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f28aa-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="f28aa-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f28aa-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="f28aa-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f28aa-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="f28aa-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f28aa-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28aa-109">DESCRIPTION</span></span>
<span data-ttu-id="f28aa-110">Команда **Get-AzDataFactoryV2PipelineRun** возвращает сведения о запусках для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="f28aa-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="f28aa-111">Если указан PipelineRunId, он отображает сведения для запуска с этим ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="f28aa-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="f28aa-112">Если PipelineRunId не указан, выводятся сведения обо всех запусках конвейеров, которые произошли между значениями LastUpdatedAfter и LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="f28aa-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="f28aa-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f28aa-113">EXAMPLES</span></span>

### <span data-ttu-id="f28aa-114">Пример 1: получение сведений для конвейерного выполнения</span><span class="sxs-lookup"><span data-stu-id="f28aa-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="f28aa-115">Эта команда получает подробные сведения о выполнении конвейера с ИДЕНТИФИКАТОРом "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="f28aa-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="f28aa-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f28aa-116">PARAMETERS</span></span>

### <span data-ttu-id="f28aa-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="f28aa-117">-DataFactory</span></span>
<span data-ttu-id="f28aa-118">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f28aa-118">The data factory object.</span></span>

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

### <span data-ttu-id="f28aa-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f28aa-119">-DataFactoryName</span></span>
<span data-ttu-id="f28aa-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f28aa-120">The data factory name.</span></span>

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

### <span data-ttu-id="f28aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28aa-121">-DefaultProfile</span></span>
<span data-ttu-id="f28aa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f28aa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f28aa-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="f28aa-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="f28aa-124">Время, по истечении которого выполнение конвейера было Обновлено в ISO8601 формате.</span><span class="sxs-lookup"><span data-stu-id="f28aa-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="f28aa-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="f28aa-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="f28aa-126">Время, в течение которого выполнение конвейера было Обновлено в формате ISO8601 или до него.</span><span class="sxs-lookup"><span data-stu-id="f28aa-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="f28aa-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f28aa-127">-PipelineName</span></span>
<span data-ttu-id="f28aa-128">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="f28aa-128">The pipeline name.</span></span>

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

### <span data-ttu-id="f28aa-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="f28aa-129">-PipelineRunId</span></span>
<span data-ttu-id="f28aa-130">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="f28aa-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="f28aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="f28aa-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f28aa-132">The resource group name.</span></span>

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

### <span data-ttu-id="f28aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28aa-133">CommonParameters</span></span>
<span data-ttu-id="f28aa-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f28aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28aa-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f28aa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28aa-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f28aa-136">INPUTS</span></span>

### <span data-ttu-id="f28aa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f28aa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="f28aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f28aa-138">System.String</span></span>

## <span data-ttu-id="f28aa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28aa-139">OUTPUTS</span></span>

### <span data-ttu-id="f28aa-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="f28aa-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="f28aa-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f28aa-141">NOTES</span></span>

## <span data-ttu-id="f28aa-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f28aa-142">RELATED LINKS</span></span>

[<span data-ttu-id="f28aa-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f28aa-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="f28aa-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="f28aa-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

