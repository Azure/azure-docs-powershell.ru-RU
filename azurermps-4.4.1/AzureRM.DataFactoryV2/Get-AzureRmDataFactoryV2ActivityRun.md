---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2000e489dcb5a0bab384ac0aad8a1ffbe53aba15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734872"
---
# <span data-ttu-id="c2a1f-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="c2a1f-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="c2a1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a1f-103">Возвращает сведения о действиях, выполняемых при выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2a1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2a1f-104">SYNTAX</span></span>

### <span data-ttu-id="c2a1f-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2a1f-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="c2a1f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c2a1f-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-DataFactory] <PSDataFactory>
```


## <span data-ttu-id="c2a1f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2a1f-107">DESCRIPTION</span></span>

<span data-ttu-id="c2a1f-108">Командлет **Get-AzureRmDataFactoryV2ActivityRun** получает сведения о выполнении в фабрике данных Azure для указанного конвейера, который произошел в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="c2a1f-109">Кроме того, можно задать фильтры для имени действия, связанной службы, который выполнял выполнение, и состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="c2a1f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2a1f-110">EXAMPLES</span></span>

### <span data-ttu-id="c2a1f-111">Пример 1: получение всех действий, выполняемых для конвейерного выполнения</span><span class="sxs-lookup"><span data-stu-id="c2a1f-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}

```

<span data-ttu-id="c2a1f-112">Эта команда получает подробные сведения обо всех действиях, выполняемых в конвейере с ИДЕНТИФИКАТОРом "f288712d-fb08-4cb8-96ef-82d3b9b30621", которое произошло между "2017-09-01" и "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="c2a1f-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="c2a1f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2a1f-113">PARAMETERS</span></span>

### <span data-ttu-id="c2a1f-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="c2a1f-114">-ActivityName</span></span>
<span data-ttu-id="c2a1f-115">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-115">The name of the activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-116">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-116">-DataFactory</span></span>
<span data-ttu-id="c2a1f-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-117">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2a1f-118">-DataFactoryName</span></span>
<span data-ttu-id="c2a1f-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-120">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c2a1f-120">-LinkedServiceName</span></span>
<span data-ttu-id="c2a1f-121">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-121">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="c2a1f-122">-PipelineRunId</span></span>
<span data-ttu-id="c2a1f-123">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-123">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a1f-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2a1f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c2a1f-126">-RunStartedAfter</span></span>
<span data-ttu-id="c2a1f-127">Время, по истечении которого началось выполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c2a1f-128">-RunStartedBefore</span></span>
<span data-ttu-id="c2a1f-129">Время, до которого началось выполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a1f-130">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c2a1f-130">-Status</span></span>
<span data-ttu-id="c2a1f-131">Состояние выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2a1f-131">The status of the pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c2a1f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2a1f-132">INPUTS</span></span>

### <span data-ttu-id="c2a1f-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c2a1f-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="c2a1f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2a1f-134">System.String</span></span>


## <span data-ttu-id="c2a1f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2a1f-135">OUTPUTS</span></span>

### <span data-ttu-id="c2a1f-136">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="c2a1f-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c2a1f-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="c2a1f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>


## <span data-ttu-id="c2a1f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2a1f-138">NOTES</span></span>

## <span data-ttu-id="c2a1f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2a1f-139">RELATED LINKS</span></span>
[<span data-ttu-id="c2a1f-140">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="c2a1f-140">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="c2a1f-141">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="c2a1f-141">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

