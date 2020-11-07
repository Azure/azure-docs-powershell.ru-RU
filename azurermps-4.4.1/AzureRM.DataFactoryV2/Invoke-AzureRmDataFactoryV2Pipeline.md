---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734074"
---
# <span data-ttu-id="35ca3-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="35ca3-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="35ca3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35ca3-102">SYNOPSIS</span></span>
  <span data-ttu-id="35ca3-103">Вызывает конвейер, чтобы запустить его для запуска.</span><span class="sxs-lookup"><span data-stu-id="35ca3-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35ca3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35ca3-104">SYNTAX</span></span>

### <span data-ttu-id="35ca3-105">ByFactoryNameByParameterFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35ca3-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="35ca3-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="35ca3-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="35ca3-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="35ca3-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="35ca3-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="35ca3-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="35ca3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ca3-109">DESCRIPTION</span></span>
<span data-ttu-id="35ca3-110">Команда **Invoke-AzureRmDataFactoryV2Pipeline** запускает выполнение в указанном конвейере и возвращает идентификатор для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="35ca3-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="35ca3-111">Этот GUID можно передать в **Get-AzureRmDataFactoryV2PipelineRun** или **Get-AzureRmDataFactoryV2ActivityRun** , чтобы получить дополнительные сведения об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="35ca3-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="35ca3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35ca3-112">EXAMPLES</span></span>

### <span data-ttu-id="35ca3-113">Пример 1: вызов конвейера для начала выполнения</span><span class="sxs-lookup"><span data-stu-id="35ca3-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="35ca3-114">Эта команда начинает выполнение конвейера "DPWikisample" в фабрике "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="35ca3-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="35ca3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35ca3-115">PARAMETERS</span></span>

### <span data-ttu-id="35ca3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35ca3-116">-Confirm</span></span>
<span data-ttu-id="35ca3-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35ca3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ca3-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="35ca3-118">-DataFactoryName</span></span>
<span data-ttu-id="35ca3-119">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="35ca3-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca3-120">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="35ca3-120">-ParameterFile</span></span>
<span data-ttu-id="35ca3-121">Имя файла с параметрами для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="35ca3-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca3-122">-Параметр</span><span class="sxs-lookup"><span data-stu-id="35ca3-122">-Parameter</span></span>
<span data-ttu-id="35ca3-123">Параметры для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="35ca3-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35ca3-124">-InputObject</span></span>
<span data-ttu-id="35ca3-125">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="35ca3-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca3-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="35ca3-126">-PipelineName</span></span>
<span data-ttu-id="35ca3-127">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="35ca3-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ca3-128">-ResourceGroupName</span></span>
<span data-ttu-id="35ca3-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35ca3-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35ca3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ca3-130">-WhatIf</span></span>
<span data-ttu-id="35ca3-131">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="35ca3-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="35ca3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35ca3-132">INPUTS</span></span>

### <span data-ttu-id="35ca3-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="35ca3-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="35ca3-134">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="35ca3-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="35ca3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ca3-135">OUTPUTS</span></span>

### <span data-ttu-id="35ca3-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="35ca3-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="35ca3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="35ca3-137">NOTES</span></span>

## <span data-ttu-id="35ca3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ca3-138">RELATED LINKS</span></span>
[<span data-ttu-id="35ca3-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="35ca3-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="35ca3-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="35ca3-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

