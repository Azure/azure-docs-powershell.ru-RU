---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 227D933A-9272-4C53-89AF-711379B47A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c32a80bec0820123a8ccf1a85f5c99bdac3195d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076010"
---
# <span data-ttu-id="f4ce5-101">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ce5-101">New-AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="f4ce5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ce5-103">Определяет новое задание свинья для службы HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-103">Defines a new Pig job for an HDInsight service.</span></span>

## <span data-ttu-id="f4ce5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4ce5-104">SYNTAX</span></span>

```
New-AzureHDInsightPigJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-Query <String>] [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4ce5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ce5-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f4ce5-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f4ce5-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f4ce5-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f4ce5-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f4ce5-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f4ce5-112">**Новый AzureHDInsightPigJobDefinition** определяет задание свинья для службы Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-112">The **New-AzureHDInsightPigJobDefinition** defines a Pig job for an Azure HDInsight service.</span></span>

## <span data-ttu-id="f4ce5-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4ce5-113">EXAMPLES</span></span>

### <span data-ttu-id="f4ce5-114">Пример 1: определение нового задания свинья</span><span class="sxs-lookup"><span data-stu-id="f4ce5-114">Example 1: Define a new Pig job</span></span>
```
PS C:\>$0 = '$0';
PS C:\> $QueryString =  "LOGS = LOAD 'wasb:///example/data/sample.log';" + "LEVELS = foreach LOGS generate REGEX_EXTRACT($0, '(TRACE|DEBUG|INFO|WARN|ERROR|FATAL)', 1) as LOGLEVEL;" + "FILTEREDLEVELS = FILTER LEVELS by LOGLEVEL is not null;" + "GROUPEDLEVELS = GROUP FILTEREDLEVELS by LOGLEVEL;" + "FREQUENCIES = foreach GROUPEDLEVELS generate group as LOGLEVEL, COUNT(FILTEREDLEVELS.LOGLEVEL) as COUNT;" + "RESULT = order FREQUENCIES by COUNT desc;" + "DUMP RESULT;"
PS C:\> $PigJobDefinition = New-AzureHDInsightPigJobDefinition -Query $QueryString
```

<span data-ttu-id="f4ce5-115">Первая команда объявляет строковое значение, а затем сохраняет его в переменной $0.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-115">The first command declares a string value, and then stores in the $0 variable.</span></span>

<span data-ttu-id="f4ce5-116">Вторая команда создает запрос задания свинья и сохраняет его в переменной $QueryString.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-116">The second command creates a Pig job query, and then stores it in the $QueryString variable.</span></span>

<span data-ttu-id="f4ce5-117">Последняя команда создает определение задания свинья, которое использует запрос в $QueryString, а затем сохраняет определение задания в переменной $PigJobDefinition.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-117">The final command creates a Pig job definition that uses the query in $QueryString, and then stores the job definition in the $PigJobDefinition variable.</span></span>

## <span data-ttu-id="f4ce5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4ce5-118">PARAMETERS</span></span>

### <span data-ttu-id="f4ce5-119">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="f4ce5-119">-Arguments</span></span>
<span data-ttu-id="f4ce5-120">Задает массив аргументов для задания свинья.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-120">Specifies an array of arguments for a Pig job.</span></span>
<span data-ttu-id="f4ce5-121">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f4ce5-122">-Файл</span><span class="sxs-lookup"><span data-stu-id="f4ce5-122">-File</span></span>
<span data-ttu-id="f4ce5-123">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-123">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="f4ce5-124">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-124">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="f4ce5-125">-Файлы</span><span class="sxs-lookup"><span data-stu-id="f4ce5-125">-Files</span></span>
<span data-ttu-id="f4ce5-126">Указывает набор файлов, связанных с заданием свинья.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-126">Specifies a collection of files that are associated with a Pig job.</span></span>

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

### <span data-ttu-id="f4ce5-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4ce5-127">-Profile</span></span>
<span data-ttu-id="f4ce5-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4ce5-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4ce5-130">-Query</span><span class="sxs-lookup"><span data-stu-id="f4ce5-130">-Query</span></span>
<span data-ttu-id="f4ce5-131">Указывает запрос задания свинья.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-131">Specifies a Pig job query.</span></span>

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

### <span data-ttu-id="f4ce5-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f4ce5-132">-StatusFolder</span></span>
<span data-ttu-id="f4ce5-133">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания, включая код завершения и журналы задач.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-133">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="f4ce5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ce5-134">CommonParameters</span></span>
<span data-ttu-id="f4ce5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4ce5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ce5-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ce5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ce5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4ce5-137">INPUTS</span></span>

## <span data-ttu-id="f4ce5-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ce5-138">OUTPUTS</span></span>

## <span data-ttu-id="f4ce5-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4ce5-139">NOTES</span></span>

## <span data-ttu-id="f4ce5-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4ce5-140">RELATED LINKS</span></span>

[<span data-ttu-id="f4ce5-141">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ce5-141">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="f4ce5-142">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ce5-142">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="f4ce5-143">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ce5-143">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)

[<span data-ttu-id="f4ce5-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f4ce5-144">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


