---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: A8953045-3836-4C5A-96F8-461CB1DB6BBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58958a6bedd29cd55535fe879fab813a430ff20b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075916"
---
# <span data-ttu-id="3d210-101">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3d210-101">New-AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="3d210-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d210-102">SYNOPSIS</span></span>
<span data-ttu-id="3d210-103">Определение нового задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="3d210-103">Defines a new MapReduce job.</span></span>

## <span data-ttu-id="3d210-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d210-104">SYNTAX</span></span>

```
New-AzureHDInsightMapReduceJobDefinition [-Arguments <String[]>] -ClassName <String> [-Defines <Hashtable>]
 [-Files <String[]>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d210-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d210-105">DESCRIPTION</span></span>
<span data-ttu-id="3d210-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="3d210-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3d210-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="3d210-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3d210-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3d210-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3d210-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="3d210-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3d210-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="3d210-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3d210-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3d210-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3d210-112">Командлет **New-AzureHDInsightMapReduceJobDefinition** определяет новое задание MapReduce для работы в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="3d210-112">The **New-AzureHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job to run on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3d210-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d210-113">EXAMPLES</span></span>

### <span data-ttu-id="3d210-114">Пример 1: определение задания MapReduce, выполнение задания и получение выходных данных</span><span class="sxs-lookup"><span data-stu-id="3d210-114">Example 1: Define a MapReduce job, run the job, and get the output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "WordCount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="3d210-115">Первая команда получает идентификатор текущей подписки, а затем сохраняет ее в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="3d210-115">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="3d210-116">Вторая команда назначает имя MyCluster переменной $Clustername.</span><span class="sxs-lookup"><span data-stu-id="3d210-116">The second command assigns the name MyCluster to the $Clustername variable.</span></span>

<span data-ttu-id="3d210-117">Третья команда использует командлет **New-AzureHDInsightMapReduceJobDefinition** , чтобы создать определение задания MapReduce, а затем сохранить его в переменной $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="3d210-117">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then store it in the $WordCountJob variable.</span></span>

<span data-ttu-id="3d210-118">Четвертая команда выполняет последовательность операций, используя следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="3d210-118">The fourth command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="3d210-119">**Start-AzureHDInsightJob** для запуска задания на $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="3d210-119">**Start-AzureHDInsightJob** to start the job on $ClusterName.</span></span> 
- <span data-ttu-id="3d210-120">**AzureHDInsightJob ожидания —** дождитесь завершения задания и отобразите ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="3d210-120">**Wait-AzureHDInsightJob** to wait for the job to finish and to display the progress toward completion.</span></span>
- <span data-ttu-id="3d210-121">**Get-AzureHDInsightJobOutput** для получения выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="3d210-121">**Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="3d210-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d210-122">PARAMETERS</span></span>

### <span data-ttu-id="3d210-123">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="3d210-123">-Arguments</span></span>
<span data-ttu-id="3d210-124">Задает массив аргументов для задания Hadoop.</span><span class="sxs-lookup"><span data-stu-id="3d210-124">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="3d210-125">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="3d210-125">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="3d210-126">-ClassName</span><span class="sxs-lookup"><span data-stu-id="3d210-126">-ClassName</span></span>
<span data-ttu-id="3d210-127">Указывает имя класса задания в файле архива Java (JAR).</span><span class="sxs-lookup"><span data-stu-id="3d210-127">Specifies the name of the job class in the Java Archive (JAR) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Class

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d210-128">-Определение</span><span class="sxs-lookup"><span data-stu-id="3d210-128">-Defines</span></span>
<span data-ttu-id="3d210-129">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="3d210-129">Specifies Hadoop configuration values to set when the job runs.</span></span>

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

### <span data-ttu-id="3d210-130">-Файлы</span><span class="sxs-lookup"><span data-stu-id="3d210-130">-Files</span></span>
<span data-ttu-id="3d210-131">Задает массив файлов WASB, необходимых для задания.</span><span class="sxs-lookup"><span data-stu-id="3d210-131">Specifies an array of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="3d210-132">-JarFile</span><span class="sxs-lookup"><span data-stu-id="3d210-132">-JarFile</span></span>
<span data-ttu-id="3d210-133">Указывает полное имя JAR-файла, который содержит код и зависимости задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="3d210-133">Specifies the fully qualified name of a JAR file that contains the code and dependencies of a MapReduce job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Jar

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d210-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="3d210-134">-JobName</span></span>
<span data-ttu-id="3d210-135">Указывает имя задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="3d210-135">Specifies the name of a MapReduce job.</span></span>
<span data-ttu-id="3d210-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3d210-136">This parameter is optional.</span></span>
<span data-ttu-id="3d210-137">Если этот параметр не указан, используется значение параметра *className* .</span><span class="sxs-lookup"><span data-stu-id="3d210-137">If you do not specify this parameter, the value of the *ClassName* parameter is used.</span></span>

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

### <span data-ttu-id="3d210-138">-LibJars</span><span class="sxs-lookup"><span data-stu-id="3d210-138">-LibJars</span></span>
<span data-ttu-id="3d210-139">Задает массив ссылок LibJar для задания.</span><span class="sxs-lookup"><span data-stu-id="3d210-139">Specifies an array of LibJar references of the job.</span></span>

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

### <span data-ttu-id="3d210-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d210-140">-Profile</span></span>
<span data-ttu-id="3d210-141">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3d210-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d210-142">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d210-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d210-143">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3d210-143">-StatusFolder</span></span>
<span data-ttu-id="3d210-144">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания, включая код завершения и журналы задач.</span><span class="sxs-lookup"><span data-stu-id="3d210-144">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="3d210-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d210-145">CommonParameters</span></span>
<span data-ttu-id="3d210-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d210-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d210-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d210-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d210-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d210-148">INPUTS</span></span>

## <span data-ttu-id="3d210-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d210-149">OUTPUTS</span></span>

## <span data-ttu-id="3d210-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d210-150">NOTES</span></span>

## <span data-ttu-id="3d210-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d210-151">RELATED LINKS</span></span>

[<span data-ttu-id="3d210-152">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="3d210-152">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="3d210-153">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3d210-153">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="3d210-154">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3d210-154">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="3d210-155">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3d210-155">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="3d210-156">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3d210-156">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="3d210-157">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3d210-157">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


