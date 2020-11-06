---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 47cbd81fa7e2e8f3877c2e933254cde4e2cee8ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556707"
---
# <span data-ttu-id="880a3-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="880a3-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="880a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="880a3-102">SYNOPSIS</span></span>
<span data-ttu-id="880a3-103">Связывание хранилища данных или облачной службы с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="880a3-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="880a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="880a3-104">SYNTAX</span></span>

### <span data-ttu-id="880a3-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="880a3-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="880a3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="880a3-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="880a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="880a3-107">DESCRIPTION</span></span>
<span data-ttu-id="880a3-108">Командлет Set-AzureRmDataFactoryV2LinkedService связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="880a3-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="880a3-109">При указании имени связанной службы, которая уже существует, этот командлет запрашивает подтверждение перед тем, как будет заменяться связанная служба.</span><span class="sxs-lookup"><span data-stu-id="880a3-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="880a3-110">Если указан параметр Force, командлет заменяет существующую связанную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="880a3-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="880a3-111">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="880a3-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="880a3-112">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="880a3-112">-- Create linked services.</span></span>
<span data-ttu-id="880a3-113">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="880a3-113">-- Create datasets.</span></span>
<span data-ttu-id="880a3-114">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="880a3-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="880a3-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="880a3-115">EXAMPLES</span></span>

### <span data-ttu-id="880a3-116">Пример 1: Создание связанной службы</span><span class="sxs-lookup"><span data-stu-id="880a3-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="880a3-117">Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="880a3-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="880a3-118">Эта связанная служба связывает хранилище больших двоичных объектов Azure, указанное в файле, с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="880a3-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="880a3-119">Команда передает результат в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="880a3-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="880a3-120">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="880a3-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="880a3-121">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="880a3-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="880a3-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="880a3-122">PARAMETERS</span></span>

### <span data-ttu-id="880a3-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="880a3-123">-DataFactoryName</span></span>
<span data-ttu-id="880a3-124">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="880a3-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="880a3-125">Этот командлет создает связанную службу для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="880a3-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="880a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880a3-126">-DefaultProfile</span></span>
<span data-ttu-id="880a3-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="880a3-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="880a3-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="880a3-128">-DefinitionFile</span></span>
<span data-ttu-id="880a3-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="880a3-129">The JSON file path.</span></span>

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

### <span data-ttu-id="880a3-130">-Force</span><span class="sxs-lookup"><span data-stu-id="880a3-130">-Force</span></span>
<span data-ttu-id="880a3-131">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="880a3-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="880a3-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="880a3-132">-Name</span></span>
<span data-ttu-id="880a3-133">Указывает имя связанной службы, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="880a3-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880a3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880a3-134">-ResourceGroupName</span></span>
<span data-ttu-id="880a3-135">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="880a3-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="880a3-136">Этот командлет создает связанную службу для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="880a3-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="880a3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="880a3-137">-ResourceId</span></span>
<span data-ttu-id="880a3-138">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="880a3-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="880a3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="880a3-139">-Confirm</span></span>
<span data-ttu-id="880a3-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="880a3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="880a3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="880a3-141">-WhatIf</span></span>
<span data-ttu-id="880a3-142">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="880a3-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="880a3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880a3-143">CommonParameters</span></span>
<span data-ttu-id="880a3-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="880a3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880a3-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880a3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880a3-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="880a3-146">INPUTS</span></span>

### <span data-ttu-id="880a3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="880a3-147">System.String</span></span>

## <span data-ttu-id="880a3-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="880a3-148">OUTPUTS</span></span>

### <span data-ttu-id="880a3-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="880a3-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="880a3-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="880a3-150">NOTES</span></span>
<span data-ttu-id="880a3-151">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="880a3-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="880a3-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="880a3-152">RELATED LINKS</span></span>

[<span data-ttu-id="880a3-153">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="880a3-153">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="880a3-154">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="880a3-154">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
