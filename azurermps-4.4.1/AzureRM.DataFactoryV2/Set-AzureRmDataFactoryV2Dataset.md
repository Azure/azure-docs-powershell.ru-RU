---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 311073fcd840e9d163c1316019e48569f7e59c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735189"
---
# <span data-ttu-id="299af-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="299af-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="299af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="299af-102">SYNOPSIS</span></span>
<span data-ttu-id="299af-103">Создает набор данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="299af-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="299af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="299af-104">SYNTAX</span></span>

### <span data-ttu-id="299af-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="299af-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="299af-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="299af-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="299af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="299af-107">DESCRIPTION</span></span>
<span data-ttu-id="299af-108">Командлет Set-AzureRmDataFactoryV2Dataset создает набор данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="299af-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="299af-109">Если вы задаете имя уже существующего набора данных, этот командлет запрашивает подтверждение перед заменой набора данных.</span><span class="sxs-lookup"><span data-stu-id="299af-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="299af-110">Если указан параметр Force, командлет заменяет существующий набор данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="299af-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="299af-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="299af-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="299af-112">Если набор данных с таким же именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписать существующий набор данных новым.</span><span class="sxs-lookup"><span data-stu-id="299af-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="299af-113">Если вы подтвердите переписать существующий набор данных, определение набора данных также заменяется.</span><span class="sxs-lookup"><span data-stu-id="299af-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="299af-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="299af-114">EXAMPLES</span></span>

### <span data-ttu-id="299af-115">Пример 1: создание набора данных</span><span class="sxs-lookup"><span data-stu-id="299af-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="299af-116">Эта команда создает набор данных с именем DA_WikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="299af-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="299af-117">В команде набор данных заосновывается на сведениях в DAWikipediaClickEvents.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="299af-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="299af-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="299af-118">PARAMETERS</span></span>

### <span data-ttu-id="299af-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="299af-119">-Confirm</span></span>
<span data-ttu-id="299af-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="299af-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299af-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="299af-121">-DataFactoryName</span></span>
<span data-ttu-id="299af-122">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="299af-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="299af-123">Этот командлет создает набор данных в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="299af-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="299af-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="299af-124">-DefinitionFile</span></span>
<span data-ttu-id="299af-125">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="299af-125">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299af-126">-Force</span><span class="sxs-lookup"><span data-stu-id="299af-126">-Force</span></span>
<span data-ttu-id="299af-127">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="299af-127">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299af-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="299af-128">-Name</span></span>
<span data-ttu-id="299af-129">Указывает имя создаваемого набора данных.</span><span class="sxs-lookup"><span data-stu-id="299af-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299af-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299af-130">-ResourceGroupName</span></span>
<span data-ttu-id="299af-131">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="299af-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="299af-132">Этот командлет создает набор данных в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="299af-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="299af-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="299af-133">-ResourceId</span></span>
<span data-ttu-id="299af-134">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="299af-134">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299af-135">-WhatIf</span></span>
<span data-ttu-id="299af-136">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="299af-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="299af-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="299af-137">INPUTS</span></span>

### <span data-ttu-id="299af-138">System. String</span><span class="sxs-lookup"><span data-stu-id="299af-138">System.String</span></span>


## <span data-ttu-id="299af-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="299af-139">OUTPUTS</span></span>

### <span data-ttu-id="299af-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="299af-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="299af-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="299af-141">NOTES</span></span>
<span data-ttu-id="299af-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="299af-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="299af-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="299af-143">RELATED LINKS</span></span>
[<span data-ttu-id="299af-144">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="299af-144">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="299af-145">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="299af-145">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
