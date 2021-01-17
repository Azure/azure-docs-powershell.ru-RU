---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324509"
---
# <span data-ttu-id="a8b1b-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a8b1b-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="a8b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b1b-103">Связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="a8b1b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8b1b-104">SYNTAX</span></span>

### <span data-ttu-id="a8b1b-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8b1b-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8b1b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a8b1b-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b1b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="a8b1b-108">**Cmdlet New-AzDataFactoryLinkedService** связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="a8b1b-109">Если указать имя связанной службы, которая уже существует, этот cmdlet запросит подтверждение перед заменой связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="a8b1b-110">Если указать параметр *Force,* он заменяет существующую связанную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="a8b1b-111">Выполните эти действия в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="a8b1b-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="a8b1b-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-112">Create a data factory.</span></span> 
- <span data-ttu-id="a8b1b-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-113">Create linked services.</span></span> 
- <span data-ttu-id="a8b1b-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-114">Create datasets.</span></span> 
- <span data-ttu-id="a8b1b-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-115">Create a pipeline.</span></span>

## <span data-ttu-id="a8b1b-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8b1b-116">EXAMPLES</span></span>

### <span data-ttu-id="a8b1b-117">Пример 1. Создание связанной службы</span><span class="sxs-lookup"><span data-stu-id="a8b1b-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="a8b1b-118">Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="a8b1b-119">Эта связанная служба связывает хранилище BLOB-файлов Azure, указанное в файле, с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="a8b1b-120">Команда передает результат командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a8b1b-121">Это Windows PowerShell форматирование результатов.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="a8b1b-122">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="a8b1b-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="a8b1b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8b1b-123">PARAMETERS</span></span>

### <span data-ttu-id="a8b1b-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a8b1b-124">-DataFactory</span></span>
<span data-ttu-id="a8b1b-125">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="a8b1b-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a8b1b-126">Этот cmdlet создает связанную службу для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8b1b-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a8b1b-127">-DataFactoryName</span></span>
<span data-ttu-id="a8b1b-128">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a8b1b-129">Этот cmdlet создает связанную службу для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8b1b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b1b-130">-DefaultProfile</span></span>
<span data-ttu-id="a8b1b-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8b1b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8b1b-132">-File</span><span class="sxs-lookup"><span data-stu-id="a8b1b-132">-File</span></span>
<span data-ttu-id="a8b1b-133">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="a8b1b-134">-Force</span><span class="sxs-lookup"><span data-stu-id="a8b1b-134">-Force</span></span>
<span data-ttu-id="a8b1b-135">Указывает на то, что этот cmdlet заменяет существующую связанную службу без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a8b1b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="a8b1b-136">-Name</span></span>
<span data-ttu-id="a8b1b-137">Указывает имя связанной службы, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="a8b1b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b1b-138">-ResourceGroupName</span></span>
<span data-ttu-id="a8b1b-139">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a8b1b-140">Этот cmdlet создает связанную службу для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a8b1b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8b1b-141">-Confirm</span></span>
<span data-ttu-id="a8b1b-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b1b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b1b-143">-WhatIf</span></span>
<span data-ttu-id="a8b1b-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8b1b-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b1b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b1b-146">CommonParameters</span></span>
<span data-ttu-id="a8b1b-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8b1b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b1b-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b1b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b1b-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8b1b-149">INPUTS</span></span>

### <span data-ttu-id="a8b1b-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a8b1b-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a8b1b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a8b1b-151">System.String</span></span>

## <span data-ttu-id="a8b1b-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8b1b-152">OUTPUTS</span></span>

### <span data-ttu-id="a8b1b-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a8b1b-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="a8b1b-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8b1b-154">NOTES</span></span>
* <span data-ttu-id="a8b1b-155">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="a8b1b-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a8b1b-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8b1b-156">RELATED LINKS</span></span>

[<span data-ttu-id="a8b1b-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a8b1b-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="a8b1b-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a8b1b-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


