---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507914"
---
# <span data-ttu-id="53424-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="53424-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="53424-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53424-102">SYNOPSIS</span></span>
<span data-ttu-id="53424-103">Отправка задания synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="53424-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="53424-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53424-104">SYNTAX</span></span>

### <span data-ttu-id="53424-105">RunSparkJobParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53424-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53424-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53424-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53424-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53424-107">DESCRIPTION</span></span>
<span data-ttu-id="53424-108">Cmdlet **Submit-AzSynapseSparkJob** передает задание Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="53424-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="53424-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53424-109">EXAMPLES</span></span>

### <span data-ttu-id="53424-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53424-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="53424-111">Эта команда представляет задание synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="53424-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="53424-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="53424-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="53424-113">Эта команда представляет задание Synapse Analytics Spark .NET.</span><span class="sxs-lookup"><span data-stu-id="53424-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="53424-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="53424-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="53424-115">Эта команда представляет задание Synapse Analytics PySpark.</span><span class="sxs-lookup"><span data-stu-id="53424-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="53424-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53424-116">PARAMETERS</span></span>

### <span data-ttu-id="53424-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="53424-117">-CommandLineArgument</span></span>
<span data-ttu-id="53424-118">Необязательные аргументы задания.</span><span class="sxs-lookup"><span data-stu-id="53424-118">Optional arguments to the job.</span></span> <span data-ttu-id="53424-119">Например, "--итерация 10 000 — время:20".</span><span class="sxs-lookup"><span data-stu-id="53424-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="53424-120">-Configuration</span></span>
<span data-ttu-id="53424-121">Свойства конфигурации спарк.</span><span class="sxs-lookup"><span data-stu-id="53424-121">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53424-122">-DefaultProfile</span></span>
<span data-ttu-id="53424-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53424-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53424-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="53424-124">-ExecutorCount</span></span>
<span data-ttu-id="53424-125">Количество исполнятелей, которые должны быть выделены в указанном пуле спарков для задания.</span><span class="sxs-lookup"><span data-stu-id="53424-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="53424-126">-ExecutorSize</span></span>
<span data-ttu-id="53424-127">Количество ядра и памяти, используемых для исполнятелей, выделенных в указанном пуле спарков для задания.</span><span class="sxs-lookup"><span data-stu-id="53424-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-128">-Language</span><span class="sxs-lookup"><span data-stu-id="53424-128">-Language</span></span>
<span data-ttu-id="53424-129">Язык задания, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="53424-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="53424-130">-MainClassName</span></span>
<span data-ttu-id="53424-131">Полное идентификатор или основной класс в основном файле определения.</span><span class="sxs-lookup"><span data-stu-id="53424-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="53424-132">Требуется для задания "Спарк" и .NET Spark.</span><span class="sxs-lookup"><span data-stu-id="53424-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="53424-133">Пример: org.apache.spark.examples.SparkPi.</span><span class="sxs-lookup"><span data-stu-id="53424-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="53424-134">-MainDefinitionFile</span></span>
<span data-ttu-id="53424-135">Основной файл, используемый для задания.</span><span class="sxs-lookup"><span data-stu-id="53424-135">The main file used for the job.</span></span>
<span data-ttu-id="53424-136">Например, abfss://filesystem@account.dfs.core.windows.net/mySpark.jar ""</span><span class="sxs-lookup"><span data-stu-id="53424-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-137">-Name</span><span class="sxs-lookup"><span data-stu-id="53424-137">-Name</span></span>
<span data-ttu-id="53424-138">Имя задания "Спарк".</span><span class="sxs-lookup"><span data-stu-id="53424-138">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="53424-139">-ReferenceFile</span></span>
<span data-ttu-id="53424-140">Дополнительные файлы, используемые для справки в основном файле определения.</span><span class="sxs-lookup"><span data-stu-id="53424-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="53424-141">Список URI хранилища с разделами-запятой.</span><span class="sxs-lookup"><span data-stu-id="53424-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="53424-142">Например, abfss://filesystem@account.dfs.core.windows.net/file1.txt ", abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="53424-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="53424-143">-SparkPoolName</span></span>
<span data-ttu-id="53424-144">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="53424-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="53424-145">-SparkPoolObject</span></span>
<span data-ttu-id="53424-146">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="53424-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53424-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53424-147">-WorkspaceName</span></span>
<span data-ttu-id="53424-148">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="53424-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53424-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53424-149">-Confirm</span></span>
<span data-ttu-id="53424-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53424-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53424-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53424-151">-WhatIf</span></span>
<span data-ttu-id="53424-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53424-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53424-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53424-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53424-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53424-154">CommonParameters</span></span>
<span data-ttu-id="53424-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53424-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53424-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53424-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53424-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53424-157">INPUTS</span></span>

### <span data-ttu-id="53424-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="53424-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="53424-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53424-159">OUTPUTS</span></span>

### <span data-ttu-id="53424-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="53424-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="53424-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53424-161">NOTES</span></span>

## <span data-ttu-id="53424-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53424-162">RELATED LINKS</span></span>