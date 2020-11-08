---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076009"
---
# <span data-ttu-id="f8f5a-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8f5a-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="f8f5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f5a-103">Определяет новое задание MapReduce для потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="f8f5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8f5a-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f8f5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f5a-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f8f5a-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f8f5a-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f8f5a-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f8f5a-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f8f5a-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f8f5a-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f8f5a-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8f5a-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f8f5a-112">Командлет **New-AzureHDInsightStreamingMapReduceJobDefinition** определяет новый объект определения задания, который представляет параметры задания потоковой передачи Hadoop.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="f8f5a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8f5a-113">EXAMPLES</span></span>

### <span data-ttu-id="f8f5a-114">Пример 1: Создание определения задания для потоковой MapReduce</span><span class="sxs-lookup"><span data-stu-id="f8f5a-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="f8f5a-115">Эта команда создает указанное определение задания для потоковой передачи (MapReduce) и сохраняет его в переменной $StreamingWordCount.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="f8f5a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8f5a-116">PARAMETERS</span></span>

### <span data-ttu-id="f8f5a-117">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="f8f5a-117">-Arguments</span></span>
<span data-ttu-id="f8f5a-118">Задает массив аргументов для задания Hadoop.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="f8f5a-119">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="f8f5a-120">-CmdEnv</span></span>
<span data-ttu-id="f8f5a-121">Задает массив переменных среды командной строки, которые должны быть заданы при запуске задания на узлах данных.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-122">-Combine</span><span class="sxs-lookup"><span data-stu-id="f8f5a-122">-Combiner</span></span>
<span data-ttu-id="f8f5a-123">Указывает имя файла для объединения.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-124">-Определение</span><span class="sxs-lookup"><span data-stu-id="f8f5a-124">-Defines</span></span>
<span data-ttu-id="f8f5a-125">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-126">-Файлы</span><span class="sxs-lookup"><span data-stu-id="f8f5a-126">-Files</span></span>
<span data-ttu-id="f8f5a-127">Задает массив файлов, необходимых для задания.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="f8f5a-128">-InputPath</span></span>
<span data-ttu-id="f8f5a-129">Указывает путь WASB к входным файлам.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="f8f5a-130">-JobName</span></span>
<span data-ttu-id="f8f5a-131">Указывает имя нового определения задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="f8f5a-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-133">-Сопоставитель</span><span class="sxs-lookup"><span data-stu-id="f8f5a-133">-Mapper</span></span>
<span data-ttu-id="f8f5a-134">Указывает имя файла сопоставителя.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f8f5a-135">-OutputPath</span></span>
<span data-ttu-id="f8f5a-136">Указывает путь WASB для выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="f8f5a-137">-Profile</span></span>
<span data-ttu-id="f8f5a-138">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f8f5a-139">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-140">-Reduce</span><span class="sxs-lookup"><span data-stu-id="f8f5a-140">-Reducer</span></span>
<span data-ttu-id="f8f5a-141">Указывает имя файла сокращения.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f8f5a-142">-StatusFolder</span></span>
<span data-ttu-id="f8f5a-143">Указывает папку, в которой содержатся стандартные выходные данные и выходные ошибки для задания, включая код завершения и журналы задач.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f5a-144">CommonParameters</span></span>
<span data-ttu-id="f8f5a-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8f5a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f5a-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f5a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f5a-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8f5a-147">INPUTS</span></span>

## <span data-ttu-id="f8f5a-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8f5a-148">OUTPUTS</span></span>

## <span data-ttu-id="f8f5a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8f5a-149">NOTES</span></span>

## <span data-ttu-id="f8f5a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8f5a-150">RELATED LINKS</span></span>

[<span data-ttu-id="f8f5a-151">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8f5a-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f8f5a-152">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8f5a-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="f8f5a-153">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8f5a-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="f8f5a-154">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f8f5a-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


