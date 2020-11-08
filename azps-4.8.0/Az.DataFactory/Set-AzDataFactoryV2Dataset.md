---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235617"
---
# <span data-ttu-id="03ac4-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="03ac4-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="03ac4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="03ac4-103">Создает набор данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="03ac4-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="03ac4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03ac4-104">SYNTAX</span></span>

### <span data-ttu-id="03ac4-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03ac4-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03ac4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03ac4-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ac4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ac4-107">DESCRIPTION</span></span>
<span data-ttu-id="03ac4-108">Командлет Set-AzDataFactoryV2Dataset создает набор данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="03ac4-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="03ac4-109">Если вы задаете имя уже существующего набора данных, этот командлет запрашивает подтверждение перед заменой набора данных.</span><span class="sxs-lookup"><span data-stu-id="03ac4-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="03ac4-110">Если указан параметр Force, командлет заменяет существующий набор данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="03ac4-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="03ac4-111">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="03ac4-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="03ac4-112">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="03ac4-112">-- Create linked services.</span></span>
<span data-ttu-id="03ac4-113">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="03ac4-113">-- Create datasets.</span></span>
<span data-ttu-id="03ac4-114">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="03ac4-114">-- Create a pipeline.</span></span>
<span data-ttu-id="03ac4-115">Если набор данных с таким же именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписать существующий набор данных новым.</span><span class="sxs-lookup"><span data-stu-id="03ac4-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="03ac4-116">Если вы подтвердите переписать существующий набор данных, определение набора данных также заменяется.</span><span class="sxs-lookup"><span data-stu-id="03ac4-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="03ac4-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03ac4-117">EXAMPLES</span></span>

### <span data-ttu-id="03ac4-118">Пример 1: создание набора данных</span><span class="sxs-lookup"><span data-stu-id="03ac4-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="03ac4-119">Эта команда создает набор данных с именем DA_WikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="03ac4-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="03ac4-120">В команде набор данных заосновывается на сведениях в DAWikipediaClickEvents.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="03ac4-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="03ac4-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03ac4-121">PARAMETERS</span></span>

### <span data-ttu-id="03ac4-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="03ac4-122">-DataFactoryName</span></span>
<span data-ttu-id="03ac4-123">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="03ac4-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="03ac4-124">Этот командлет создает набор данных в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="03ac4-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="03ac4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ac4-125">-DefaultProfile</span></span>
<span data-ttu-id="03ac4-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03ac4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ac4-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="03ac4-127">-DefinitionFile</span></span>
<span data-ttu-id="03ac4-128">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="03ac4-128">The JSON file path.</span></span>

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

### <span data-ttu-id="03ac4-129">-Force</span><span class="sxs-lookup"><span data-stu-id="03ac4-129">-Force</span></span>
<span data-ttu-id="03ac4-130">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="03ac4-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="03ac4-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03ac4-131">-Name</span></span>
<span data-ttu-id="03ac4-132">Указывает имя создаваемого набора данных.</span><span class="sxs-lookup"><span data-stu-id="03ac4-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="03ac4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ac4-133">-ResourceGroupName</span></span>
<span data-ttu-id="03ac4-134">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="03ac4-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="03ac4-135">Этот командлет создает набор данных в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="03ac4-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="03ac4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03ac4-136">-ResourceId</span></span>
<span data-ttu-id="03ac4-137">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="03ac4-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="03ac4-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03ac4-138">-Confirm</span></span>
<span data-ttu-id="03ac4-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03ac4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ac4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ac4-140">-WhatIf</span></span>
<span data-ttu-id="03ac4-141">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="03ac4-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="03ac4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ac4-142">CommonParameters</span></span>
<span data-ttu-id="03ac4-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03ac4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ac4-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ac4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ac4-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03ac4-145">INPUTS</span></span>

### <span data-ttu-id="03ac4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="03ac4-146">System.String</span></span>

## <span data-ttu-id="03ac4-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ac4-147">OUTPUTS</span></span>

### <span data-ttu-id="03ac4-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="03ac4-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="03ac4-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="03ac4-149">NOTES</span></span>
<span data-ttu-id="03ac4-150">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="03ac4-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="03ac4-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03ac4-151">RELATED LINKS</span></span>

[<span data-ttu-id="03ac4-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="03ac4-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="03ac4-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="03ac4-153">Remove-AzDataFactoryV2Dataset</span></span>]()