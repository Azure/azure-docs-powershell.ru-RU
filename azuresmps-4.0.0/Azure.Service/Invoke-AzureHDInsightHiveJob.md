---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076248"
---
# <span data-ttu-id="755e9-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="755e9-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="755e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="755e9-102">SYNOPSIS</span></span>
<span data-ttu-id="755e9-103">Отправляет запросы Hive в кластер HDInsight, отображает ход выполнения запроса и возвращает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="755e9-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="755e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="755e9-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="755e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="755e9-105">DESCRIPTION</span></span>
<span data-ttu-id="755e9-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="755e9-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="755e9-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="755e9-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="755e9-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="755e9-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="755e9-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="755e9-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="755e9-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="755e9-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="755e9-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="755e9-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="755e9-112">Командлет **Invoke-AzureHDInsightHiveJob** отправляет запросы Hive в кластер HDInsight, отображает ход выполнения запроса и получает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="755e9-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="755e9-113">Перед запуском **Invoke-AzureHDInsightHiveJob** необходимо выполнить командлет Use-AzureHDInsightCluster, чтобы указать кластер HDInsight для отправки запроса.</span><span class="sxs-lookup"><span data-stu-id="755e9-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="755e9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="755e9-114">EXAMPLES</span></span>

### <span data-ttu-id="755e9-115">Пример 1: Отправка запроса куста</span><span class="sxs-lookup"><span data-stu-id="755e9-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="755e9-116">В первой команде используется командлет **use-AzureHDInsightCluster** , чтобы указать кластер в текущей подписке, который будет использоваться для запроса Hive.</span><span class="sxs-lookup"><span data-stu-id="755e9-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="755e9-117">Вторая команда использует командлет **Invoke-AzureHDInsightHiveJob** для отправки запроса куста.</span><span class="sxs-lookup"><span data-stu-id="755e9-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="755e9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="755e9-118">PARAMETERS</span></span>

### <span data-ttu-id="755e9-119">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="755e9-119">-Arguments</span></span>
<span data-ttu-id="755e9-120">Задает массив аргументов для задания Hadoop.</span><span class="sxs-lookup"><span data-stu-id="755e9-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="755e9-121">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="755e9-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="755e9-122">-Определение</span><span class="sxs-lookup"><span data-stu-id="755e9-122">-Defines</span></span>
<span data-ttu-id="755e9-123">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="755e9-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="755e9-124">-Файл</span><span class="sxs-lookup"><span data-stu-id="755e9-124">-File</span></span>
<span data-ttu-id="755e9-125">Указывает путь к большому двоичному хранилищу Windows Azure (WASB) для файла в хранилище BLOB-объектов Azure, содержащего запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="755e9-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="755e9-126">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="755e9-126">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755e9-127">-Файлы</span><span class="sxs-lookup"><span data-stu-id="755e9-127">-Files</span></span>
<span data-ttu-id="755e9-128">Указывает набор файлов, необходимых для задания куста.</span><span class="sxs-lookup"><span data-stu-id="755e9-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="755e9-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="755e9-129">-JobName</span></span>
<span data-ttu-id="755e9-130">Указывает имя задания куста.</span><span class="sxs-lookup"><span data-stu-id="755e9-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="755e9-131">Если этот параметр не указан, используется значение по умолчанию: "куст: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="755e9-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="755e9-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="755e9-132">-Profile</span></span>
<span data-ttu-id="755e9-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="755e9-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="755e9-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="755e9-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="755e9-135">-Query</span><span class="sxs-lookup"><span data-stu-id="755e9-135">-Query</span></span>
<span data-ttu-id="755e9-136">Указывает на запрос куста.</span><span class="sxs-lookup"><span data-stu-id="755e9-136">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755e9-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="755e9-137">-RunAsFileJob</span></span>
<span data-ttu-id="755e9-138">Указывает на то, что этот командлет создает файл в учетной записи хранения Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="755e9-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="755e9-139">Этот командлет отправляет задание, которое ссылается на этот файл, как сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="755e9-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="755e9-140">С помощью этой функции можно обрабатывать специальные символы, такие как знак процента (%) Это может привести к сбою отправки задания через Templeton, поскольку Templeton интерпретирует запрос с символом процента в качестве параметра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="755e9-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="755e9-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="755e9-141">-StatusFolder</span></span>
<span data-ttu-id="755e9-142">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания, включая код завершения и журналы задач.</span><span class="sxs-lookup"><span data-stu-id="755e9-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="755e9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755e9-143">CommonParameters</span></span>
<span data-ttu-id="755e9-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="755e9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755e9-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755e9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755e9-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="755e9-146">INPUTS</span></span>

## <span data-ttu-id="755e9-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="755e9-147">OUTPUTS</span></span>

## <span data-ttu-id="755e9-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="755e9-148">NOTES</span></span>

## <span data-ttu-id="755e9-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="755e9-149">RELATED LINKS</span></span>

[<span data-ttu-id="755e9-150">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="755e9-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="755e9-151">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="755e9-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


