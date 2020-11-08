---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0B194605-F6B2-4FBC-ABF8-E49876EC7CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b215cfa95c20a2e8d13cfefa9e2ef0b3794a6727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075640"
---
# <span data-ttu-id="fb9ab-101">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="fb9ab-101">Get-AzureHDInsightJobOutput</span></span>

## <span data-ttu-id="fb9ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9ab-103">Получает выходные данные журнала для задания.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-103">Gets the log output for a job.</span></span>

## <span data-ttu-id="fb9ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb9ab-104">SYNTAX</span></span>

```
Get-AzureHDInsightJobOutput [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-DownloadTaskLogs] [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-StandardError]
 [-StandardOutput] [-Subscription <String>] [-TaskLogsDirectory <String>] [-TaskSummary]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fb9ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="fb9ab-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="fb9ab-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="fb9ab-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="fb9ab-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров на базе Linux в [HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="fb9ab-109">For information about how to use the new HDInsight to create a cluster, see Create Linux-based clusters in [HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="fb9ab-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="fb9ab-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="fb9ab-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb9ab-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="fb9ab-112">Командлет **Get-AzureHDInsightJobOutput** получает выходные данные журнала для задания из учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-112">The **Get-AzureHDInsightJobOutput** cmdlet gets the log output for a job from the storage account associated with a cluster.</span></span>
<span data-ttu-id="fb9ab-113">Вы можете получать различные типы журналов заданий, включая стандартный вывод, стандартную ошибку, журналы задач и сводку по журналам задач.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-113">You can get various types of job logs including standard output, standard error, task logs, and a summary of the task logs.</span></span>

## <span data-ttu-id="fb9ab-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb9ab-114">EXAMPLES</span></span>

### <span data-ttu-id="fb9ab-115">Пример 1: получение выходных данных задания</span><span class="sxs-lookup"><span data-stu-id="fb9ab-115">Example 1: Get job output</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "MyCluster"
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" $WordCountJob
    | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -StandardError
```

<span data-ttu-id="fb9ab-116">Первая команда получает идентификатор текущей подписки, а затем сохраняет ее в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-116">The first command gets the ID of the current subscription, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="fb9ab-117">Вторая команда сохраняет имя MyCluster в переменной $Clustername.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-117">The second command stores the name MyCluster in the $Clustername variable.</span></span>

<span data-ttu-id="fb9ab-118">Третья команда создает определение задания MapReduce и сохраняет его в переменной $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-118">The third command creates a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>
<span data-ttu-id="fb9ab-119">Команда передает задание в $WordCountJob командлету **Start-AzureHDInsightJob** , чтобы запустить задание.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-119">The command passes the job in $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="fb9ab-120">Кроме того, он передает $WordCountJob командлету **Wait-AzureHDInsightJob** , чтобы дождаться завершения задания, а затем использует **Get-AzureHDInsightJobOutput** для получения выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-120">It also passes $WordCountJob to the **Wait-AzureHDInsightJob** cmdlet to wait for the job to finish, and then it uses **Get-AzureHDInsightJobOutput** to get the job output.</span></span>

## <span data-ttu-id="fb9ab-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb9ab-121">PARAMETERS</span></span>

### <span data-ttu-id="fb9ab-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="fb9ab-122">-Certificate</span></span>
<span data-ttu-id="fb9ab-123">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-123">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-124">-Cluster</span><span class="sxs-lookup"><span data-stu-id="fb9ab-124">-Cluster</span></span>
<span data-ttu-id="fb9ab-125">Указывает кластер.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-125">Specifies a cluster.</span></span>
<span data-ttu-id="fb9ab-126">Этот командлет получает журналы заданий из кластера, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-126">This cmdlet gets job logs from the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-127">-DownloadTaskLogs</span><span class="sxs-lookup"><span data-stu-id="fb9ab-127">-DownloadTaskLogs</span></span>
<span data-ttu-id="fb9ab-128">Указывает на то, что этот командлет получает журналы задач для задания.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-128">Indicates that this cmdlet gets the task logs for a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-129">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="fb9ab-129">-Endpoint</span></span>
<span data-ttu-id="fb9ab-130">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-130">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="fb9ab-131">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-131">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-132">-HostedService</span><span class="sxs-lookup"><span data-stu-id="fb9ab-132">-HostedService</span></span>
<span data-ttu-id="fb9ab-133">Указывает пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-133">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-134">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="fb9ab-134">-IgnoreSslErrors</span></span>
<span data-ttu-id="fb9ab-135">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="fb9ab-135">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-136">-JobId</span><span class="sxs-lookup"><span data-stu-id="fb9ab-136">-JobId</span></span>
<span data-ttu-id="fb9ab-137">Указывает ИД задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-137">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="fb9ab-138">-Profile</span></span>
<span data-ttu-id="fb9ab-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb9ab-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb9ab-141">-StandardError</span><span class="sxs-lookup"><span data-stu-id="fb9ab-141">-StandardError</span></span>
<span data-ttu-id="fb9ab-142">Указывает на то, что этот командлет получает выходные данные StdErr для задания.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-142">Indicates that this cmdlet gets the StdErr output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-143">-StandardOutput</span><span class="sxs-lookup"><span data-stu-id="fb9ab-143">-StandardOutput</span></span>
<span data-ttu-id="fb9ab-144">Указывает на то, что этот командлет получает выходные данные SdtOut для задания.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-144">Indicates that this cmdlet gets the SdtOut output of a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-145">-Подписка</span><span class="sxs-lookup"><span data-stu-id="fb9ab-145">-Subscription</span></span>
<span data-ttu-id="fb9ab-146">Указывает подписку, которая содержит кластер HDInsight для получения.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-146">Specifies the subscription that contains the HDInsight cluster to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-147">-TaskLogsDirectory</span><span class="sxs-lookup"><span data-stu-id="fb9ab-147">-TaskLogsDirectory</span></span>
<span data-ttu-id="fb9ab-148">Указывает локальную папку для хранения журналов задач.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-148">Specifies a local folder in which to store tasks logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogsDir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-149">-TaskSummary</span><span class="sxs-lookup"><span data-stu-id="fb9ab-149">-TaskSummary</span></span>
<span data-ttu-id="fb9ab-150">Указывает на то, что этот командлет получает сводку журнала задач.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-150">Indicates that this cmdlets gets the task log summary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb9ab-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9ab-151">CommonParameters</span></span>
<span data-ttu-id="fb9ab-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb9ab-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9ab-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb9ab-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9ab-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb9ab-154">INPUTS</span></span>

## <span data-ttu-id="fb9ab-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb9ab-155">OUTPUTS</span></span>

## <span data-ttu-id="fb9ab-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb9ab-156">NOTES</span></span>

## <span data-ttu-id="fb9ab-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb9ab-157">RELATED LINKS</span></span>

[<span data-ttu-id="fb9ab-158">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fb9ab-158">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="fb9ab-159">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fb9ab-159">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="fb9ab-160">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fb9ab-160">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)
