---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508493"
---
# <span data-ttu-id="1a88c-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1a88c-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="1a88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a88c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a88c-103">Создает конвейер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1a88c-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="1a88c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a88c-104">SYNTAX</span></span>

### <span data-ttu-id="1a88c-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a88c-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a88c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1a88c-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a88c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a88c-107">DESCRIPTION</span></span>
<span data-ttu-id="1a88c-108">Для создания конвейера в фабрике данных Azure создается новый **cmdlet AzDataFactoryPipeline.**</span><span class="sxs-lookup"><span data-stu-id="1a88c-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="1a88c-109">Если указать имя для конвейера, который уже существует, то перед заменой конвейера будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1a88c-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="1a88c-110">При указании *параметра Force* вместо существующего конвейера не будет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1a88c-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="1a88c-111">Выполните эти действия в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="1a88c-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="1a88c-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1a88c-112">Create a data factory.</span></span> 
- <span data-ttu-id="1a88c-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="1a88c-113">Create linked services.</span></span> 
- <span data-ttu-id="1a88c-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="1a88c-114">Create datasets.</span></span> 
- <span data-ttu-id="1a88c-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="1a88c-115">Create a pipeline.</span></span>
<span data-ttu-id="1a88c-116">Если в фабрике данных уже существует канал с таким же именем, этот cmdlet запросит подтверждение перезаписи существующего конвейера с помощью нового.</span><span class="sxs-lookup"><span data-stu-id="1a88c-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="1a88c-117">При подтверждении переописи существующего конвейера определение конвейера также заменяется.</span><span class="sxs-lookup"><span data-stu-id="1a88c-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="1a88c-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a88c-118">EXAMPLES</span></span>

### <span data-ttu-id="1a88c-119">Пример 1. Создание конвейера</span><span class="sxs-lookup"><span data-stu-id="1a88c-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="1a88c-120">Эта команда создает конвейер под названием DPWikisample в фабрике данных ADF.</span><span class="sxs-lookup"><span data-stu-id="1a88c-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="1a88c-121">Эта команда будет базой данных в канале, DPWikisample.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="1a88c-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="1a88c-122">Этот файл содержит сведения о действиях, таких как копирование и HDInsight в конвейере.</span><span class="sxs-lookup"><span data-stu-id="1a88c-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="1a88c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a88c-123">PARAMETERS</span></span>

### <span data-ttu-id="1a88c-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1a88c-124">-DataFactory</span></span>
<span data-ttu-id="1a88c-125">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="1a88c-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1a88c-126">Этот cmdlet создает канал для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1a88c-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a88c-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1a88c-127">-DataFactoryName</span></span>
<span data-ttu-id="1a88c-128">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1a88c-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1a88c-129">Этот cmdlet создает канал для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1a88c-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a88c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a88c-130">-DefaultProfile</span></span>
<span data-ttu-id="1a88c-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a88c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a88c-132">-File</span><span class="sxs-lookup"><span data-stu-id="1a88c-132">-File</span></span>
<span data-ttu-id="1a88c-133">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание конвейера.</span><span class="sxs-lookup"><span data-stu-id="1a88c-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="1a88c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="1a88c-134">-Force</span></span>
<span data-ttu-id="1a88c-135">Указывает на то, что этот cmdlet заменяет существующий канал без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1a88c-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1a88c-136">-Name</span><span class="sxs-lookup"><span data-stu-id="1a88c-136">-Name</span></span>
<span data-ttu-id="1a88c-137">Указывает имя созда создаемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="1a88c-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a88c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a88c-138">-ResourceGroupName</span></span>
<span data-ttu-id="1a88c-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1a88c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1a88c-140">Этот cmdlet создает канал для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1a88c-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1a88c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a88c-141">-Confirm</span></span>
<span data-ttu-id="1a88c-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a88c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a88c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a88c-143">-WhatIf</span></span>
<span data-ttu-id="1a88c-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a88c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a88c-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a88c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a88c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a88c-146">CommonParameters</span></span>
<span data-ttu-id="1a88c-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a88c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a88c-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a88c-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a88c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a88c-149">INPUTS</span></span>

### <span data-ttu-id="1a88c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1a88c-150">System.String</span></span>

### <span data-ttu-id="1a88c-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1a88c-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="1a88c-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a88c-152">OUTPUTS</span></span>

### <span data-ttu-id="1a88c-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1a88c-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="1a88c-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a88c-154">NOTES</span></span>
* <span data-ttu-id="1a88c-155">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="1a88c-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1a88c-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a88c-156">RELATED LINKS</span></span>

[<span data-ttu-id="1a88c-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1a88c-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="1a88c-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1a88c-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="1a88c-159">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1a88c-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="1a88c-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1a88c-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1a88c-161">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1a88c-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


