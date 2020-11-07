---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 87d4cfadd183a6aa2652b86336b4dc8d089936fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912847"
---
# <span data-ttu-id="f795d-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="f795d-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="f795d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f795d-102">SYNOPSIS</span></span>
  <span data-ttu-id="f795d-103">Вызывает конвейер, чтобы запустить его для запуска.</span><span class="sxs-lookup"><span data-stu-id="f795d-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="f795d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f795d-104">SYNTAX</span></span>

### <span data-ttu-id="f795d-105">ByFactoryNameByParameterFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f795d-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f795d-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="f795d-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f795d-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="f795d-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f795d-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="f795d-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f795d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f795d-109">DESCRIPTION</span></span>
<span data-ttu-id="f795d-110">Команда **Invoke-AzDataFactoryV2Pipeline** запускает выполнение в указанном конвейере и возвращает идентификатор для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f795d-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="f795d-111">Этот GUID можно передать в **Get-AzDataFactoryV2PipelineRun** или **Get-AzDataFactoryV2ActivityRun** , чтобы получить дополнительные сведения об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="f795d-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="f795d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f795d-112">EXAMPLES</span></span>

### <span data-ttu-id="f795d-113">Пример 1: вызов конвейера для начала выполнения</span><span class="sxs-lookup"><span data-stu-id="f795d-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="f795d-114">Эта команда начинает выполнение конвейера "DPWikisample" в фабрике "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="f795d-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="f795d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f795d-115">PARAMETERS</span></span>

### <span data-ttu-id="f795d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f795d-116">-DataFactoryName</span></span>
<span data-ttu-id="f795d-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f795d-117">The data factory name.</span></span>

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

### <span data-ttu-id="f795d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f795d-118">-DefaultProfile</span></span>
<span data-ttu-id="f795d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f795d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f795d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f795d-120">-InputObject</span></span>
<span data-ttu-id="f795d-121">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f795d-121">The data factory object.</span></span>

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

### <span data-ttu-id="f795d-122">-Параметр</span><span class="sxs-lookup"><span data-stu-id="f795d-122">-Parameter</span></span>
<span data-ttu-id="f795d-123">Параметры для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="f795d-123">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="f795d-124">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="f795d-124">-ParameterFile</span></span>
<span data-ttu-id="f795d-125">Имя файла с параметрами для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="f795d-125">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="f795d-126">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f795d-126">-PipelineName</span></span>
<span data-ttu-id="f795d-127">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="f795d-127">The pipeline name.</span></span>

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

### <span data-ttu-id="f795d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f795d-128">-ResourceGroupName</span></span>
<span data-ttu-id="f795d-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f795d-129">The resource group name.</span></span>

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

### <span data-ttu-id="f795d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f795d-130">-Confirm</span></span>
<span data-ttu-id="f795d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f795d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f795d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f795d-132">-WhatIf</span></span>
<span data-ttu-id="f795d-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="f795d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f795d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f795d-134">CommonParameters</span></span>
<span data-ttu-id="f795d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f795d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f795d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f795d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f795d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f795d-137">INPUTS</span></span>

### <span data-ttu-id="f795d-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f795d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="f795d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f795d-139">System.String</span></span>

### <span data-ttu-id="f795d-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f795d-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f795d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f795d-141">OUTPUTS</span></span>

### <span data-ttu-id="f795d-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f795d-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="f795d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f795d-143">NOTES</span></span>

## <span data-ttu-id="f795d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f795d-144">RELATED LINKS</span></span>

[<span data-ttu-id="f795d-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="f795d-145">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="f795d-146">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="f795d-146">Get-AzDataFactoryV2ActivityRun</span></span>]()

