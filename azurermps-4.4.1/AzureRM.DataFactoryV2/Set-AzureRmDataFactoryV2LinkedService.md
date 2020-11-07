---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: f977344f2beabe8352a7417130063c3e9d4d3e1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735188"
---
# <span data-ttu-id="01e49-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="01e49-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="01e49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01e49-102">SYNOPSIS</span></span>
<span data-ttu-id="01e49-103">Связывание хранилища данных или облачной службы с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="01e49-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01e49-104">SYNTAX</span></span>

### <span data-ttu-id="01e49-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01e49-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="01e49-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01e49-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="01e49-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e49-107">DESCRIPTION</span></span>
<span data-ttu-id="01e49-108">Командлет Set-AzureRmDataFactoryV2LinkedService связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="01e49-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="01e49-109">При указании имени связанной службы, которая уже существует, этот командлет запрашивает подтверждение перед тем, как будет заменяться связанная служба.</span><span class="sxs-lookup"><span data-stu-id="01e49-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="01e49-110">Если указан параметр Force, командлет заменяет существующую связанную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="01e49-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="01e49-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="01e49-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="01e49-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01e49-112">EXAMPLES</span></span>

### <span data-ttu-id="01e49-113">Пример 1: Создание связанной службы</span><span class="sxs-lookup"><span data-stu-id="01e49-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

```

<span data-ttu-id="01e49-114">Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="01e49-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="01e49-115">Эта связанная служба связывает хранилище больших двоичных объектов Azure, указанное в файле, с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="01e49-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="01e49-116">Команда передает результат в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="01e49-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="01e49-117">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="01e49-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="01e49-118">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="01e49-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="01e49-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01e49-119">PARAMETERS</span></span>

### <span data-ttu-id="01e49-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e49-120">-Confirm</span></span>
<span data-ttu-id="01e49-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01e49-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e49-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="01e49-122">-DataFactoryName</span></span>
<span data-ttu-id="01e49-123">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="01e49-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="01e49-124">Этот командлет создает связанную службу для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="01e49-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="01e49-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="01e49-125">-DefinitionFile</span></span>
<span data-ttu-id="01e49-126">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="01e49-126">The JSON file path.</span></span>

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

### <span data-ttu-id="01e49-127">-Force</span><span class="sxs-lookup"><span data-stu-id="01e49-127">-Force</span></span>
<span data-ttu-id="01e49-128">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="01e49-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="01e49-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01e49-129">-Name</span></span>
<span data-ttu-id="01e49-130">Указывает имя связанной службы, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="01e49-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e49-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e49-131">-ResourceGroupName</span></span>
<span data-ttu-id="01e49-132">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="01e49-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="01e49-133">Этот командлет создает связанную службу для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="01e49-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="01e49-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01e49-134">-ResourceId</span></span>
<span data-ttu-id="01e49-135">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="01e49-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="01e49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e49-136">-WhatIf</span></span>
<span data-ttu-id="01e49-137">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="01e49-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="01e49-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01e49-138">INPUTS</span></span>

### <span data-ttu-id="01e49-139">System. String</span><span class="sxs-lookup"><span data-stu-id="01e49-139">System.String</span></span>


## <span data-ttu-id="01e49-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e49-140">OUTPUTS</span></span>

### <span data-ttu-id="01e49-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="01e49-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="01e49-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="01e49-142">NOTES</span></span>
<span data-ttu-id="01e49-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="01e49-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="01e49-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01e49-144">RELATED LINKS</span></span>
[<span data-ttu-id="01e49-145">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="01e49-145">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="01e49-146">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="01e49-146">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
