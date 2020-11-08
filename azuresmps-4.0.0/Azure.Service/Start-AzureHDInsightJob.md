---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 60A5ACF7-2637-4BDC-BF41-80E81B23F4CD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0308c3ff5bee358a82d74d452784f42c69bc7c32
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075424"
---
# <span data-ttu-id="bad9d-101">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bad9d-101">Start-AzureHDInsightJob</span></span>

## <span data-ttu-id="bad9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bad9d-102">SYNOPSIS</span></span>
<span data-ttu-id="bad9d-103">Запускает задание HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bad9d-103">Starts an HDInsight job.</span></span>

## <span data-ttu-id="bad9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bad9d-104">SYNTAX</span></span>

### <span data-ttu-id="bad9d-105">Запуск jobDetails на кластере HDInsight (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bad9d-105">Start jobDetails on an HDInsight Cluster (Default)</span></span>
```
Start-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>]
 -JobDefinition <AzureHDInsightJobDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bad9d-106">Запуск jobDetails в кластере HDInsight (с определенными учетными данными подписки)</span><span class="sxs-lookup"><span data-stu-id="bad9d-106">Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Start-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobDefinition <AzureHDInsightJobDefinition>
 [-Subscription <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bad9d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bad9d-107">DESCRIPTION</span></span>
<span data-ttu-id="bad9d-108">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="bad9d-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="bad9d-109">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="bad9d-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="bad9d-110">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bad9d-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="bad9d-111">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="bad9d-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="bad9d-112">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="bad9d-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="bad9d-113">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bad9d-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="bad9d-114">Командлет **Start-AzureHDInsightJob** запускает определенное задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="bad9d-114">The **Start-AzureHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="bad9d-115">Запуск задания может быть заданием MapReduce, потоковым заданием, заданием куста или заданием свинья.</span><span class="sxs-lookup"><span data-stu-id="bad9d-115">The job to start can be a MapReduce job, a streaming job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="bad9d-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bad9d-116">EXAMPLES</span></span>

### <span data-ttu-id="bad9d-117">Пример 1: запуск задания HDInsight</span><span class="sxs-lookup"><span data-stu-id="bad9d-117">Example 1: Start an HDInsight job</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $ClusterName = "Cluster01" 
PS C:\> $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:\> $WordCountJob | Start-AzureHDInsightJob -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="bad9d-118">Первая команда получает идентификатор текущей подписки, а затем сохраняет ее в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="bad9d-118">The first command gets the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="bad9d-119">Вторая команда назначает имя Cluster01 переменной $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="bad9d-119">The second command assigns the name Cluster01 to the $ClusterName variable.</span></span>

<span data-ttu-id="bad9d-120">Третья команда использует командлет **New-AzureHDInsightMapReduceJobDefinition** для создания определения задания MapReduce, а затем сохраняет его в переменной $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="bad9d-120">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="bad9d-121">В последней команде используется оператор Pipeline для передачи $WordCountJob командлету **Start-AzureHDInsightJob** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="bad9d-121">The final command uses the pipeline operator to pass the $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span>
<span data-ttu-id="bad9d-122">После запуска задания оно передается командлету **Wait-AzureHDInsightJob** , который ожидает завершения задания, прежде чем передать его командлету **Get-AzureHDInsightJobOutput** , чтобы получить выходные данные задания.</span><span class="sxs-lookup"><span data-stu-id="bad9d-122">After the job starts, it is passed to the **Wait-AzureHDInsightJob** cmdlet, which waits for the job to complete before passing it to the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="bad9d-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bad9d-123">PARAMETERS</span></span>

### <span data-ttu-id="bad9d-124">-Certificate</span><span class="sxs-lookup"><span data-stu-id="bad9d-124">-Certificate</span></span>
<span data-ttu-id="bad9d-125">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="bad9d-125">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-126">-Cluster</span><span class="sxs-lookup"><span data-stu-id="bad9d-126">-Cluster</span></span>
<span data-ttu-id="bad9d-127">Указывает кластер.</span><span class="sxs-lookup"><span data-stu-id="bad9d-127">Specifies a cluster.</span></span>
<span data-ttu-id="bad9d-128">Этот командлет запускает задание в кластере, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bad9d-128">This cmdlet starts a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="bad9d-129">-Credential</span></span>
<span data-ttu-id="bad9d-130">Указывает учетные данные кластера для прямого доступа по протоколу HTTP к кластеру.</span><span class="sxs-lookup"><span data-stu-id="bad9d-130">Specifies cluster credentials for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="bad9d-131">Вы можете указать этот параметр вместо параметра *подписки* для проверки подлинности доступа к кластеру.</span><span class="sxs-lookup"><span data-stu-id="bad9d-131">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-132">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="bad9d-132">-Endpoint</span></span>
<span data-ttu-id="bad9d-133">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="bad9d-133">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="bad9d-134">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bad9d-134">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-135">-HostedService</span><span class="sxs-lookup"><span data-stu-id="bad9d-135">-HostedService</span></span>
<span data-ttu-id="bad9d-136">Указывает пространство имен службы HDInsight, если вы не хотите использовать пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bad9d-136">Specifies the namespace of an HDInsight service if you do not want to use the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-137">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="bad9d-137">-IgnoreSslErrors</span></span>
<span data-ttu-id="bad9d-138">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="bad9d-138">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-139">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="bad9d-139">-JobDefinition</span></span>
<span data-ttu-id="bad9d-140">Задает конечную точку, используемую при подключении к Microsoft Azure, если конечная точка отличается от используемой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bad9d-140">Specifies the endpoint to use when connecting to Microsoft Azure if the endpoint is different from the default.</span></span>

```yaml
Type: AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases: jobDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="bad9d-141">-Profile</span></span>
<span data-ttu-id="bad9d-142">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bad9d-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bad9d-143">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bad9d-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bad9d-144">-Подписка</span><span class="sxs-lookup"><span data-stu-id="bad9d-144">-Subscription</span></span>
<span data-ttu-id="bad9d-145">Указывает подписку.</span><span class="sxs-lookup"><span data-stu-id="bad9d-145">Specifies a subscription.</span></span>
<span data-ttu-id="bad9d-146">Этот командлет запускает задание для подписки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bad9d-146">This cmdlet starts a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad9d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad9d-147">CommonParameters</span></span>
<span data-ttu-id="bad9d-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bad9d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad9d-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad9d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad9d-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bad9d-150">INPUTS</span></span>

## <span data-ttu-id="bad9d-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bad9d-151">OUTPUTS</span></span>

## <span data-ttu-id="bad9d-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="bad9d-152">NOTES</span></span>

## <span data-ttu-id="bad9d-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bad9d-153">RELATED LINKS</span></span>

[<span data-ttu-id="bad9d-154">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bad9d-154">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="bad9d-155">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="bad9d-155">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="bad9d-156">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bad9d-156">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="bad9d-157">Остановить-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bad9d-157">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)

[<span data-ttu-id="bad9d-158">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bad9d-158">Wait-AzureHDInsightJob</span></span>](./Wait-AzureHDInsightJob.md)


