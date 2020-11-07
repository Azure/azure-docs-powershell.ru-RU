---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 2ff8e4a92c01c38b81ad5f1fded5661501b1c46c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721435"
---
# <span data-ttu-id="ebebd-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ebebd-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="ebebd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebebd-102">SYNOPSIS</span></span>
<span data-ttu-id="ebebd-103">Связывание хранилища данных или облачной службы с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="ebebd-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="ebebd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebebd-104">SYNTAX</span></span>

### <span data-ttu-id="ebebd-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebebd-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebebd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebebd-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebebd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebebd-107">DESCRIPTION</span></span>
<span data-ttu-id="ebebd-108">Командлет Set-AzDataFactoryV2LinkedService связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ebebd-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="ebebd-109">При указании имени связанной службы, которая уже существует, этот командлет запрашивает подтверждение перед тем, как будет заменяться связанная служба.</span><span class="sxs-lookup"><span data-stu-id="ebebd-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="ebebd-110">Если указан параметр Force, командлет заменяет существующую связанную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ebebd-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="ebebd-111">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ebebd-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="ebebd-112">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="ebebd-112">-- Create linked services.</span></span>
<span data-ttu-id="ebebd-113">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="ebebd-113">-- Create datasets.</span></span>
<span data-ttu-id="ebebd-114">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="ebebd-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="ebebd-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebebd-115">EXAMPLES</span></span>

### <span data-ttu-id="ebebd-116">Пример 1: Создание связанной службы</span><span class="sxs-lookup"><span data-stu-id="ebebd-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="ebebd-117">Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ebebd-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="ebebd-118">Эта связанная служба связывает хранилище больших двоичных объектов Azure, указанное в файле, с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ebebd-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="ebebd-119">Команда передает результат в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ebebd-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebebd-120">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="ebebd-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ebebd-121">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="ebebd-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="ebebd-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebebd-122">PARAMETERS</span></span>

### <span data-ttu-id="ebebd-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ebebd-123">-DataFactoryName</span></span>
<span data-ttu-id="ebebd-124">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ebebd-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ebebd-125">Этот командлет создает связанную службу для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ebebd-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ebebd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebebd-126">-DefaultProfile</span></span>
<span data-ttu-id="ebebd-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebebd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebebd-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ebebd-128">-DefinitionFile</span></span>
<span data-ttu-id="ebebd-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="ebebd-129">The JSON file path.</span></span>

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

### <span data-ttu-id="ebebd-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ebebd-130">-Force</span></span>
<span data-ttu-id="ebebd-131">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ebebd-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ebebd-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebebd-132">-Name</span></span>
<span data-ttu-id="ebebd-133">Указывает имя связанной службы, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="ebebd-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="ebebd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebebd-134">-ResourceGroupName</span></span>
<span data-ttu-id="ebebd-135">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ebebd-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ebebd-136">Этот командлет создает связанную службу для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ebebd-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ebebd-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebebd-137">-ResourceId</span></span>
<span data-ttu-id="ebebd-138">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="ebebd-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ebebd-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebebd-139">-Confirm</span></span>
<span data-ttu-id="ebebd-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebebd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebebd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebebd-141">-WhatIf</span></span>
<span data-ttu-id="ebebd-142">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="ebebd-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ebebd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebebd-143">CommonParameters</span></span>
<span data-ttu-id="ebebd-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebebd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebebd-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebebd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebebd-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebebd-146">INPUTS</span></span>

### <span data-ttu-id="ebebd-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ebebd-147">System.String</span></span>

## <span data-ttu-id="ebebd-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebebd-148">OUTPUTS</span></span>

### <span data-ttu-id="ebebd-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="ebebd-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="ebebd-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebebd-150">NOTES</span></span>
<span data-ttu-id="ebebd-151">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="ebebd-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ebebd-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebebd-152">RELATED LINKS</span></span>

[<span data-ttu-id="ebebd-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ebebd-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="ebebd-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="ebebd-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
