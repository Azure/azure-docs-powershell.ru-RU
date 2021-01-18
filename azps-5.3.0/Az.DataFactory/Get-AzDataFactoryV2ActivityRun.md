---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508542"
---
# <span data-ttu-id="7b506-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="7b506-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="7b506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b506-102">SYNOPSIS</span></span>
<span data-ttu-id="7b506-103">Сведения о действиях для запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="7b506-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="7b506-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b506-104">SYNTAX</span></span>

### <span data-ttu-id="7b506-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b506-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b506-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7b506-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b506-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b506-107">DESCRIPTION</span></span>
<span data-ttu-id="7b506-108">**Cmdlet Get-AzDataFactoryV2ActivityRun** получает сведения о запусках в фабрике данных Azure для указанного запуска конвейера, который произошел в указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="7b506-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="7b506-109">Кроме того, можно указать фильтры для имени действия, связанного имени службы, который выполнил выполнение, и состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="7b506-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="7b506-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b506-110">EXAMPLES</span></span>

### <span data-ttu-id="7b506-111">Пример 1. Все действия для запуска конвейера</span><span class="sxs-lookup"><span data-stu-id="7b506-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="7b506-112">Эта команда получает сведения обо всех действиях, которые выполняется в конвейере с помощью ID "f288712d-fb08-4cb8-96ef-82d3b9b30621", которые произошли между "2017-09-01" и "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="7b506-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="7b506-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b506-113">PARAMETERS</span></span>

### <span data-ttu-id="7b506-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="7b506-114">-ActivityName</span></span>
<span data-ttu-id="7b506-115">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="7b506-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b506-116">-DataFactory</span></span>
<span data-ttu-id="7b506-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7b506-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7b506-118">-DataFactoryName</span></span>
<span data-ttu-id="7b506-119">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7b506-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b506-120">-DefaultProfile</span></span>
<span data-ttu-id="7b506-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b506-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b506-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="7b506-122">-PipelineRunId</span></span>
<span data-ttu-id="7b506-123">Запустите ИД конвейера.</span><span class="sxs-lookup"><span data-stu-id="7b506-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b506-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b506-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b506-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="7b506-126">-RunStartedAfter</span></span>
<span data-ttu-id="7b506-127">Время запуска (или после запуска) конвейера.</span><span class="sxs-lookup"><span data-stu-id="7b506-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="7b506-128">-RunStartedBefore</span></span>
<span data-ttu-id="7b506-129">Время запуска конвейера или до его запуска.</span><span class="sxs-lookup"><span data-stu-id="7b506-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-130">-Status</span><span class="sxs-lookup"><span data-stu-id="7b506-130">-Status</span></span>
<span data-ttu-id="7b506-131">Состояние запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="7b506-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b506-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b506-132">CommonParameters</span></span>
<span data-ttu-id="7b506-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b506-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b506-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b506-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b506-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b506-135">INPUTS</span></span>

### <span data-ttu-id="7b506-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7b506-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="7b506-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7b506-137">System.String</span></span>

## <span data-ttu-id="7b506-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b506-138">OUTPUTS</span></span>

### <span data-ttu-id="7b506-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="7b506-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="7b506-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b506-140">NOTES</span></span>

## <span data-ttu-id="7b506-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b506-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b506-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7b506-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7b506-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="7b506-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

