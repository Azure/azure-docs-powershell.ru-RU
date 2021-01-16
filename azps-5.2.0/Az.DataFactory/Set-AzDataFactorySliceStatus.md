---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412095"
---
# <span data-ttu-id="cb48f-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="cb48f-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="cb48f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb48f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb48f-103">Задает состояние срезов для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="cb48f-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="cb48f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb48f-104">SYNTAX</span></span>

### <span data-ttu-id="cb48f-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb48f-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb48f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cb48f-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb48f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb48f-107">DESCRIPTION</span></span>
<span data-ttu-id="cb48f-108">**Cmdlet Set-AzDataFactorySliceStatus** задает состояние срезов для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="cb48f-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="cb48f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb48f-109">EXAMPLES</span></span>

### <span data-ttu-id="cb48f-110">Пример 1. Настройка состояния всех срезов</span><span class="sxs-lookup"><span data-stu-id="cb48f-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="cb48f-111">Эта команда задает состояние всех срезов для набора данных DAWikiAggregatedData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cb48f-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="cb48f-112">Параметр *UpdateType* имеет значение UpstreamInPipeline, поэтому команда задает состояние каждого набора данных и всех зависимых наборов данных.</span><span class="sxs-lookup"><span data-stu-id="cb48f-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="cb48f-113">Зависимые наборы данных используются в качестве наборов входных данных для действий в конвейере.</span><span class="sxs-lookup"><span data-stu-id="cb48f-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="cb48f-114">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="cb48f-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="cb48f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb48f-115">PARAMETERS</span></span>

### <span data-ttu-id="cb48f-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb48f-116">-DataFactory</span></span>
<span data-ttu-id="cb48f-117">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="cb48f-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cb48f-118">Этот cmdlet изменяет состояние срезов, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cb48f-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb48f-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cb48f-119">-DataFactoryName</span></span>
<span data-ttu-id="cb48f-120">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="cb48f-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cb48f-121">Этот cmdlet изменяет состояние срезов, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cb48f-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb48f-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="cb48f-122">-DatasetName</span></span>
<span data-ttu-id="cb48f-123">Указывает имя набора данных, для которого этот cmdlet изменяет срезы.</span><span class="sxs-lookup"><span data-stu-id="cb48f-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="cb48f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb48f-124">-DefaultProfile</span></span>
<span data-ttu-id="cb48f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cb48f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb48f-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="cb48f-126">-EndDateTime</span></span>
<span data-ttu-id="cb48f-127">Окончание периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="cb48f-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="cb48f-128">На этот раз завершится анализ среза данных.</span><span class="sxs-lookup"><span data-stu-id="cb48f-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="cb48f-129">Чтобы получить дополнительные сведения об **объектах даты и времени,** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cb48f-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="cb48f-130">В формате ISO8601 необходимо указать *endDateTime,* как в следующих примерах: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское время) По умолчанию часовой пояс имеет значение UTC.</span><span class="sxs-lookup"><span data-stu-id="cb48f-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="cb48f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb48f-131">-ResourceGroupName</span></span>
<span data-ttu-id="cb48f-132">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="cb48f-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cb48f-133">Этот cmdlet изменяет состояние срезов, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cb48f-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb48f-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="cb48f-134">-StartDateTime</span></span>
<span data-ttu-id="cb48f-135">Начало периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="cb48f-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="cb48f-136">Это время — начало среза данных.</span><span class="sxs-lookup"><span data-stu-id="cb48f-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="cb48f-137">-Status</span><span class="sxs-lookup"><span data-stu-id="cb48f-137">-Status</span></span>
<span data-ttu-id="cb48f-138">Указывает состояние, назначаемого срезу данных.</span><span class="sxs-lookup"><span data-stu-id="cb48f-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="cb48f-139">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="cb48f-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb48f-140">"Ожидание".</span><span class="sxs-lookup"><span data-stu-id="cb48f-140">Waiting.</span></span>
<span data-ttu-id="cb48f-141">Перед обработкой среза данных ожидается проверка политик проверки.</span><span class="sxs-lookup"><span data-stu-id="cb48f-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="cb48f-142">"Готово".</span><span class="sxs-lookup"><span data-stu-id="cb48f-142">Ready.</span></span>
<span data-ttu-id="cb48f-143">Обработка данных завершена, и набор данных готов.</span><span class="sxs-lookup"><span data-stu-id="cb48f-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="cb48f-144">InProgress.</span><span class="sxs-lookup"><span data-stu-id="cb48f-144">InProgress.</span></span>
<span data-ttu-id="cb48f-145">Обработка данных продолжается.</span><span class="sxs-lookup"><span data-stu-id="cb48f-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="cb48f-146">Не удалось.</span><span class="sxs-lookup"><span data-stu-id="cb48f-146">Failed.</span></span>
<span data-ttu-id="cb48f-147">При обработке данных не удалось.</span><span class="sxs-lookup"><span data-stu-id="cb48f-147">Data processing failed.</span></span>
- <span data-ttu-id="cb48f-148">Пропущено.</span><span class="sxs-lookup"><span data-stu-id="cb48f-148">Skipped.</span></span>
<span data-ttu-id="cb48f-149">Пропущена обработка среза данных.</span><span class="sxs-lookup"><span data-stu-id="cb48f-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="cb48f-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="cb48f-150">-UpdateType</span></span>
<span data-ttu-id="cb48f-151">Определяет тип обновления для среза.</span><span class="sxs-lookup"><span data-stu-id="cb48f-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="cb48f-152">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="cb48f-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb48f-153">Индивидуальный.</span><span class="sxs-lookup"><span data-stu-id="cb48f-153">Individual.</span></span>
<span data-ttu-id="cb48f-154">Задает состояние каждого среза для набора данных в указанном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="cb48f-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="cb48f-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="cb48f-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="cb48f-156">Задает состояние каждого набора данных и всех зависимых наборов данных, которые используются в качестве наборов входных данных для действий в конвейере.</span><span class="sxs-lookup"><span data-stu-id="cb48f-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="cb48f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb48f-157">CommonParameters</span></span>
<span data-ttu-id="cb48f-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb48f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb48f-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb48f-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb48f-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb48f-160">INPUTS</span></span>

### <span data-ttu-id="cb48f-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cb48f-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cb48f-162">System.String</span><span class="sxs-lookup"><span data-stu-id="cb48f-162">System.String</span></span>

## <span data-ttu-id="cb48f-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb48f-163">OUTPUTS</span></span>

### <span data-ttu-id="cb48f-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb48f-164">System.Boolean</span></span>

## <span data-ttu-id="cb48f-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb48f-165">NOTES</span></span>
* <span data-ttu-id="cb48f-166">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="cb48f-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb48f-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb48f-167">RELATED LINKS</span></span>

[<span data-ttu-id="cb48f-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="cb48f-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


