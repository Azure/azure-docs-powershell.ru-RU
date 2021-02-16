---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242808"
---
# <span data-ttu-id="f41c1-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f41c1-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="f41c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f41c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f41c1-103">Создает набор данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="f41c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f41c1-104">SYNTAX</span></span>

### <span data-ttu-id="f41c1-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f41c1-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f41c1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f41c1-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f41c1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f41c1-107">DESCRIPTION</span></span>
<span data-ttu-id="f41c1-108">Для создания нового наборов данных в фабрике данных Azure создается набор данных **New-AzDataFactoryDataset.**</span><span class="sxs-lookup"><span data-stu-id="f41c1-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="f41c1-109">Если указать имя для уже существующий набор данных, этот набор данных запросит подтверждение перед заменой.</span><span class="sxs-lookup"><span data-stu-id="f41c1-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="f41c1-110">При указании *параметра Force* существующий набор данных будет замещается этим набором данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f41c1-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="f41c1-111">Выполните эти действия в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="f41c1-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="f41c1-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-112">Create a data factory.</span></span> 
- <span data-ttu-id="f41c1-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="f41c1-113">Create linked services.</span></span> 
- <span data-ttu-id="f41c1-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-114">Create datasets.</span></span> 
- <span data-ttu-id="f41c1-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="f41c1-115">Create a pipeline.</span></span>
<span data-ttu-id="f41c1-116">Если в фабрике данных уже существует набор данных с таким же именем, этот набор будет предложено подтвердить, следует ли перезаписать существующий набор данных с помощью нового.</span><span class="sxs-lookup"><span data-stu-id="f41c1-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="f41c1-117">Если вы подтверждаете, что существующий набор данных переопишется, его определение также заменяется.</span><span class="sxs-lookup"><span data-stu-id="f41c1-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="f41c1-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f41c1-118">EXAMPLES</span></span>

### <span data-ttu-id="f41c1-119">Пример 1. Создание наборов данных</span><span class="sxs-lookup"><span data-stu-id="f41c1-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="f41c1-120">Эта команда создает набор данных с именем DA_WikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f41c1-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="f41c1-121">Набор данных будет базой данных на данных из DAWikipediaClickEvents.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="f41c1-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="f41c1-122">Пример 2. Просмотр доступности для нового наборов данных</span><span class="sxs-lookup"><span data-stu-id="f41c1-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="f41c1-123">Первая команда создает набор данных с именем DA_WikipediaClickEvents, как в предыдущем примере, а затем назначает его переменной $Dataset данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="f41c1-124">Вторая команда использует стандартную точку для отображения сведений о свойстве Availability в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="f41c1-125">Пример 3. Просмотр расположения для нового наборов данных</span><span class="sxs-lookup"><span data-stu-id="f41c1-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="f41c1-126">Первая команда создает набор данных с именем DA_WikipediaClickEvents, как в предыдущем примере, а затем назначает его переменной $Dataset данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="f41c1-127">Вторая команда отображает сведения о свойстве Location для наборов данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="f41c1-128">Пример 4. Просмотр правил проверки для нового набора данных</span><span class="sxs-lookup"><span data-stu-id="f41c1-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="f41c1-129">Первая команда создает набор данных с именем DA_WikipediaClickEvents, как в предыдущем примере, а затем назначает его переменной $Dataset данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="f41c1-130">Вторая команда получает подробные сведения о правилах проверки для наборов данных и передает их в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f41c1-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f41c1-131">Это Windows PowerShell форматирование результатов.</span><span class="sxs-lookup"><span data-stu-id="f41c1-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="f41c1-132">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f41c1-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="f41c1-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f41c1-133">PARAMETERS</span></span>

### <span data-ttu-id="f41c1-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f41c1-134">-DataFactory</span></span>
<span data-ttu-id="f41c1-135">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f41c1-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f41c1-136">Этот cmdlet создает набор данных в фабрике данных, заданном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f41c1-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f41c1-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f41c1-137">-DataFactoryName</span></span>
<span data-ttu-id="f41c1-138">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f41c1-139">Этот cmdlet создает набор данных в фабрике данных, заданном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f41c1-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f41c1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41c1-140">-DefaultProfile</span></span>
<span data-ttu-id="f41c1-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f41c1-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f41c1-142">-File</span><span class="sxs-lookup"><span data-stu-id="f41c1-142">-File</span></span>
<span data-ttu-id="f41c1-143">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41c1-144">-Force</span><span class="sxs-lookup"><span data-stu-id="f41c1-144">-Force</span></span>
<span data-ttu-id="f41c1-145">Указывает на то, что этот cmdlet заменяет существующий набор данных, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f41c1-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41c1-146">-Name</span><span class="sxs-lookup"><span data-stu-id="f41c1-146">-Name</span></span>
<span data-ttu-id="f41c1-147">Указывает имя созда создаемого наборов данных.</span><span class="sxs-lookup"><span data-stu-id="f41c1-147">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f41c1-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41c1-148">-ResourceGroupName</span></span>
<span data-ttu-id="f41c1-149">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f41c1-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f41c1-150">Этот cmdlet создает набор данных в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f41c1-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f41c1-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f41c1-151">-Confirm</span></span>
<span data-ttu-id="f41c1-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f41c1-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41c1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f41c1-153">-WhatIf</span></span>
<span data-ttu-id="f41c1-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f41c1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f41c1-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f41c1-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41c1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41c1-156">CommonParameters</span></span>
<span data-ttu-id="f41c1-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f41c1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41c1-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f41c1-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41c1-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f41c1-159">INPUTS</span></span>

### <span data-ttu-id="f41c1-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f41c1-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f41c1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="f41c1-161">System.String</span></span>

## <span data-ttu-id="f41c1-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f41c1-162">OUTPUTS</span></span>

### <span data-ttu-id="f41c1-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="f41c1-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="f41c1-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f41c1-164">NOTES</span></span>
* <span data-ttu-id="f41c1-165">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="f41c1-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f41c1-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f41c1-166">RELATED LINKS</span></span>

[<span data-ttu-id="f41c1-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f41c1-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="f41c1-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f41c1-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


