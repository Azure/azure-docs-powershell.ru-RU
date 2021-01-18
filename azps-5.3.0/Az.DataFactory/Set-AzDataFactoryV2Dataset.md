---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518910"
---
# <span data-ttu-id="67049-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="67049-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="67049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67049-102">SYNOPSIS</span></span>
<span data-ttu-id="67049-103">Создает набор данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="67049-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="67049-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67049-104">SYNTAX</span></span>

### <span data-ttu-id="67049-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67049-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67049-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67049-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67049-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67049-107">DESCRIPTION</span></span>
<span data-ttu-id="67049-108">Новый Set-AzDataFactoryV2Dataset создает набор данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="67049-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="67049-109">Если указать имя для уже существующий набор данных, этот cmdlet запросит подтверждение перед заменой.</span><span class="sxs-lookup"><span data-stu-id="67049-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="67049-110">При указании параметра Force существующий набор данных будет замещается этим набором данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="67049-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="67049-111">Выполните эти действия в следующем порядке: создайте фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="67049-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="67049-112">-- Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="67049-112">-- Create linked services.</span></span>
<span data-ttu-id="67049-113">— создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="67049-113">-- Create datasets.</span></span>
<span data-ttu-id="67049-114">— создать канал.</span><span class="sxs-lookup"><span data-stu-id="67049-114">-- Create a pipeline.</span></span>
<span data-ttu-id="67049-115">Если в фабрике данных уже существует набор данных с таким же именем, этот набор будет предложено подтвердить, следует ли перезаписать существующий набор данных с помощью нового.</span><span class="sxs-lookup"><span data-stu-id="67049-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="67049-116">Если вы подтверждаете, что существующий набор данных переопишется, его определение также заменяется.</span><span class="sxs-lookup"><span data-stu-id="67049-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="67049-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67049-117">EXAMPLES</span></span>

### <span data-ttu-id="67049-118">Пример 1. Создание наборов данных</span><span class="sxs-lookup"><span data-stu-id="67049-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="67049-119">Эта команда создает набор данных с именем DA_WikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="67049-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="67049-120">Эта команда будет базой данных на данных из DAWikipediaClickEvents.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="67049-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="67049-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67049-121">PARAMETERS</span></span>

### <span data-ttu-id="67049-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="67049-122">-DataFactoryName</span></span>
<span data-ttu-id="67049-123">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="67049-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="67049-124">Этот cmdlet создает набор данных в фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="67049-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="67049-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67049-125">-DefaultProfile</span></span>
<span data-ttu-id="67049-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67049-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67049-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="67049-127">-DefinitionFile</span></span>
<span data-ttu-id="67049-128">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="67049-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67049-129">-Force</span><span class="sxs-lookup"><span data-stu-id="67049-129">-Force</span></span>
<span data-ttu-id="67049-130">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="67049-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="67049-131">-Name</span><span class="sxs-lookup"><span data-stu-id="67049-131">-Name</span></span>
<span data-ttu-id="67049-132">Указывает имя созда создаемого наборов данных.</span><span class="sxs-lookup"><span data-stu-id="67049-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67049-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67049-133">-ResourceGroupName</span></span>
<span data-ttu-id="67049-134">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="67049-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="67049-135">Этот cmdlet создает набор данных в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="67049-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="67049-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67049-136">-ResourceId</span></span>
<span data-ttu-id="67049-137">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="67049-137">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67049-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67049-138">-Confirm</span></span>
<span data-ttu-id="67049-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="67049-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67049-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67049-140">-WhatIf</span></span>
<span data-ttu-id="67049-141">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67049-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67049-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67049-142">CommonParameters</span></span>
<span data-ttu-id="67049-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67049-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67049-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67049-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67049-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67049-145">INPUTS</span></span>

### <span data-ttu-id="67049-146">System.String</span><span class="sxs-lookup"><span data-stu-id="67049-146">System.String</span></span>

## <span data-ttu-id="67049-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67049-147">OUTPUTS</span></span>

### <span data-ttu-id="67049-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="67049-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="67049-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67049-149">NOTES</span></span>
<span data-ttu-id="67049-150">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="67049-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="67049-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67049-151">RELATED LINKS</span></span>

[<span data-ttu-id="67049-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="67049-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="67049-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="67049-153">Remove-AzDataFactoryV2Dataset</span></span>]()
