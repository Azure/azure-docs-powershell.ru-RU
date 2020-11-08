---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 2EA36090-1A45-4F77-9222-9C0E9C07656C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea1247fd2b91f173b8125ad61c0bf2b57f408d18
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075832"
---
# <span data-ttu-id="86c57-101">Wait-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="86c57-101">Wait-AzureHDInsightJob</span></span>

## <span data-ttu-id="86c57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86c57-102">SYNOPSIS</span></span>
<span data-ttu-id="86c57-103">Ожидает завершения или сбоя задания HDInsight и отображает ход выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="86c57-103">Awaits the completion or failure of an HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="86c57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86c57-104">SYNTAX</span></span>

### <span data-ttu-id="86c57-105">Получение журнала jobDetails для кластера HDInsight (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86c57-105">Get jobDetails History of a HDInsight Cluster (Default)</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="86c57-106">Получение журнала jobDetails для кластера HDInsight (с определенными учетными данными подписки)</span><span class="sxs-lookup"><span data-stu-id="86c57-106">Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)</span></span>
```
Wait-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] [-Endpoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Job <AzureHDInsightJob> -Subscription <String> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="86c57-107">Ожидание задания с JobId в кластере HDInsight</span><span class="sxs-lookup"><span data-stu-id="86c57-107">Wait Job with JobId on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-WaitTimeoutInSeconds <Double>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="86c57-108">Ожидание задания в кластере HDInsight</span><span class="sxs-lookup"><span data-stu-id="86c57-108">Wait Job with Job on an HDInsight Cluster</span></span>
```
Wait-AzureHDInsightJob [-Credential <PSCredential>] -Job <AzureHDInsightJob> [-WaitTimeoutInSeconds <Double>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86c57-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c57-109">DESCRIPTION</span></span>
<span data-ttu-id="86c57-110">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="86c57-110">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="86c57-111">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="86c57-111">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="86c57-112">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="86c57-112">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="86c57-113">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="86c57-113">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="86c57-114">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="86c57-114">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="86c57-115">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="86c57-115">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="86c57-116">Командлет **Wait-AzureHDInsightJob** ожидает завершения или сбоя задания Azure HDInsight и отображает ход выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="86c57-116">The **Wait-AzureHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job and displays the progress of the job.</span></span>

## <span data-ttu-id="86c57-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86c57-117">EXAMPLES</span></span>

### <span data-ttu-id="86c57-118">Пример 1: запуск задания и ожидание его завершения</span><span class="sxs-lookup"><span data-stu-id="86c57-118">Example 1: Run a job and wait for it to complete</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:>\ $ClusterName = "MyCluster"
PS C:>\ $WordCountJob = New-AzureHDInsightMapReduceJobDefinition -JarFile "/Example/Apps/Hadoop-examples.jar" -ClassName "Wordcount" -Defines @{ "mapred.map.tasks" = "3" } -Arguments "/Example/Data/Gutenberg/Davinci.txt", "/Example/Output/WordCount" 
PS C:>\ $WordCountJob | Start-AzureHDInsightJob -Subscription $SubId -Cluster $ClusterName 
    | Wait-AzureHDInsightJob -Subscription $SubId -WaitTimeoutInSeconds 3600 
    | Get-AzureHDInsightJobOutput -Cluster $ClusterName -Subscription $SubId -StandardError
```

<span data-ttu-id="86c57-119">Первая команда получает идентификатор текущей подписки Azure, а затем сохраняет ее в переменной $SubId.</span><span class="sxs-lookup"><span data-stu-id="86c57-119">The first command gets the current Azure subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="86c57-120">Вторая команда возвращает указанный кластер, а затем сохраняет его в переменной $ClusterName.</span><span class="sxs-lookup"><span data-stu-id="86c57-120">The second command gets the specified cluster, and then stores it in the $ClusterName variable.</span></span>

<span data-ttu-id="86c57-121">Третья команда использует командлет **New-AzureHDInsightMapReduceJobDefinition** для создания определения задания MapReduce, а затем сохраняет его в переменной $WordCountJob.</span><span class="sxs-lookup"><span data-stu-id="86c57-121">The third command uses the **New-AzureHDInsightMapReduceJobDefinition** cmdlet to create a MapReduce job definition, and then stores it in the $WordCountJob variable.</span></span>

<span data-ttu-id="86c57-122">Четвертая команда использует несколько командлетов в последовательности:</span><span class="sxs-lookup"><span data-stu-id="86c57-122">The fourth command uses several cmdlets in sequence:</span></span> 

- <span data-ttu-id="86c57-123">Он использует оператор конвейера для передачи $WordCountJob командлету **Start-AzureHDInsightJob** для запуска задания.</span><span class="sxs-lookup"><span data-stu-id="86c57-123">It uses the pipeline operator to pass $WordCountJob to the **Start-AzureHDInsightJob** cmdlet to start the job.</span></span> 
- <span data-ttu-id="86c57-124">Задание передается командлету **Wait-AzureHDInsightJob** , чтобы подождать 3600 секунд, пока не завершится выполнение задания.</span><span class="sxs-lookup"><span data-stu-id="86c57-124">The job is passed to the **Wait-AzureHDInsightJob** cmdlet to wait 3600 seconds for the job to complete.</span></span> 
- <span data-ttu-id="86c57-125">Если задание завершается, команда использует командлет **Get-AzureHDInsightJobOutput** для получения выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="86c57-125">If the job completes, the command uses the **Get-AzureHDInsightJobOutput** cmdlet to get the job output.</span></span>

## <span data-ttu-id="86c57-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86c57-126">PARAMETERS</span></span>

### <span data-ttu-id="86c57-127">-Certificate</span><span class="sxs-lookup"><span data-stu-id="86c57-127">-Certificate</span></span>
<span data-ttu-id="86c57-128">Указывает сертификат управления для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="86c57-128">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-129">-Cluster</span><span class="sxs-lookup"><span data-stu-id="86c57-129">-Cluster</span></span>
<span data-ttu-id="86c57-130">Указывает кластер.</span><span class="sxs-lookup"><span data-stu-id="86c57-130">Specifies a cluster.</span></span>
<span data-ttu-id="86c57-131">Этот командлет ожидает задания в кластере, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="86c57-131">This cmdlet waits for a job on the cluster that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="86c57-132">-Credential</span></span>
<span data-ttu-id="86c57-133">Указывает учетные данные, которые следует использовать для прямого доступа по протоколу HTTP к кластеру.</span><span class="sxs-lookup"><span data-stu-id="86c57-133">Specifies the credentials to use for direct HTTP access to a cluster.</span></span>
<span data-ttu-id="86c57-134">Вы можете указать этот параметр вместо параметра *подписки* для проверки подлинности доступа к кластеру.</span><span class="sxs-lookup"><span data-stu-id="86c57-134">You can specify this parameter instead of the *Subscription* parameter to authenticate access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: Get jobDetails History of a HDInsight Cluster, Wait Job with JobId on an HDInsight Cluster, Wait Job with Job on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-135">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="86c57-135">-Endpoint</span></span>
<span data-ttu-id="86c57-136">Задает конечную точку, используемую для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="86c57-136">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="86c57-137">Если этот параметр не указан, этот командлет использует конечную точку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86c57-137">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-138">-HostedService</span><span class="sxs-lookup"><span data-stu-id="86c57-138">-HostedService</span></span>
<span data-ttu-id="86c57-139">Задает пространство имен службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="86c57-139">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="86c57-140">Если этот параметр не указан, используется пространство имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86c57-140">If you do not specify this parameter, the default namespace is used.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-141">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="86c57-141">-IgnoreSslErrors</span></span>
<span data-ttu-id="86c57-142">Указывает, пропускаются ли ошибки SSL (Secure Socketing Layer).</span><span class="sxs-lookup"><span data-stu-id="86c57-142">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-143">-Job</span><span class="sxs-lookup"><span data-stu-id="86c57-143">-Job</span></span>
<span data-ttu-id="86c57-144">Указывает задание Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="86c57-144">Specifies an Azure HDInsight job.</span></span>

```yaml
Type: AzureHDInsightJob
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential), Wait Job with Job on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-145">-JobId</span><span class="sxs-lookup"><span data-stu-id="86c57-145">-JobId</span></span>
<span data-ttu-id="86c57-146">Указывает ИД задания, которое нужно дождаться.</span><span class="sxs-lookup"><span data-stu-id="86c57-146">Specifies the ID of the job to wait for.</span></span>

