---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232897"
---
# <span data-ttu-id="d8eb6-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d8eb6-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="d8eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8eb6-102">SYNOPSIS</span></span>
  <span data-ttu-id="d8eb6-103">Вызывает конвейер, чтобы запустить его.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="d8eb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8eb6-104">SYNTAX</span></span>

### <span data-ttu-id="d8eb6-105">ByFactoryNameByParameterFile (Default)</span><span class="sxs-lookup"><span data-stu-id="d8eb6-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8eb6-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="d8eb6-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8eb6-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="d8eb6-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8eb6-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="d8eb6-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8eb6-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8eb6-109">DESCRIPTION</span></span>
<span data-ttu-id="d8eb6-110">Команда **Invoke-AzDataFactoryV2Pipeline** запускает запуск в указанном канале и возвращает для этого запуска его ИД.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="d8eb6-111">Этот GUID можно передать **в Get-AzDataFactoryV2PipelineRun** или **Get-AzDataFactoryV2ActivityRun** для получения дополнительных сведений об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="d8eb6-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8eb6-112">EXAMPLES</span></span>

### <span data-ttu-id="d8eb6-113">Пример 1. Вызов конвейера для запуска запуска</span><span class="sxs-lookup"><span data-stu-id="d8eb6-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="d8eb6-114">Эта команда запускает запуск для конвейера DPWikisample на заводе "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="d8eb6-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="d8eb6-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8eb6-115">Example 2</span></span>

<span data-ttu-id="d8eb6-116">Вызывает конвейер, чтобы запустить его.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="d8eb6-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="d8eb6-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="d8eb6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8eb6-118">PARAMETERS</span></span>

### <span data-ttu-id="d8eb6-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8eb6-119">-DataFactoryName</span></span>
<span data-ttu-id="d8eb6-120">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-120">The data factory name.</span></span>

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

### <span data-ttu-id="d8eb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8eb6-121">-DefaultProfile</span></span>
<span data-ttu-id="d8eb6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8eb6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8eb6-123">-InputObject</span></span>
<span data-ttu-id="d8eb6-124">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-124">The data factory object.</span></span>

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

### <span data-ttu-id="d8eb6-125">-IsRecovery</span><span class="sxs-lookup"><span data-stu-id="d8eb6-125">-IsRecovery</span></span>
<span data-ttu-id="d8eb6-126">Флаг режима восстановления.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-126">Recovery mode flag.</span></span> <span data-ttu-id="d8eb6-127">Если для режима восстановления задано истинность, указанный канал, на который указывает ссылка, запустится, и новый запуск будет сгрупп указан в том же groupId.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eb6-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d8eb6-128">-Parameter</span></span>
<span data-ttu-id="d8eb6-129">Параметры для запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="d8eb6-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="d8eb6-130">-ParameterFile</span></span>
<span data-ttu-id="d8eb6-131">Имя файла с параметрами для запуска конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="d8eb6-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="d8eb6-132">-PipelineName</span></span>
<span data-ttu-id="d8eb6-133">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-133">The pipeline name.</span></span>

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

### <span data-ttu-id="d8eb6-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="d8eb6-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="d8eb6-135">Повторно запустится ИД конвейера.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="d8eb6-136">Если задан ИД запуска, для создания нового запуска будут использоваться параметры указанного запуска.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eb6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8eb6-137">-ResourceGroupName</span></span>
<span data-ttu-id="d8eb6-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-138">The resource group name.</span></span>

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

### <span data-ttu-id="d8eb6-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="d8eb6-139">-StartActivityName</span></span>
<span data-ttu-id="d8eb6-140">В режиме восстановления повторное запуск будет начинаться с этого действия.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="d8eb6-141">Если не указано, будут выполниться все действия.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-141">If not specified, all activities will run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eb6-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="d8eb6-142">-StartFromFailure</span></span>
<span data-ttu-id="d8eb6-143">Запуск повторного запуска из флага сбойных действий.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="d8eb6-144">В режиме восстановления, если задан этот режим, повторное запуск будет начинаться из сбойных действий.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8eb6-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8eb6-145">-Confirm</span></span>
<span data-ttu-id="d8eb6-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8eb6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8eb6-147">-WhatIf</span></span>
<span data-ttu-id="d8eb6-148">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d8eb6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8eb6-149">CommonParameters</span></span>
<span data-ttu-id="d8eb6-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8eb6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8eb6-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8eb6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8eb6-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8eb6-152">INPUTS</span></span>

### <span data-ttu-id="d8eb6-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d8eb6-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="d8eb6-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d8eb6-154">System.String</span></span>

### <span data-ttu-id="d8eb6-155">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8eb6-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8eb6-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8eb6-156">OUTPUTS</span></span>

### <span data-ttu-id="d8eb6-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d8eb6-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="d8eb6-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8eb6-158">NOTES</span></span>

## <span data-ttu-id="d8eb6-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8eb6-159">RELATED LINKS</span></span>

[<span data-ttu-id="d8eb6-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="d8eb6-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="d8eb6-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="d8eb6-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

