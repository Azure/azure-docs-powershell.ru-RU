---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409463"
---
# <span data-ttu-id="a41e2-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a41e2-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="a41e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a41e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a41e2-103">Связывает хранилище данных или облачную службу с фабрикой данных.</span><span class="sxs-lookup"><span data-stu-id="a41e2-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="a41e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a41e2-104">SYNTAX</span></span>

### <span data-ttu-id="a41e2-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a41e2-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a41e2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a41e2-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a41e2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a41e2-107">DESCRIPTION</span></span>
<span data-ttu-id="a41e2-108">Этот Set-AzDataFactoryV2LinkedService связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a41e2-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="a41e2-109">Если указать имя связанной службы, которая уже существует, этот cmdlet запросит подтверждение перед заменой связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a41e2-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="a41e2-110">Если указать параметр Force, то вместо существующей связанной службы не будет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a41e2-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="a41e2-111">Выполните эти действия в следующем порядке: создайте фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="a41e2-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="a41e2-112">-- Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="a41e2-112">-- Create linked services.</span></span>
<span data-ttu-id="a41e2-113">— создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="a41e2-113">-- Create datasets.</span></span>
<span data-ttu-id="a41e2-114">— создать канал.</span><span class="sxs-lookup"><span data-stu-id="a41e2-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="a41e2-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a41e2-115">EXAMPLES</span></span>

### <span data-ttu-id="a41e2-116">Пример 1. Создание связанной службы</span><span class="sxs-lookup"><span data-stu-id="a41e2-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="a41e2-117">Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a41e2-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="a41e2-118">Эта связанная служба связывает указанное в файле хранилище BLOB-приложений Azure с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a41e2-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="a41e2-119">Команда передает результат командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a41e2-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a41e2-120">Это Windows PowerShell форматирование результатов.</span><span class="sxs-lookup"><span data-stu-id="a41e2-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="a41e2-121">Для получения дополнительных сведений введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="a41e2-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="a41e2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a41e2-122">PARAMETERS</span></span>

### <span data-ttu-id="a41e2-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a41e2-123">-DataFactoryName</span></span>
<span data-ttu-id="a41e2-124">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a41e2-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a41e2-125">Этот cmdlet создает связанную службу для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a41e2-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a41e2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41e2-126">-DefaultProfile</span></span>
<span data-ttu-id="a41e2-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a41e2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a41e2-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="a41e2-128">-DefinitionFile</span></span>
<span data-ttu-id="a41e2-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="a41e2-129">The JSON file path.</span></span>

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

### <span data-ttu-id="a41e2-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a41e2-130">-Force</span></span>
<span data-ttu-id="a41e2-131">Выполняется cmdlet без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a41e2-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a41e2-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a41e2-132">-Name</span></span>
<span data-ttu-id="a41e2-133">Указывает имя создаемой связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a41e2-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="a41e2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a41e2-134">-ResourceGroupName</span></span>
<span data-ttu-id="a41e2-135">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a41e2-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a41e2-136">Этот cmdlet создает связанную службу для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a41e2-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a41e2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a41e2-137">-ResourceId</span></span>
<span data-ttu-id="a41e2-138">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="a41e2-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a41e2-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a41e2-139">-Confirm</span></span>
<span data-ttu-id="a41e2-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a41e2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a41e2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a41e2-141">-WhatIf</span></span>
<span data-ttu-id="a41e2-142">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a41e2-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a41e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41e2-143">CommonParameters</span></span>
<span data-ttu-id="a41e2-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a41e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41e2-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a41e2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41e2-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a41e2-146">INPUTS</span></span>

### <span data-ttu-id="a41e2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a41e2-147">System.String</span></span>

## <span data-ttu-id="a41e2-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a41e2-148">OUTPUTS</span></span>

### <span data-ttu-id="a41e2-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a41e2-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="a41e2-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a41e2-150">NOTES</span></span>
<span data-ttu-id="a41e2-151">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="a41e2-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a41e2-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a41e2-152">RELATED LINKS</span></span>

[<span data-ttu-id="a41e2-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a41e2-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="a41e2-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a41e2-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
