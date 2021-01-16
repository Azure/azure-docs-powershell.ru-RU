---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: f04f2d2d96dd0b293850ca3150568eb015ab5bbb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407463"
---
# <span data-ttu-id="4f137-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="4f137-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="4f137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f137-102">SYNOPSIS</span></span>
<span data-ttu-id="4f137-103">Выполняется для среза данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4f137-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="4f137-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f137-104">SYNTAX</span></span>

### <span data-ttu-id="4f137-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f137-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f137-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4f137-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f137-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f137-107">DESCRIPTION</span></span>
<span data-ttu-id="4f137-108">Для среза данных в фабрике данных Azure выполняется cmdlet **Get-AzDataFactoryRun.**</span><span class="sxs-lookup"><span data-stu-id="4f137-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4f137-109">Набор данных в фабрике данных состоит из срезов по оси времени.</span><span class="sxs-lookup"><span data-stu-id="4f137-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="4f137-110">Ширина среза определяется расписанием (почасовой или ежедневной).</span><span class="sxs-lookup"><span data-stu-id="4f137-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="4f137-111">Запуск — это единица обработки для среза.</span><span class="sxs-lookup"><span data-stu-id="4f137-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="4f137-112">Один или несколько запусков для среза могут быть на случай искомого фрагмента или повторного его запуска из-за сбоев.</span><span class="sxs-lookup"><span data-stu-id="4f137-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="4f137-113">Время начала для среза.</span><span class="sxs-lookup"><span data-stu-id="4f137-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="4f137-114">Чтобы получить время начала среза, воспользуйтесь Get-AzDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="4f137-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="4f137-115">Например, чтобы получить запуск для следующего среза, используйте время начала 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="4f137-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="4f137-116">ResourceGroupName : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingSetaignEffectivenessBlobDataset Start : 02.05.2014 8:00:00 End : 05.03.2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span><span class="sxs-lookup"><span data-stu-id="4f137-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="4f137-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f137-117">EXAMPLES</span></span>

### <span data-ttu-id="4f137-118">Пример 1. Получить набор данных</span><span class="sxs-lookup"><span data-stu-id="4f137-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="4f137-119">Эта команда выполняет все запускы для срезов с именем DAWikiAggregatedData в фабрике данных WikiADF, которые начинаются с 16:00 GMT 21.05.2014.</span><span class="sxs-lookup"><span data-stu-id="4f137-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="4f137-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f137-120">PARAMETERS</span></span>

### <span data-ttu-id="4f137-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f137-121">-DataFactory</span></span>
<span data-ttu-id="4f137-122">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="4f137-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4f137-123">Этот cmdlet выполняется для срезов, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4f137-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f137-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f137-124">-DataFactoryName</span></span>
<span data-ttu-id="4f137-125">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4f137-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4f137-126">Этот cmdlet выполняется для срезов, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4f137-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f137-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="4f137-127">-DatasetName</span></span>
<span data-ttu-id="4f137-128">Указывает имя наборов данных.</span><span class="sxs-lookup"><span data-stu-id="4f137-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="4f137-129">Этот cmdlet выполняется для срезов, которые относятся к набору данных, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4f137-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f137-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f137-130">-DefaultProfile</span></span>
<span data-ttu-id="4f137-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4f137-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f137-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f137-132">-ResourceGroupName</span></span>
<span data-ttu-id="4f137-133">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4f137-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4f137-134">Этот cmdlet возвращает заводские запуски для срезов, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4f137-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f137-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="4f137-135">-StartDateTime</span></span>
<span data-ttu-id="4f137-136">Начало периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="4f137-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="4f137-137">Этот командлет выполняется для срезов данных, которые соответствуют данному периоду времени.</span><span class="sxs-lookup"><span data-stu-id="4f137-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="4f137-138">*Формат STARTDateTime* должен быть указан в формате ISO8601, как в следующих примерах: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское время) Часовой пояс по умолчанию — UTC.</span><span class="sxs-lookup"><span data-stu-id="4f137-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="4f137-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f137-139">CommonParameters</span></span>
<span data-ttu-id="4f137-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f137-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f137-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f137-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f137-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f137-142">INPUTS</span></span>

### <span data-ttu-id="4f137-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4f137-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4f137-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4f137-144">System.String</span></span>

## <span data-ttu-id="4f137-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f137-145">OUTPUTS</span></span>

### <span data-ttu-id="4f137-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="4f137-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="4f137-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f137-147">NOTES</span></span>
* <span data-ttu-id="4f137-148">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="4f137-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4f137-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f137-149">RELATED LINKS</span></span>

[<span data-ttu-id="4f137-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="4f137-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


