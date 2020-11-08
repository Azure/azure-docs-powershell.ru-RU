---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: E11AAB11-0CBF-4746-91D7-4D5E64801C29
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6dba4c331a69093f49c95728c028eaaf5d0bdb4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075915"
---
# <span data-ttu-id="ee314-101">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee314-101">New-AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="ee314-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee314-102">SYNOPSIS</span></span>
<span data-ttu-id="ee314-103">Определяет новое задание Sqoop.</span><span class="sxs-lookup"><span data-stu-id="ee314-103">Defines a new Sqoop job.</span></span>

## <span data-ttu-id="ee314-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee314-104">SYNTAX</span></span>

```
New-AzureHDInsightSqoopJobDefinition [-Command <String>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee314-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee314-105">DESCRIPTION</span></span>
<span data-ttu-id="ee314-106">Эта версия Azure PowerShell HDInsight устарела.</span><span class="sxs-lookup"><span data-stu-id="ee314-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="ee314-107">Эти командлеты будут удалены с 1 января 2017 г.</span><span class="sxs-lookup"><span data-stu-id="ee314-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="ee314-108">Пожалуйста, используйте более новую версию Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ee314-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="ee314-109">Сведения о том, как использовать новую HDInsight для создания кластера, можно найти в разделе Создание кластеров [на базе Linux в HDInsight с помощью Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ee314-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="ee314-110">Сведения о том, как отправлять задания с помощью Azure PowerShell и другие подходы, приведены [в разделе Отправка заданий Hadoop в HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="ee314-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="ee314-111">Справочные сведения о службе Azure PowerShell HDInsight можно найти в [командлетах Azure hdinsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ee314-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="ee314-112">Командлет **New-AzureHDInsightSqoopJobDefinition** создает задание Sqoop для выполнения в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="ee314-112">The **New-AzureHDInsightSqoopJobDefinition** cmdlet creates a Sqoop job to run on an Azure HDInsight cluster.</span></span>

<span data-ttu-id="ee314-113">Sqoop — это инструмент для передачи данных между кластерами Hadoop и реляционными базами данных.</span><span class="sxs-lookup"><span data-stu-id="ee314-113">Sqoop is a tool to transfer data between Hadoop clusters and relational databases.</span></span>
<span data-ttu-id="ee314-114">Вы можете использовать Sqoop для импорта данных из базы данных SQL Server в распределенную файловую систему Hadoop (HDFS), преобразовать данные с помощью Hadoop MapReduce и затем экспортировать данные из HDFS обратно в базу данных SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ee314-114">You can use Sqoop to import data from a SQL Server database to a Hadoop Distributed File System (HDFS), transform the data with Hadoop MapReduce, and then export the data from the HDFS back to the SQL Server database.</span></span>

## <span data-ttu-id="ee314-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee314-115">EXAMPLES</span></span>

### <span data-ttu-id="ee314-116">Пример 1: импорт данных</span><span class="sxs-lookup"><span data-stu-id="ee314-116">Example 1: Import data</span></span>
```
PS C:\>$SqoopJobDef = New-AzureHDInsightSqoopJobDefinition -Command "import --connect jdbc:sqlserver://<SQLDatabaseServerName>.database.windows.net:1433;username=<SQLDatabasUsername>@<SQLDatabaseServerName>; password=<SQLDatabasePassword>; database=<SQLDatabaseDatabaseName> --table <TableName> --target-dir wasb://<ContainerName>@<WindowsAzureStorageAccountName>.blob.core.windows.net/<Path>"
```

<span data-ttu-id="ee314-117">Эта команда определяет задание Sqoop, которое импортирует все строки в таблице из базы данных сервера AzureSQL в кластер HDInsight, а затем сохраняет определение задания в переменной $SqoopJobDef.</span><span class="sxs-lookup"><span data-stu-id="ee314-117">This command defines a Sqoop job that imports all of the rows in a table from an AzureSQL Server database to an HDInsight cluster, and then stores the job definition in the $SqoopJobDef variable.</span></span>

## <span data-ttu-id="ee314-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee314-118">PARAMETERS</span></span>

### <span data-ttu-id="ee314-119">-Command</span><span class="sxs-lookup"><span data-stu-id="ee314-119">-Command</span></span>
<span data-ttu-id="ee314-120">Указывает команду Sqoop и ее аргументы.</span><span class="sxs-lookup"><span data-stu-id="ee314-120">Specifies a Sqoop command and its arguments.</span></span>

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

### <span data-ttu-id="ee314-121">-Файл</span><span class="sxs-lookup"><span data-stu-id="ee314-121">-File</span></span>
<span data-ttu-id="ee314-122">Задает путь к файлу сценария, содержащему команды для выполнения.</span><span class="sxs-lookup"><span data-stu-id="ee314-122">Specifies the path to a script file that contains the commands to run.</span></span>
<span data-ttu-id="ee314-123">Файл сценария должен находиться на WASB.</span><span class="sxs-lookup"><span data-stu-id="ee314-123">The script file must be located on WASB.</span></span>

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

### <span data-ttu-id="ee314-124">-Файлы</span><span class="sxs-lookup"><span data-stu-id="ee314-124">-Files</span></span>
<span data-ttu-id="ee314-125">Указывает коллекцию файлов WASB, необходимых для задания.</span><span class="sxs-lookup"><span data-stu-id="ee314-125">Specifies the collection of WASB files that are required for a job.</span></span>

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

### <span data-ttu-id="ee314-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="ee314-126">-Profile</span></span>
<span data-ttu-id="ee314-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ee314-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee314-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ee314-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee314-129">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ee314-129">-StatusFolder</span></span>
<span data-ttu-id="ee314-130">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания, включая код завершения и журналы задач.</span><span class="sxs-lookup"><span data-stu-id="ee314-130">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="ee314-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee314-131">CommonParameters</span></span>
<span data-ttu-id="ee314-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee314-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee314-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee314-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee314-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee314-134">INPUTS</span></span>

## <span data-ttu-id="ee314-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee314-135">OUTPUTS</span></span>

## <span data-ttu-id="ee314-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee314-136">NOTES</span></span>

## <span data-ttu-id="ee314-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee314-137">RELATED LINKS</span></span>

[<span data-ttu-id="ee314-138">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee314-138">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="ee314-139">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee314-139">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="ee314-140">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee314-140">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="ee314-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ee314-141">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>](./New-AzureHDInsightStreamingMapReduceJobDefinition.md)


