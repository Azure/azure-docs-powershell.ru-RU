---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 46d631c9fed6906db44bc91b6f8624abb4499ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564604"
---
# <span data-ttu-id="e956e-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e956e-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="e956e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e956e-102">SYNOPSIS</span></span>
<span data-ttu-id="e956e-103">Создает набор данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="e956e-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e956e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e956e-104">SYNTAX</span></span>

### <span data-ttu-id="e956e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e956e-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e956e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e956e-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e956e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e956e-107">DESCRIPTION</span></span>
<span data-ttu-id="e956e-108">Командлет Set-AzureRmDataFactoryV2Dataset создает набор данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="e956e-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="e956e-109">Если вы задаете имя уже существующего набора данных, этот командлет запрашивает подтверждение перед заменой набора данных.</span><span class="sxs-lookup"><span data-stu-id="e956e-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="e956e-110">Если указан параметр Force, командлет заменяет существующий набор данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e956e-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="e956e-111">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e956e-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e956e-112">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="e956e-112">-- Create linked services.</span></span>
<span data-ttu-id="e956e-113">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="e956e-113">-- Create datasets.</span></span>
<span data-ttu-id="e956e-114">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="e956e-114">-- Create a pipeline.</span></span>
<span data-ttu-id="e956e-115">Если набор данных с таким же именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписать существующий набор данных новым.</span><span class="sxs-lookup"><span data-stu-id="e956e-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="e956e-116">Если вы подтвердите переписать существующий набор данных, определение набора данных также заменяется.</span><span class="sxs-lookup"><span data-stu-id="e956e-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="e956e-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e956e-117">EXAMPLES</span></span>

### <span data-ttu-id="e956e-118">Пример 1: создание набора данных</span><span class="sxs-lookup"><span data-stu-id="e956e-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="e956e-119">Эта команда создает набор данных с именем DA_WikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e956e-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="e956e-120">В команде набор данных заосновывается на сведениях в DAWikipediaClickEvents.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="e956e-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="e956e-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e956e-121">PARAMETERS</span></span>

### <span data-ttu-id="e956e-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e956e-122">-DataFactoryName</span></span>
<span data-ttu-id="e956e-123">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e956e-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e956e-124">Этот командлет создает набор данных в фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e956e-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e956e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e956e-125">-DefaultProfile</span></span>
<span data-ttu-id="e956e-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e956e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e956e-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e956e-127">-DefinitionFile</span></span>
<span data-ttu-id="e956e-128">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="e956e-128">The JSON file path.</span></span>

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

### <span data-ttu-id="e956e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e956e-129">-Force</span></span>
<span data-ttu-id="e956e-130">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e956e-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e956e-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e956e-131">-Name</span></span>
<span data-ttu-id="e956e-132">Указывает имя создаваемого набора данных.</span><span class="sxs-lookup"><span data-stu-id="e956e-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="e956e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e956e-133">-ResourceGroupName</span></span>
<span data-ttu-id="e956e-134">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e956e-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e956e-135">Этот командлет создает набор данных в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="e956e-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e956e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e956e-136">-ResourceId</span></span>
<span data-ttu-id="e956e-137">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e956e-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e956e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e956e-138">-Confirm</span></span>
<span data-ttu-id="e956e-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e956e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e956e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e956e-140">-WhatIf</span></span>
<span data-ttu-id="e956e-141">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="e956e-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e956e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e956e-142">CommonParameters</span></span>
<span data-ttu-id="e956e-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e956e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e956e-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e956e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e956e-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e956e-145">INPUTS</span></span>

### <span data-ttu-id="e956e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e956e-146">System.String</span></span>

## <span data-ttu-id="e956e-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e956e-147">OUTPUTS</span></span>

### <span data-ttu-id="e956e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e956e-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="e956e-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="e956e-149">NOTES</span></span>
<span data-ttu-id="e956e-150">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="e956e-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e956e-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e956e-151">RELATED LINKS</span></span>

[<span data-ttu-id="e956e-152">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e956e-152">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="e956e-153">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e956e-153">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
