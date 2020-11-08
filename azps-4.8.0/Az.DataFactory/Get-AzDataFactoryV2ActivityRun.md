---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236806"
---
# <span data-ttu-id="a3510-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="a3510-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="a3510-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3510-102">SYNOPSIS</span></span>
<span data-ttu-id="a3510-103">Возвращает сведения о действиях, выполняемых при выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="a3510-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="a3510-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3510-104">SYNTAX</span></span>

### <span data-ttu-id="a3510-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3510-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3510-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a3510-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3510-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3510-107">DESCRIPTION</span></span>
<span data-ttu-id="a3510-108">Командлет **Get-AzDataFactoryV2ActivityRun** получает сведения о выполнении в фабрике данных Azure для указанного конвейера, который произошел в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="a3510-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="a3510-109">Кроме того, можно задать фильтры для имени действия, связанной службы, который выполнял выполнение, и состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="a3510-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="a3510-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3510-110">EXAMPLES</span></span>

### <span data-ttu-id="a3510-111">Пример 1: получение всех действий, выполняемых для конвейерного выполнения</span><span class="sxs-lookup"><span data-stu-id="a3510-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="a3510-112">Эта команда получает подробные сведения обо всех действиях, выполняемых в конвейере с ИДЕНТИФИКАТОРом "f288712d-fb08-4cb8-96ef-82d3b9b30621", которое произошло между "2017-09-01" и "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="a3510-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="a3510-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3510-113">PARAMETERS</span></span>

### <span data-ttu-id="a3510-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="a3510-114">-ActivityName</span></span>
<span data-ttu-id="a3510-115">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="a3510-115">The name of the activity.</span></span>

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

### <span data-ttu-id="a3510-116">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a3510-116">-DataFactory</span></span>
<span data-ttu-id="a3510-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a3510-117">The data factory object.</span></span>

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

### <span data-ttu-id="a3510-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a3510-118">-DataFactoryName</span></span>
<span data-ttu-id="a3510-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a3510-119">The data factory name.</span></span>

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

### <span data-ttu-id="a3510-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3510-120">-DefaultProfile</span></span>
<span data-ttu-id="a3510-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3510-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3510-122">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="a3510-122">-PipelineRunId</span></span>
<span data-ttu-id="a3510-123">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="a3510-123">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="a3510-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3510-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3510-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3510-125">The resource group name.</span></span>

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

### <span data-ttu-id="a3510-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="a3510-126">-RunStartedAfter</span></span>
<span data-ttu-id="a3510-127">Время, по истечении которого началось выполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="a3510-127">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="a3510-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="a3510-128">-RunStartedBefore</span></span>
<span data-ttu-id="a3510-129">Время, до которого началось выполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="a3510-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="a3510-130">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a3510-130">-Status</span></span>
<span data-ttu-id="a3510-131">Состояние выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="a3510-131">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="a3510-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3510-132">CommonParameters</span></span>
<span data-ttu-id="a3510-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3510-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3510-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3510-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3510-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3510-135">INPUTS</span></span>

### <span data-ttu-id="a3510-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a3510-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="a3510-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a3510-137">System.String</span></span>

## <span data-ttu-id="a3510-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3510-138">OUTPUTS</span></span>

### <span data-ttu-id="a3510-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="a3510-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="a3510-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3510-140">NOTES</span></span>

## <span data-ttu-id="a3510-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3510-141">RELATED LINKS</span></span>

[<span data-ttu-id="a3510-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a3510-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a3510-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a3510-143">Get-AzDataFactoryV2PipelineRun</span></span>]()

