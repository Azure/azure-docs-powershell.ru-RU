---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 0DFCB891-7431-4C00-98DD-263DC2794354
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea6fbc76a76533c07b11935e50e25418d10e38ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075917"
---
# <span data-ttu-id="f04b9-101">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f04b9-101">New-AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="f04b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f04b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f04b9-103">Определяет новое задание куста для службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f04b9-103">Defines a new Hive job for an HDInsight service.</span></span>

## <span data-ttu-id="f04b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f04b9-104">SYNTAX</span></span>

```
New-AzureHDInsightHiveJobDefinition [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f04b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f04b9-105">DESCRIPTION</span></span>
<span data-ttu-id="f04b9-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="f04b9-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f04b9-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="f04b9-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f04b9-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f04b9-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f04b9-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f04b9-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f04b9-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f04b9-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f04b9-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f04b9-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f04b9-112">Командлет **New-AzureHDInsightHiveJobDefinition** определяет задание куста для службы Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f04b9-112">The **New-AzureHDInsightHiveJobDefinition** cmdlet defines a Hive job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="f04b9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f04b9-113">EXAMPLES</span></span>

### <span data-ttu-id="f04b9-114">Пример 1: Создание определения задания куста</span><span class="sxs-lookup"><span data-stu-id="f04b9-114">Example 1: Create a Hive job definition</span></span>
```
PS C:\>$HiveJobDefinition = New-AzureHDInsightHiveJobDefinition -Query $QueryString
```

<span data-ttu-id="f04b9-115">Эта команда создает определение задания куста, которое использует предварительно определенную строку запроса, а затем сохраняет ее в переменной $HiveJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="f04b9-115">This command creates a Hive job definition that uses a pre-defined query string, and then stores it in the $HiveJobDefinition variable.</span></span>

## <span data-ttu-id="f04b9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f04b9-116">PARAMETERS</span></span>

### <span data-ttu-id="f04b9-117">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="f04b9-117">-Arguments</span></span>
<span data-ttu-id="f04b9-118">Задает массив аргументов для задания Hadoop.</span><span class="sxs-lookup"><span data-stu-id="f04b9-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="f04b9-119">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="f04b9-119">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f04b9-120">-Определение</span><span class="sxs-lookup"><span data-stu-id="f04b9-120">-Defines</span></span>
<span data-ttu-id="f04b9-121">Задает значения конфигурации Hadoop, которые должны быть заданы для выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="f04b9-121">Specifies Hadoop configuration values to set for when a job runs.</span></span>

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

### <span data-ttu-id="f04b9-122">-Файл</span><span class="sxs-lookup"><span data-stu-id="f04b9-122">-File</span></span>
<span data-ttu-id="f04b9-123">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="f04b9-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="f04b9-124">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="f04b9-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f04b9-125">-Файлы</span><span class="sxs-lookup"><span data-stu-id="f04b9-125">-Files</span></span>
<span data-ttu-id="f04b9-126">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="f04b9-126">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f04b9-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="f04b9-127">-JobName</span></span>
<span data-ttu-id="f04b9-128">Указывает имя задания куста, которое нужно определить.</span><span class="sxs-lookup"><span data-stu-id="f04b9-128">Specifies the name of the Hive job to define.</span></span>
<span data-ttu-id="f04b9-129">Если этот параметр не указан, используется имя по умолчанию: "куст: \<first 100 characters of query\> ".</span><span class="sxs-lookup"><span data-stu-id="f04b9-129">If you do not specify this parameter, the default name is used: "Hive: \<first 100 characters of query\>".</span></span>

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

### <span data-ttu-id="f04b9-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="f04b9-130">-Profile</span></span>
<span data-ttu-id="f04b9-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f04b9-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f04b9-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f04b9-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f04b9-133">-Query</span><span class="sxs-lookup"><span data-stu-id="f04b9-133">-Query</span></span>
<span data-ttu-id="f04b9-134">Указывает на запрос куста.</span><span class="sxs-lookup"><span data-stu-id="f04b9-134">Specifies a Hive query.</span></span>

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

### <span data-ttu-id="f04b9-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="f04b9-135">-RunAsFileJob</span></span>
<span data-ttu-id="f04b9-136">Указывает на то, что этот командлет создает файл в учетной записи хранения Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="f04b9-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="f04b9-137">Этот командлет отправляет задание, которое ссылается на этот файл, как сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="f04b9-137">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="f04b9-138">С помощью этой функции можно обрабатывать специальные символы, такие как знак процента (%) Это может привести к сбою отправки задания через Templeton, поскольку Templeton интерпретирует запрос с символом процента в качестве параметра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f04b9-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="f04b9-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f04b9-139">-StatusFolder</span></span>
<span data-ttu-id="f04b9-140">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания, включая код завершения и журналы задач.</span><span class="sxs-lookup"><span data-stu-id="f04b9-140">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="f04b9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04b9-141">CommonParameters</span></span>
<span data-ttu-id="f04b9-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f04b9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04b9-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f04b9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04b9-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f04b9-144">INPUTS</span></span>

## <span data-ttu-id="f04b9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f04b9-145">OUTPUTS</span></span>

## <span data-ttu-id="f04b9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="f04b9-146">NOTES</span></span>

## <span data-ttu-id="f04b9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f04b9-147">RELATED LINKS</span></span>

[<span data-ttu-id="f04b9-148">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f04b9-148">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="f04b9-149">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f04b9-149">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="f04b9-150">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f04b9-150">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="f04b9-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f04b9-151">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


