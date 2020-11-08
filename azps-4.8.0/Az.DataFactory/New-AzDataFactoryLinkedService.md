---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236788"
---
# <span data-ttu-id="c2de1-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="c2de1-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="c2de1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2de1-102">SYNOPSIS</span></span>
<span data-ttu-id="c2de1-103">Связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c2de1-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="c2de1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2de1-104">SYNTAX</span></span>

### <span data-ttu-id="c2de1-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2de1-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2de1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c2de1-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2de1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2de1-107">DESCRIPTION</span></span>
<span data-ttu-id="c2de1-108">Командлет **New-AzDataFactoryLinkedService** связывает хранилище данных или облачную службу с фабрикой данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c2de1-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="c2de1-109">При указании имени связанной службы, которая уже существует, этот командлет запрашивает подтверждение перед тем, как будет заменяться связанная служба.</span><span class="sxs-lookup"><span data-stu-id="c2de1-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="c2de1-110">Если указан параметр *Force* , командлет заменяет существующую связанную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c2de1-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="c2de1-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c2de1-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="c2de1-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c2de1-112">Create a data factory.</span></span> 
- <span data-ttu-id="c2de1-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="c2de1-113">Create linked services.</span></span> 
- <span data-ttu-id="c2de1-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="c2de1-114">Create datasets.</span></span> 
- <span data-ttu-id="c2de1-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2de1-115">Create a pipeline.</span></span>

## <span data-ttu-id="c2de1-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2de1-116">EXAMPLES</span></span>

### <span data-ttu-id="c2de1-117">Пример 1: Создание связанной службы</span><span class="sxs-lookup"><span data-stu-id="c2de1-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="c2de1-118">Эта команда создает связанную службу с именем LinkedServiceCuratedWikiData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c2de1-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="c2de1-119">Эта связанная служба связывает хранилище больших двоичных объектов Azure, указанное в файле, с фабрикой данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c2de1-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="c2de1-120">Команда передает результат в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2de1-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c2de1-121">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="c2de1-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="c2de1-122">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="c2de1-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="c2de1-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2de1-123">PARAMETERS</span></span>

### <span data-ttu-id="c2de1-124">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="c2de1-124">-DataFactory</span></span>
<span data-ttu-id="c2de1-125">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c2de1-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c2de1-126">Этот командлет создает связанную службу для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c2de1-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2de1-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2de1-127">-DataFactoryName</span></span>
<span data-ttu-id="c2de1-128">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c2de1-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c2de1-129">Этот командлет создает связанную службу для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c2de1-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2de1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2de1-130">-DefaultProfile</span></span>
<span data-ttu-id="c2de1-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c2de1-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2de1-132">-Файл</span><span class="sxs-lookup"><span data-stu-id="c2de1-132">-File</span></span>
<span data-ttu-id="c2de1-133">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание связанной службы.</span><span class="sxs-lookup"><span data-stu-id="c2de1-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="c2de1-134">-Force</span><span class="sxs-lookup"><span data-stu-id="c2de1-134">-Force</span></span>
<span data-ttu-id="c2de1-135">Указывает на то, что этот командлет заменяет существующую связанную службу, не запрашивая подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c2de1-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c2de1-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2de1-136">-Name</span></span>
<span data-ttu-id="c2de1-137">Указывает имя связанной службы, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="c2de1-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="c2de1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2de1-138">-ResourceGroupName</span></span>
<span data-ttu-id="c2de1-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c2de1-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c2de1-140">Этот командлет создает связанную службу для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c2de1-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c2de1-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2de1-141">-Confirm</span></span>
<span data-ttu-id="c2de1-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2de1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2de1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2de1-143">-WhatIf</span></span>
<span data-ttu-id="c2de1-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2de1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2de1-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2de1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2de1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2de1-146">CommonParameters</span></span>
<span data-ttu-id="c2de1-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2de1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2de1-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2de1-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2de1-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2de1-149">INPUTS</span></span>

### <span data-ttu-id="c2de1-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c2de1-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c2de1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c2de1-151">System.String</span></span>

## <span data-ttu-id="c2de1-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2de1-152">OUTPUTS</span></span>

### <span data-ttu-id="c2de1-153">Microsoft. Azure. Commands. Factoring. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="c2de1-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="c2de1-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2de1-154">NOTES</span></span>
* <span data-ttu-id="c2de1-155">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="c2de1-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c2de1-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2de1-156">RELATED LINKS</span></span>

[<span data-ttu-id="c2de1-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="c2de1-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="c2de1-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="c2de1-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


