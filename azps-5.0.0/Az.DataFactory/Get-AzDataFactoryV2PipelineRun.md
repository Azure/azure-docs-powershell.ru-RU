---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313997"
---
# <span data-ttu-id="4e542-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4e542-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="4e542-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e542-102">SYNOPSIS</span></span>
<span data-ttu-id="4e542-103">Получает сведения о выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="4e542-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="4e542-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e542-104">SYNTAX</span></span>

### <span data-ttu-id="4e542-105">ByFactoryNameByRunId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e542-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e542-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="4e542-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e542-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="4e542-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e542-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="4e542-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e542-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e542-109">DESCRIPTION</span></span>
<span data-ttu-id="4e542-110">Команда **Get-AzDataFactoryV2PipelineRun** возвращает сведения о запусках для указанного конвейера.</span><span class="sxs-lookup"><span data-stu-id="4e542-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4e542-111">Если указан PipelineRunId, он отображает сведения для запуска с этим ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="4e542-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4e542-112">Если PipelineRunId не указан, выводятся сведения обо всех запусках конвейеров, которые произошли между значениями LastUpdatedAfter и LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="4e542-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="4e542-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e542-113">EXAMPLES</span></span>

### <span data-ttu-id="4e542-114">Пример 1: получение сведений для конвейерного выполнения</span><span class="sxs-lookup"><span data-stu-id="4e542-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="4e542-115">Эта команда получает подробные сведения о выполнении конвейера с ИДЕНТИФИКАТОРом "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="4e542-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4e542-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e542-116">PARAMETERS</span></span>

### <span data-ttu-id="4e542-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="4e542-117">-DataFactory</span></span>
<span data-ttu-id="4e542-118">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4e542-118">The data factory object.</span></span>

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

### <span data-ttu-id="4e542-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4e542-119">-DataFactoryName</span></span>
<span data-ttu-id="4e542-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4e542-120">The data factory name.</span></span>

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

### <span data-ttu-id="4e542-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e542-121">-DefaultProfile</span></span>
<span data-ttu-id="4e542-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e542-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e542-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="4e542-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="4e542-124">Время, по истечении которого выполнение конвейера было Обновлено в ISO8601 формате.</span><span class="sxs-lookup"><span data-stu-id="4e542-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="4e542-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="4e542-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="4e542-126">Время, в течение которого выполнение конвейера было Обновлено в формате ISO8601 или до него.</span><span class="sxs-lookup"><span data-stu-id="4e542-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="4e542-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4e542-127">-PipelineName</span></span>
<span data-ttu-id="4e542-128">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="4e542-128">The pipeline name.</span></span>

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

### <span data-ttu-id="4e542-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4e542-129">-PipelineRunId</span></span>
<span data-ttu-id="4e542-130">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="4e542-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="4e542-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e542-131">-ResourceGroupName</span></span>
<span data-ttu-id="4e542-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e542-132">The resource group name.</span></span>

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

### <span data-ttu-id="4e542-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e542-133">CommonParameters</span></span>
<span data-ttu-id="4e542-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e542-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e542-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e542-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e542-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e542-136">INPUTS</span></span>

### <span data-ttu-id="4e542-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4e542-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="4e542-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4e542-138">System.String</span></span>

## <span data-ttu-id="4e542-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e542-139">OUTPUTS</span></span>

### <span data-ttu-id="4e542-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="4e542-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4e542-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e542-141">NOTES</span></span>

## <span data-ttu-id="4e542-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e542-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e542-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4e542-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4e542-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="4e542-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

