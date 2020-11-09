---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: e4204068b12a21732cca1802dcc20a770d74d5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313970"
---
# <span data-ttu-id="e1ee9-101">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="e1ee9-101">Invoke-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="e1ee9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1ee9-102">SYNOPSIS</span></span>
  <span data-ttu-id="e1ee9-103">Вызывает конвейер, чтобы запустить его для запуска.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="e1ee9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1ee9-104">SYNTAX</span></span>

### <span data-ttu-id="e1ee9-105">ByFactoryNameByParameterFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1ee9-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ee9-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1ee9-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ee9-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1ee9-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>]
 [[-ReferencePipelineRunId] <String>] [-IsRecovery] [[-StartActivityName] <String>] [-StartFromFailure]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ee9-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1ee9-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [[-ReferencePipelineRunId] <String>] [-IsRecovery]
 [[-StartActivityName] <String>] [-StartFromFailure] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ee9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1ee9-109">DESCRIPTION</span></span>
<span data-ttu-id="e1ee9-110">Команда **Invoke-AzDataFactoryV2Pipeline** запускает выполнение в указанном конвейере и возвращает идентификатор для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-110">The **Invoke-AzDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="e1ee9-111">Этот GUID можно передать в **Get-AzDataFactoryV2PipelineRun** или **Get-AzDataFactoryV2ActivityRun** , чтобы получить дополнительные сведения об этом запуске.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-111">This GUID can be passed to **Get-AzDataFactoryV2PipelineRun** or **Get-AzDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="e1ee9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1ee9-112">EXAMPLES</span></span>

### <span data-ttu-id="e1ee9-113">Пример 1: вызов конвейера для начала выполнения</span><span class="sxs-lookup"><span data-stu-id="e1ee9-113">Example 1: Invoke a pipeline to start a run</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="e1ee9-114">Эта команда начинает выполнение конвейера "DPWikisample" в фабрике "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="e1ee9-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

### <span data-ttu-id="e1ee9-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e1ee9-115">Example 2</span></span>

<span data-ttu-id="e1ee9-116">Вызывает конвейер, чтобы запустить его для запуска.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-116">Invokes a pipeline to start a run for it.</span></span> <span data-ttu-id="e1ee9-117">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="e1ee9-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Invoke-AzDataFactoryV2Pipeline -DataFactoryName 'WikiADF' -Parameter <Hashtable> -PipelineName 'DPWikisample' -ResourceGroupName 'ADF'
```

## <span data-ttu-id="e1ee9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1ee9-118">PARAMETERS</span></span>

### <span data-ttu-id="e1ee9-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e1ee9-119">-DataFactoryName</span></span>
<span data-ttu-id="e1ee9-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-120">The data factory name.</span></span>

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

### <span data-ttu-id="e1ee9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ee9-121">-DefaultProfile</span></span>
<span data-ttu-id="e1ee9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ee9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1ee9-123">-InputObject</span></span>
<span data-ttu-id="e1ee9-124">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-124">The data factory object.</span></span>

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

### <span data-ttu-id="e1ee9-125">-NORECOVERY</span><span class="sxs-lookup"><span data-stu-id="e1ee9-125">-IsRecovery</span></span>
<span data-ttu-id="e1ee9-126">Флаг режима восстановления.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-126">Recovery mode flag.</span></span> <span data-ttu-id="e1ee9-127">Если для режима восстановления установлено значение true, выполнение указанного конвейера, на который указывает ссылка, и новый прогон будут сгруппированы в том же элементе groupId.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

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

### <span data-ttu-id="e1ee9-128">-Параметр</span><span class="sxs-lookup"><span data-stu-id="e1ee9-128">-Parameter</span></span>
<span data-ttu-id="e1ee9-129">Параметры для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-129">Parameters for pipeline run.</span></span>

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

### <span data-ttu-id="e1ee9-130">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1ee9-130">-ParameterFile</span></span>
<span data-ttu-id="e1ee9-131">Имя файла с параметрами для выполнения конвейера.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="e1ee9-132">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="e1ee9-132">-PipelineName</span></span>
<span data-ttu-id="e1ee9-133">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-133">The pipeline name.</span></span>

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

### <span data-ttu-id="e1ee9-134">-ReferencePipelineRunId</span><span class="sxs-lookup"><span data-stu-id="e1ee9-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="e1ee9-135">Идентификатор запускаемого конвейера для повторного выполнения.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-135">The pipeline run ID for rerun.</span></span> <span data-ttu-id="e1ee9-136">Если указан идентификатор запуска, для создания нового запуска будут использоваться параметры указанного запуска.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="e1ee9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ee9-137">-ResourceGroupName</span></span>
<span data-ttu-id="e1ee9-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-138">The resource group name.</span></span>

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

### <span data-ttu-id="e1ee9-139">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="e1ee9-139">-StartActivityName</span></span>
<span data-ttu-id="e1ee9-140">В режиме восстановления повторный запуск начнется с этого действия.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-140">In recovery mode, the rerun will start from this activity.</span></span> <span data-ttu-id="e1ee9-141">Если не указано, будут запущены все действия.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-141">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="e1ee9-142">-StartFromFailure</span><span class="sxs-lookup"><span data-stu-id="e1ee9-142">-StartFromFailure</span></span>
<span data-ttu-id="e1ee9-143">Запустите повторный запуск из флага неудачных действий.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-143">Start rerun from failed activities flag.</span></span> <span data-ttu-id="e1ee9-144">В режиме восстановления, если оно задано, повторное выполнение начинается с невыполненных действий.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-144">In recovery mode, if specified, the rerun will start from failed activities.</span></span>

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

### <span data-ttu-id="e1ee9-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1ee9-145">-Confirm</span></span>
<span data-ttu-id="e1ee9-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ee9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ee9-147">-WhatIf</span></span>
<span data-ttu-id="e1ee9-148">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-148">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e1ee9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ee9-149">CommonParameters</span></span>
<span data-ttu-id="e1ee9-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1ee9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ee9-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1ee9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ee9-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1ee9-152">INPUTS</span></span>

### <span data-ttu-id="e1ee9-153">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e1ee9-153">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="e1ee9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ee9-154">System.String</span></span>

### <span data-ttu-id="e1ee9-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1ee9-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1ee9-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1ee9-156">OUTPUTS</span></span>

### <span data-ttu-id="e1ee9-157">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="e1ee9-157">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="e1ee9-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1ee9-158">NOTES</span></span>

## <span data-ttu-id="e1ee9-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1ee9-159">RELATED LINKS</span></span>

[<span data-ttu-id="e1ee9-160">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="e1ee9-160">Get-AzDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="e1ee9-161">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="e1ee9-161">Get-AzDataFactoryV2ActivityRun</span></span>]()

