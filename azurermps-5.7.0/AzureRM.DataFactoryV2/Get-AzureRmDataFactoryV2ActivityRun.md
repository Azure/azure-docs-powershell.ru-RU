---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 300aad37f2dede64a4adebc4f1a9d9eb9cc43743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559099"
---
# <span data-ttu-id="9dc1b-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="9dc1b-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="9dc1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc1b-103">Возвращает сведения о действиях, выполняемых при выполнении конвейера.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dc1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dc1b-104">SYNTAX</span></span>

### <span data-ttu-id="9dc1b-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9dc1b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dc1b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9dc1b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dc1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc1b-107">DESCRIPTION</span></span>
<span data-ttu-id="9dc1b-108">Командлет **Get-AzureRmDataFactoryV2ActivityRun** получает сведения о выполнении в фабрике данных Azure для указанного конвейера, который произошел в течение заданного периода.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="9dc1b-109">Кроме того, можно задать фильтры для имени действия, связанной службы, который выполнял выполнение, и состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="9dc1b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dc1b-110">EXAMPLES</span></span>

### <span data-ttu-id="9dc1b-111">Пример 1: получение всех действий, выполняемых для конвейерного выполнения</span><span class="sxs-lookup"><span data-stu-id="9dc1b-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="9dc1b-112">Эта команда получает подробные сведения обо всех действиях, выполняемых в конвейере с ИДЕНТИФИКАТОРом "f288712d-fb08-4cb8-96ef-82d3b9b30621", которое произошло между "2017-09-01" и "2017-09-30".</span><span class="sxs-lookup"><span data-stu-id="9dc1b-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="9dc1b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dc1b-113">PARAMETERS</span></span>

### <span data-ttu-id="9dc1b-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="9dc1b-114">-ActivityName</span></span>
<span data-ttu-id="9dc1b-115">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-115">The name of the activity.</span></span>

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

### <span data-ttu-id="9dc1b-116">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-116">-DataFactory</span></span>
<span data-ttu-id="9dc1b-117">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-117">The data factory object.</span></span>

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

### <span data-ttu-id="9dc1b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9dc1b-118">-DataFactoryName</span></span>
<span data-ttu-id="9dc1b-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-119">The data factory name.</span></span>

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

### <span data-ttu-id="9dc1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc1b-120">-DefaultProfile</span></span>
<span data-ttu-id="9dc1b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc1b-122">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="9dc1b-122">-LinkedServiceName</span></span>
<span data-ttu-id="9dc1b-123">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-123">The linked service name.</span></span>

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

### <span data-ttu-id="9dc1b-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="9dc1b-124">-PipelineRunId</span></span>
<span data-ttu-id="9dc1b-125">КОД запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="9dc1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9dc1b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-127">The resource group name.</span></span>

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

### <span data-ttu-id="9dc1b-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="9dc1b-128">-RunStartedAfter</span></span>
<span data-ttu-id="9dc1b-129">Время, по истечении которого началось выполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-129">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="9dc1b-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="9dc1b-130">-RunStartedBefore</span></span>
<span data-ttu-id="9dc1b-131">Время, до которого началось выполнение конвейера.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-131">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="9dc1b-132">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="9dc1b-132">-Status</span></span>
<span data-ttu-id="9dc1b-133">Состояние выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-133">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="9dc1b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc1b-134">CommonParameters</span></span>
<span data-ttu-id="9dc1b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dc1b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc1b-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dc1b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc1b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dc1b-137">INPUTS</span></span>

### <span data-ttu-id="9dc1b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9dc1b-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9dc1b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc1b-139">System.String</span></span>

## <span data-ttu-id="9dc1b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc1b-140">OUTPUTS</span></span>

### <span data-ttu-id="9dc1b-141">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9dc1b-141">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9dc1b-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="9dc1b-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="9dc1b-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dc1b-143">NOTES</span></span>

## <span data-ttu-id="9dc1b-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dc1b-144">RELATED LINKS</span></span>

[<span data-ttu-id="9dc1b-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="9dc1b-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="9dc1b-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="9dc1b-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