```yaml
Type: String
Parameter Sets: Wait Job with JobId on an HDInsight Cluster
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="86c57-147">-Profile</span></span>
<span data-ttu-id="86c57-148">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="86c57-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86c57-149">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86c57-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86c57-150">-Подписка</span><span class="sxs-lookup"><span data-stu-id="86c57-150">-Subscription</span></span>
<span data-ttu-id="86c57-151">Указывает подписку.</span><span class="sxs-lookup"><span data-stu-id="86c57-151">Specifies a subscription.</span></span>
<span data-ttu-id="86c57-152">Этот командлет ожидает задания для подписки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="86c57-152">This cmdlet waits for a job for the subscription that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Get jobDetails History of a HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-153">-WaitTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="86c57-153">-WaitTimeoutInSeconds</span></span>
<span data-ttu-id="86c57-154">Указывает время ожидания в секундах для операции ожидания.</span><span class="sxs-lookup"><span data-stu-id="86c57-154">Specifies the time-out, in seconds, for the wait operation.</span></span>
<span data-ttu-id="86c57-155">Если тайм-аута истекает до завершения задания, командлет прекращает работу.</span><span class="sxs-lookup"><span data-stu-id="86c57-155">If the time-out expires before the job completes, the cmdlet ceases to run.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c57-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c57-156">CommonParameters</span></span>
<span data-ttu-id="86c57-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86c57-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c57-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c57-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c57-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86c57-159">INPUTS</span></span>

## <span data-ttu-id="86c57-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86c57-160">OUTPUTS</span></span>

## <span data-ttu-id="86c57-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="86c57-161">NOTES</span></span>

## <span data-ttu-id="86c57-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86c57-162">RELATED LINKS</span></span>

[<span data-ttu-id="86c57-163">Get-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="86c57-163">Get-AzureHDInsightJob</span></span>](./Get-AzureHDInsightJob.md)

[<span data-ttu-id="86c57-164">Get-AzureHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="86c57-164">Get-AzureHDInsightJobOutput</span></span>](./Get-AzureHDInsightJobOutput.md)

[<span data-ttu-id="86c57-165">Start-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="86c57-165">Start-AzureHDInsightJob</span></span>](./Start-AzureHDInsightJob.md)

[<span data-ttu-id="86c57-166">Остановить-AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="86c57-166">Stop-AzureHDInsightJob</span></span>](./Stop-AzureHDInsightJob.md)


