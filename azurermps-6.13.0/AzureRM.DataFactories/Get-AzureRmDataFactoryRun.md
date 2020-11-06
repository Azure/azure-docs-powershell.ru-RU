---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: 77ca77322cec186878b327bcafa9fce626a99c02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564628"
---
# <span data-ttu-id="f0952-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="f0952-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="f0952-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0952-102">SYNOPSIS</span></span>
<span data-ttu-id="f0952-103">Вызывается для среза данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f0952-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0952-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0952-104">SYNTAX</span></span>

### <span data-ttu-id="f0952-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0952-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0952-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f0952-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0952-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0952-107">DESCRIPTION</span></span>
<span data-ttu-id="f0952-108">Командлет **Get-AzureRmDataFactoryRun** возвращает выполнение для среза данных набора данных в службе фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f0952-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="f0952-109">Набор данных в фабрике данных состоит из фрагментов на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="f0952-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="f0952-110">Ширина среза определяется расписанием (ежечасно или ежедневно).</span><span class="sxs-lookup"><span data-stu-id="f0952-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="f0952-111">Выполнение — это блок обработки для среза.</span><span class="sxs-lookup"><span data-stu-id="f0952-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="f0952-112">Для среза может быть один или несколько запусков в случае повторных попыток или на случай, если вы перезапустите срез из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="f0952-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="f0952-113">Срез определяется по времени начала.</span><span class="sxs-lookup"><span data-stu-id="f0952-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="f0952-114">Чтобы получить время начала среза, используйте командлет Get-AzureRmDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="f0952-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="f0952-115">Например, чтобы получить доступ к следующему фрагменту, используйте время запуска 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="f0952-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="f0952-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM End: 5/3/2014 8:00:00 PM RetryCount: 0 состояние: готовый LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="f0952-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="f0952-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0952-117">EXAMPLES</span></span>

### <span data-ttu-id="f0952-118">Пример 1: получение набора данных</span><span class="sxs-lookup"><span data-stu-id="f0952-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="f0952-119">Эта команда возвращает "все" для фрагментов набора данных с именем DAWikiAggregatedData в фабрике данных с именем WikiADF, которая начинается с 4 PM GMT на 05/21/2014.</span><span class="sxs-lookup"><span data-stu-id="f0952-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="f0952-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0952-120">PARAMETERS</span></span>

### <span data-ttu-id="f0952-121">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="f0952-121">-DataFactory</span></span>
<span data-ttu-id="f0952-122">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f0952-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f0952-123">Этот командлет запускается для фрагментов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f0952-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0952-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f0952-124">-DataFactoryName</span></span>
<span data-ttu-id="f0952-125">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f0952-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f0952-126">Этот командлет запускается для фрагментов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f0952-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0952-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="f0952-127">-DatasetName</span></span>
<span data-ttu-id="f0952-128">Указывает имя набора данных.</span><span class="sxs-lookup"><span data-stu-id="f0952-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="f0952-129">Этот командлет запускается для фрагментов, относящихся к набору данных, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f0952-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0952-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0952-130">-DefaultProfile</span></span>
<span data-ttu-id="f0952-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f0952-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0952-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0952-132">-ResourceGroupName</span></span>
<span data-ttu-id="f0952-133">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f0952-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f0952-134">Этот командлет получает заводские запуски для фрагментов, принадлежащих к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f0952-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f0952-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="f0952-135">-StartDateTime</span></span>
<span data-ttu-id="f0952-136">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="f0952-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="f0952-137">Этот командлет запускается для срезов данных, которые соответствуют этому периоду времени.</span><span class="sxs-lookup"><span data-stu-id="f0952-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="f0952-138">*StartDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах: 2015-01-01Z 2015-01-01T00:00:00Z, 00:01T00, 1 — 01:00-01-00.000:00 — 8-08:00 (Тихоокеанское время). обозначение часового пояса по умолчанию — UTC.</span><span class="sxs-lookup"><span data-stu-id="f0952-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="f0952-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0952-139">CommonParameters</span></span>
<span data-ttu-id="f0952-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0952-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0952-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0952-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0952-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0952-142">INPUTS</span></span>

### <span data-ttu-id="f0952-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f0952-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f0952-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f0952-144">System.String</span></span>

## <span data-ttu-id="f0952-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0952-145">OUTPUTS</span></span>

### <span data-ttu-id="f0952-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="f0952-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="f0952-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0952-147">NOTES</span></span>
* <span data-ttu-id="f0952-148">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="f0952-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f0952-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0952-149">RELATED LINKS</span></span>

[<span data-ttu-id="f0952-150">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="f0952-150">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


