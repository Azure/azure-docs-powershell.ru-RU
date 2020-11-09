---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryPipeline.md
ms.openlocfilehash: e8917b9c68cb0708d34faa0e0dfec8e0e912f54b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313913"
---
# <span data-ttu-id="a72c9-101">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a72c9-101">New-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="a72c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a72c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a72c9-103">Создание конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="a72c9-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="a72c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a72c9-104">SYNTAX</span></span>

### <span data-ttu-id="a72c9-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a72c9-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a72c9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a72c9-106">ByFactoryObject</span></span>
```
New-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a72c9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a72c9-107">DESCRIPTION</span></span>
<span data-ttu-id="a72c9-108">Командлет **New-AzDataFactoryPipeline** создает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a72c9-108">The **New-AzDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="a72c9-109">Если указать имя для конвейера, который уже существует, командлет запрашивает подтверждение перед заменой конвейера.</span><span class="sxs-lookup"><span data-stu-id="a72c9-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="a72c9-110">Если указан параметр *Force* , командлет заменяет существующий конвейер без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a72c9-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="a72c9-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a72c9-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="a72c9-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a72c9-112">Create a data factory.</span></span> 
- <span data-ttu-id="a72c9-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="a72c9-113">Create linked services.</span></span> 
- <span data-ttu-id="a72c9-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="a72c9-114">Create datasets.</span></span> 
- <span data-ttu-id="a72c9-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="a72c9-115">Create a pipeline.</span></span>
<span data-ttu-id="a72c9-116">Если конвейер с таким именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписывать существующий конвейер с помощью нового конвейера.</span><span class="sxs-lookup"><span data-stu-id="a72c9-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="a72c9-117">Если вы подтвердите перезапись существующего конвейера, определение конвейера также заменяется.</span><span class="sxs-lookup"><span data-stu-id="a72c9-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="a72c9-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a72c9-118">EXAMPLES</span></span>

### <span data-ttu-id="a72c9-119">Пример 1: создание конвейера</span><span class="sxs-lookup"><span data-stu-id="a72c9-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="a72c9-120">Эта команда создает конвейер с именем DPWikisample в фабрике данных с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="a72c9-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="a72c9-121">Команда основывается на сведениях в DPWikisample.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="a72c9-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="a72c9-122">Этот файл содержит сведения о действиях, таких как копирование и действия по HDInsight в конвейере.</span><span class="sxs-lookup"><span data-stu-id="a72c9-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="a72c9-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a72c9-123">PARAMETERS</span></span>

### <span data-ttu-id="a72c9-124">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="a72c9-124">-DataFactory</span></span>
<span data-ttu-id="a72c9-125">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a72c9-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a72c9-126">Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a72c9-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a72c9-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a72c9-127">-DataFactoryName</span></span>
<span data-ttu-id="a72c9-128">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="a72c9-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a72c9-129">Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a72c9-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a72c9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72c9-130">-DefaultProfile</span></span>
<span data-ttu-id="a72c9-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a72c9-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a72c9-132">-Файл</span><span class="sxs-lookup"><span data-stu-id="a72c9-132">-File</span></span>
<span data-ttu-id="a72c9-133">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание конвейера.</span><span class="sxs-lookup"><span data-stu-id="a72c9-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

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

### <span data-ttu-id="a72c9-134">-Force</span><span class="sxs-lookup"><span data-stu-id="a72c9-134">-Force</span></span>
<span data-ttu-id="a72c9-135">Указывает на то, что этот командлет заменяет существующий конвейер без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a72c9-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a72c9-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a72c9-136">-Name</span></span>
<span data-ttu-id="a72c9-137">Указывает имя создаваемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="a72c9-137">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="a72c9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72c9-138">-ResourceGroupName</span></span>
<span data-ttu-id="a72c9-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a72c9-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a72c9-140">Этот командлет создает конвейер для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a72c9-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a72c9-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a72c9-141">-Confirm</span></span>
<span data-ttu-id="a72c9-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a72c9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a72c9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a72c9-143">-WhatIf</span></span>
<span data-ttu-id="a72c9-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a72c9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a72c9-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a72c9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a72c9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72c9-146">CommonParameters</span></span>
<span data-ttu-id="a72c9-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a72c9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72c9-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a72c9-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72c9-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a72c9-149">INPUTS</span></span>

### <span data-ttu-id="a72c9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a72c9-150">System.String</span></span>

### <span data-ttu-id="a72c9-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a72c9-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a72c9-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a72c9-152">OUTPUTS</span></span>

### <span data-ttu-id="a72c9-153">Microsoft. Azure. Commands. Factoring. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a72c9-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="a72c9-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="a72c9-154">NOTES</span></span>
* <span data-ttu-id="a72c9-155">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="a72c9-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a72c9-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a72c9-156">RELATED LINKS</span></span>

[<span data-ttu-id="a72c9-157">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a72c9-157">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="a72c9-158">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a72c9-158">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="a72c9-159">Возобновить — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a72c9-159">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="a72c9-160">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a72c9-160">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="a72c9-161">Приостановить — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a72c9-161">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


