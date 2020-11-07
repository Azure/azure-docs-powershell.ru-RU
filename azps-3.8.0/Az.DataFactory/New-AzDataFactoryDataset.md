---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912845"
---
# <span data-ttu-id="16910-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="16910-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="16910-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16910-102">SYNOPSIS</span></span>
<span data-ttu-id="16910-103">Создает набор данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="16910-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="16910-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16910-104">SYNTAX</span></span>

### <span data-ttu-id="16910-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16910-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16910-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16910-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16910-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16910-107">DESCRIPTION</span></span>
<span data-ttu-id="16910-108">Командлет **New-AzDataFactoryDataset** создает набор данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="16910-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="16910-109">Если вы задаете имя уже существующего набора данных, этот командлет запрашивает подтверждение перед заменой набора данных.</span><span class="sxs-lookup"><span data-stu-id="16910-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="16910-110">Если указан параметр *Force* , командлет заменяет существующий набор данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="16910-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="16910-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="16910-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="16910-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="16910-112">Create a data factory.</span></span> 
- <span data-ttu-id="16910-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="16910-113">Create linked services.</span></span> 
- <span data-ttu-id="16910-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="16910-114">Create datasets.</span></span> 
- <span data-ttu-id="16910-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="16910-115">Create a pipeline.</span></span>
<span data-ttu-id="16910-116">Если набор данных с таким же именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписать существующий набор данных новым.</span><span class="sxs-lookup"><span data-stu-id="16910-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="16910-117">Если вы подтвердите переписать существующий набор данных, определение набора данных также заменяется.</span><span class="sxs-lookup"><span data-stu-id="16910-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="16910-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16910-118">EXAMPLES</span></span>

### <span data-ttu-id="16910-119">Пример 1: создание набора данных</span><span class="sxs-lookup"><span data-stu-id="16910-119">Example 1: Create a dataset</span></span>
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

<span data-ttu-id="16910-120">Эта команда создает набор данных с именем DA_WikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="16910-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="16910-121">В команде набор данных заосновывается на сведениях в DAWikipediaClickEvents.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="16910-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="16910-122">Пример 2: Просмотр сведений о доступности для нового набора данных</span><span class="sxs-lookup"><span data-stu-id="16910-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="16910-123">Первая команда создает набор данных с именем DA_WikipediaClickEvents, как в предыдущем примере, а затем присваивает этот набор данных переменной $Dataset.</span><span class="sxs-lookup"><span data-stu-id="16910-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="16910-124">Во второй команде используется стандартная точечная нотация для отображения подробных сведений о свойстве доступности набора данных.</span><span class="sxs-lookup"><span data-stu-id="16910-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="16910-125">Пример 3: Просмотр расположения для нового набора данных</span><span class="sxs-lookup"><span data-stu-id="16910-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="16910-126">Первая команда создает набор данных с именем DA_WikipediaClickEvents, как в предыдущем примере, а затем присваивает этот набор данных переменной $Dataset.</span><span class="sxs-lookup"><span data-stu-id="16910-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="16910-127">Вторая команда отображает сведения о свойстве Location набора данных.</span><span class="sxs-lookup"><span data-stu-id="16910-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="16910-128">Пример 4: Просмотр правил проверки для нового набора данных</span><span class="sxs-lookup"><span data-stu-id="16910-128">Example 4: View validation rules for a new dataset</span></span>
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

<span data-ttu-id="16910-129">Первая команда создает набор данных с именем DA_WikipediaClickEvents, как в предыдущем примере, а затем присваивает этот набор данных переменной $Dataset.</span><span class="sxs-lookup"><span data-stu-id="16910-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="16910-130">Вторая команда получает сведения о правилах проверки для набора данных, а затем передает их в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="16910-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="16910-131">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="16910-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="16910-132">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="16910-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="16910-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16910-133">PARAMETERS</span></span>

### <span data-ttu-id="16910-134">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="16910-134">-DataFactory</span></span>
<span data-ttu-id="16910-135">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="16910-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="16910-136">Этот командлет создает набор данных в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16910-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="16910-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16910-137">-DataFactoryName</span></span>
<span data-ttu-id="16910-138">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="16910-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="16910-139">Этот командлет создает набор данных в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16910-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="16910-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16910-140">-DefaultProfile</span></span>
<span data-ttu-id="16910-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16910-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16910-142">-Файл</span><span class="sxs-lookup"><span data-stu-id="16910-142">-File</span></span>
<span data-ttu-id="16910-143">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание набора данных.</span><span class="sxs-lookup"><span data-stu-id="16910-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

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

### <span data-ttu-id="16910-144">-Force</span><span class="sxs-lookup"><span data-stu-id="16910-144">-Force</span></span>
<span data-ttu-id="16910-145">Указывает на то, что этот командлет заменяет существующий набор данных без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="16910-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="16910-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16910-146">-Name</span></span>
<span data-ttu-id="16910-147">Указывает имя создаваемого набора данных.</span><span class="sxs-lookup"><span data-stu-id="16910-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="16910-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16910-148">-ResourceGroupName</span></span>
<span data-ttu-id="16910-149">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="16910-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="16910-150">Этот командлет создает набор данных в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16910-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16910-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16910-151">-Confirm</span></span>
<span data-ttu-id="16910-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16910-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16910-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16910-153">-WhatIf</span></span>
<span data-ttu-id="16910-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16910-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16910-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16910-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16910-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16910-156">CommonParameters</span></span>
<span data-ttu-id="16910-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16910-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16910-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16910-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16910-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16910-159">INPUTS</span></span>

### <span data-ttu-id="16910-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="16910-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="16910-161">System. String</span><span class="sxs-lookup"><span data-stu-id="16910-161">System.String</span></span>

## <span data-ttu-id="16910-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16910-162">OUTPUTS</span></span>

### <span data-ttu-id="16910-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="16910-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="16910-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="16910-164">NOTES</span></span>
* <span data-ttu-id="16910-165">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="16910-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16910-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16910-166">RELATED LINKS</span></span>

[<span data-ttu-id="16910-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="16910-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="16910-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="16910-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


