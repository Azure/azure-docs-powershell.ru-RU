---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912800"
---
# <span data-ttu-id="eafe1-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="eafe1-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="eafe1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eafe1-102">SYNOPSIS</span></span>
<span data-ttu-id="eafe1-103">Задает состояние срезов для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="eafe1-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="eafe1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eafe1-104">SYNTAX</span></span>

### <span data-ttu-id="eafe1-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eafe1-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eafe1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eafe1-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eafe1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafe1-107">DESCRIPTION</span></span>
<span data-ttu-id="eafe1-108">Командлет **Set-AzDataFactorySliceStatus** задает состояние срезов для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="eafe1-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="eafe1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eafe1-109">EXAMPLES</span></span>

### <span data-ttu-id="eafe1-110">Пример 1: Настройка состояния всех срезов</span><span class="sxs-lookup"><span data-stu-id="eafe1-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="eafe1-111">Эта команда задает состояние всех срезов для набора данных с именем DAWikiAggregatedData на ожидание в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="eafe1-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="eafe1-112">Параметр *UpdateType* имеет значение UpstreamInPipeline, поэтому команда задает состояние каждого сектора для набора данных и всех зависимых наборов.</span><span class="sxs-lookup"><span data-stu-id="eafe1-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="eafe1-113">Зависимые наборы данных используются как входные наборы данных для действий в конвейере.</span><span class="sxs-lookup"><span data-stu-id="eafe1-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="eafe1-114">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="eafe1-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="eafe1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eafe1-115">PARAMETERS</span></span>

### <span data-ttu-id="eafe1-116">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="eafe1-116">-DataFactory</span></span>
<span data-ttu-id="eafe1-117">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="eafe1-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="eafe1-118">Этот командлет изменяет состояние срезов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eafe1-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eafe1-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="eafe1-119">-DataFactoryName</span></span>
<span data-ttu-id="eafe1-120">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="eafe1-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="eafe1-121">Этот командлет изменяет состояние срезов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eafe1-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eafe1-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="eafe1-122">-DatasetName</span></span>
<span data-ttu-id="eafe1-123">Указывает имя набора данных, для которого этот командлет изменяет фрагменты.</span><span class="sxs-lookup"><span data-stu-id="eafe1-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="eafe1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafe1-124">-DefaultProfile</span></span>
<span data-ttu-id="eafe1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eafe1-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eafe1-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="eafe1-126">-EndDateTime</span></span>
<span data-ttu-id="eafe1-127">Указывает конец периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="eafe1-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="eafe1-128">Это время является концом среза данных.</span><span class="sxs-lookup"><span data-stu-id="eafe1-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="eafe1-129">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="eafe1-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="eafe1-130">*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах: 2015-01-01Z 2015-01-01T00:00-1-01:00Z 1:00:01T00 z (UTC) 2015-0,01-: 00.00 – 8 – 00.000</span><span class="sxs-lookup"><span data-stu-id="eafe1-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafe1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eafe1-131">-ResourceGroupName</span></span>
<span data-ttu-id="eafe1-132">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="eafe1-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eafe1-133">Этот командлет изменяет состояние срезов, относящихся к группе, в которой указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eafe1-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eafe1-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="eafe1-134">-StartDateTime</span></span>
<span data-ttu-id="eafe1-135">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="eafe1-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="eafe1-136">Это время является началом среза данных.</span><span class="sxs-lookup"><span data-stu-id="eafe1-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="eafe1-137">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="eafe1-137">-Status</span></span>
<span data-ttu-id="eafe1-138">Задает состояние, назначаемое срезу данных.</span><span class="sxs-lookup"><span data-stu-id="eafe1-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="eafe1-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eafe1-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eafe1-140">Ожида.</span><span class="sxs-lookup"><span data-stu-id="eafe1-140">Waiting.</span></span>
<span data-ttu-id="eafe1-141">Срез данных ожидает проверки политик проверки перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="eafe1-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="eafe1-142">Начать.</span><span class="sxs-lookup"><span data-stu-id="eafe1-142">Ready.</span></span>
<span data-ttu-id="eafe1-143">Обработка данных завершена, и срез данных готов.</span><span class="sxs-lookup"><span data-stu-id="eafe1-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="eafe1-144">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="eafe1-144">InProgress.</span></span>
<span data-ttu-id="eafe1-145">Выполняется обработка данных.</span><span class="sxs-lookup"><span data-stu-id="eafe1-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="eafe1-146">Ошибкой.</span><span class="sxs-lookup"><span data-stu-id="eafe1-146">Failed.</span></span>
<span data-ttu-id="eafe1-147">Обработка данных завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="eafe1-147">Data processing failed.</span></span>
- <span data-ttu-id="eafe1-148">Пропущена.</span><span class="sxs-lookup"><span data-stu-id="eafe1-148">Skipped.</span></span>
<span data-ttu-id="eafe1-149">Пропущена обработка среза данных.</span><span class="sxs-lookup"><span data-stu-id="eafe1-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafe1-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="eafe1-150">-UpdateType</span></span>
<span data-ttu-id="eafe1-151">Указывает тип обновления для среза.</span><span class="sxs-lookup"><span data-stu-id="eafe1-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="eafe1-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eafe1-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eafe1-153">Конкрет.</span><span class="sxs-lookup"><span data-stu-id="eafe1-153">Individual.</span></span>
<span data-ttu-id="eafe1-154">Задает состояние каждого среза для набора данных в указанном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="eafe1-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="eafe1-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="eafe1-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="eafe1-156">Задает состояние каждого среза для набора данных и все зависимые наборы, которые используются в качестве входных множества для действий в конвейере.</span><span class="sxs-lookup"><span data-stu-id="eafe1-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafe1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafe1-157">CommonParameters</span></span>
<span data-ttu-id="eafe1-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eafe1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafe1-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafe1-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafe1-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eafe1-160">INPUTS</span></span>

### <span data-ttu-id="eafe1-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eafe1-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="eafe1-162">System. String</span><span class="sxs-lookup"><span data-stu-id="eafe1-162">System.String</span></span>

## <span data-ttu-id="eafe1-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafe1-163">OUTPUTS</span></span>

### <span data-ttu-id="eafe1-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eafe1-164">System.Boolean</span></span>

## <span data-ttu-id="eafe1-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="eafe1-165">NOTES</span></span>
* <span data-ttu-id="eafe1-166">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="eafe1-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eafe1-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eafe1-167">RELATED LINKS</span></span>

[<span data-ttu-id="eafe1-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="eafe1-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


