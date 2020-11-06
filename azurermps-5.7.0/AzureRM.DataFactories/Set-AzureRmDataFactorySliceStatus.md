---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559103"
---
# <span data-ttu-id="d450c-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="d450c-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="d450c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d450c-102">SYNOPSIS</span></span>
<span data-ttu-id="d450c-103">Задает состояние срезов для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d450c-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d450c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d450c-104">SYNTAX</span></span>

### <span data-ttu-id="d450c-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d450c-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d450c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d450c-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d450c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d450c-107">DESCRIPTION</span></span>
<span data-ttu-id="d450c-108">Командлет **Set-AzureRmDataFactorySliceStatus** задает состояние срезов для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="d450c-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="d450c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d450c-109">EXAMPLES</span></span>

### <span data-ttu-id="d450c-110">Пример 1: Настройка состояния всех срезов</span><span class="sxs-lookup"><span data-stu-id="d450c-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="d450c-111">Эта команда задает состояние всех срезов для набора данных с именем DAWikiAggregatedData на ожидание в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d450c-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="d450c-112">Параметр *UpdateType* имеет значение UpstreamInPipeline, поэтому команда задает состояние каждого сектора для набора данных и всех зависимых наборов.</span><span class="sxs-lookup"><span data-stu-id="d450c-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="d450c-113">Зависимые наборы данных используются как входные наборы данных для действий в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d450c-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="d450c-114">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="d450c-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="d450c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d450c-115">PARAMETERS</span></span>

### <span data-ttu-id="d450c-116">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="d450c-116">-DataFactory</span></span>
<span data-ttu-id="d450c-117">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d450c-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d450c-118">Этот командлет изменяет состояние срезов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d450c-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d450c-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d450c-119">-DataFactoryName</span></span>
<span data-ttu-id="d450c-120">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d450c-121">Этот командлет изменяет состояние срезов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d450c-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d450c-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d450c-122">-DatasetName</span></span>
<span data-ttu-id="d450c-123">Указывает имя набора данных, для которого этот командлет изменяет фрагменты.</span><span class="sxs-lookup"><span data-stu-id="d450c-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d450c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d450c-124">-DefaultProfile</span></span>
<span data-ttu-id="d450c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d450c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d450c-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="d450c-126">-EndDateTime</span></span>
<span data-ttu-id="d450c-127">Указывает конец периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d450c-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d450c-128">Это время является концом среза данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="d450c-129">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d450c-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="d450c-130">*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="d450c-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="d450c-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское стандартное время)</span><span class="sxs-lookup"><span data-stu-id="d450c-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="d450c-132">Обозначение часового пояса по умолчанию — UTC.</span><span class="sxs-lookup"><span data-stu-id="d450c-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d450c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d450c-133">-ResourceGroupName</span></span>
<span data-ttu-id="d450c-134">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d450c-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d450c-135">Этот командлет изменяет состояние срезов, относящихся к группе, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d450c-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d450c-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d450c-136">-StartDateTime</span></span>
<span data-ttu-id="d450c-137">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d450c-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d450c-138">Это время является началом среза данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-138">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="d450c-139">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="d450c-139">-Status</span></span>
<span data-ttu-id="d450c-140">Задает состояние, назначаемое срезу данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="d450c-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d450c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d450c-142">Ожида.</span><span class="sxs-lookup"><span data-stu-id="d450c-142">Waiting.</span></span>
<span data-ttu-id="d450c-143">Срез данных ожидает проверки политик проверки перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="d450c-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="d450c-144">Начать.</span><span class="sxs-lookup"><span data-stu-id="d450c-144">Ready.</span></span>
<span data-ttu-id="d450c-145">Обработка данных завершена, и срез данных готов.</span><span class="sxs-lookup"><span data-stu-id="d450c-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="d450c-146">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="d450c-146">InProgress.</span></span>
<span data-ttu-id="d450c-147">Выполняется обработка данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="d450c-148">Ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d450c-148">Failed.</span></span>
<span data-ttu-id="d450c-149">Обработка данных завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="d450c-149">Data processing failed.</span></span>
- <span data-ttu-id="d450c-150">Пропущена.</span><span class="sxs-lookup"><span data-stu-id="d450c-150">Skipped.</span></span>
<span data-ttu-id="d450c-151">Пропущена обработка среза данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d450c-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="d450c-152">-UpdateType</span></span>
<span data-ttu-id="d450c-153">Указывает тип обновления для среза.</span><span class="sxs-lookup"><span data-stu-id="d450c-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="d450c-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d450c-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d450c-155">Конкрет.</span><span class="sxs-lookup"><span data-stu-id="d450c-155">Individual.</span></span>
<span data-ttu-id="d450c-156">Задает состояние каждого среза для набора данных в указанном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="d450c-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="d450c-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="d450c-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="d450c-158">Задает состояние каждого среза для набора данных и все зависимые наборы, которые используются в качестве входных множества для действий в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d450c-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d450c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d450c-159">CommonParameters</span></span>
<span data-ttu-id="d450c-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d450c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d450c-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d450c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d450c-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d450c-162">INPUTS</span></span>

### <span data-ttu-id="d450c-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="d450c-163">None</span></span>
<span data-ttu-id="d450c-164">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d450c-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d450c-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d450c-165">OUTPUTS</span></span>

### <span data-ttu-id="d450c-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d450c-166">System.Boolean</span></span>

## <span data-ttu-id="d450c-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="d450c-167">NOTES</span></span>
* <span data-ttu-id="d450c-168">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="d450c-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d450c-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d450c-169">RELATED LINKS</span></span>

[<span data-ttu-id="d450c-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="d450c-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


