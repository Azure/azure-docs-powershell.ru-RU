---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: e7bfd0b72f5dffe4e5ff4d7e52394846d5f17afa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560968"
---
# <span data-ttu-id="51950-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="51950-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="51950-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51950-102">SYNOPSIS</span></span>
  <span data-ttu-id="51950-103">Вызывает конвейер, чтобы запустить его для запуска.</span><span class="sxs-lookup"><span data-stu-id="51950-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51950-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51950-104">SYNTAX</span></span>

### <span data-ttu-id="51950-105">ByFactoryNameByParameterFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51950-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51950-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="51950-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51950-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="51950-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51950-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="51950-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51950-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51950-109">DESCRIPTION</span></span>
<span data-ttu-id="51950-110">Команда **Invoke-AzureRmDataFactoryV2Pipeline** запускает выполнение в указанном конвейере и возвращает идентификатор для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="51950-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="51950-111">Этот GUID можно передать в **Get-AzureRmDataFactoryV2PipelineRun** или **Get-AzureRmDataFactoryV2ActivityRun** , чтобы получить дополнительные сведения об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="51950-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="51950-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51950-112">EXAMPLES</span></span>

### <span data-ttu-id="51950-113">Пример 1: вызов конвейера для начала выполнения</span><span class="sxs-lookup"><span data-stu-id="51950-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="51950-114">Эта команда начинает выполнение конвейера "DPWikisample" в фабрике "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="51950-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="51950-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51950-115">PARAMETERS</span></span>

### <span data-ttu-id="51950-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="51950-116">-DataFactoryName</span></span>
<span data-ttu-id="51950-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="51950-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51950-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51950-118">-DefaultProfile</span></span>
<span data-ttu-id="51950-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51950-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51950-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51950-120">-InputObject</span></span>
<span data-ttu-id="51950-121">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="51950-121">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51950-122">-Параметр</span><span class="sxs-lookup"><span data-stu-id="51950-122">-Parameter</span></span>
<span data-ttu-id="51950-123">Параметры для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="51950-123">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51950-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="51950-124">-ParameterFile</span></span>
<span data-ttu-id="51950-125">Имя файла с параметрами для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="51950-125">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51950-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="51950-126">-PipelineName</span></span>
<span data-ttu-id="51950-127">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="51950-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51950-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51950-128">-ResourceGroupName</span></span>
<span data-ttu-id="51950-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51950-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51950-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51950-130">-Confirm</span></span>
<span data-ttu-id="51950-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51950-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51950-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51950-132">-WhatIf</span></span>
<span data-ttu-id="51950-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="51950-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="51950-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51950-134">CommonParameters</span></span>
<span data-ttu-id="51950-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51950-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51950-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51950-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51950-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51950-137">INPUTS</span></span>

### <span data-ttu-id="51950-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="51950-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="51950-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="51950-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="51950-140">System. String</span><span class="sxs-lookup"><span data-stu-id="51950-140">System.String</span></span>

### <span data-ttu-id="51950-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="51950-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51950-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51950-142">OUTPUTS</span></span>

### <span data-ttu-id="51950-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="51950-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="51950-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="51950-144">NOTES</span></span>

## <span data-ttu-id="51950-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51950-145">RELATED LINKS</span></span>

[<span data-ttu-id="51950-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="51950-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="51950-147">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="51950-147">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

