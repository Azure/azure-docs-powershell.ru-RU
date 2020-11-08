---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: be478ff5c5fb6c638a0fc775c7c6787083a182cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245359"
---
# <span data-ttu-id="4115c-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="4115c-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="4115c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4115c-102">SYNOPSIS</span></span>
<span data-ttu-id="4115c-103">Отправляет запрос на куст в кластер HDInsight и извлекает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="4115c-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="4115c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4115c-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4115c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4115c-105">DESCRIPTION</span></span>
<span data-ttu-id="4115c-106">Командлет **Invoke-AzHDInsightHiveJob** отправляет запрос Hive в кластер Azure HDInsight и извлекает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="4115c-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="4115c-107">Используйте командлет Use-AzHDInsightCluster перед вызовом **Invoke-AzHDInsightHiveJob** , чтобы указать кластер, который будет использоваться для запроса.</span><span class="sxs-lookup"><span data-stu-id="4115c-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="4115c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4115c-108">EXAMPLES</span></span>

### <span data-ttu-id="4115c-109">Пример 1: Отправка запроса куста в кластер HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="4115c-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="4115c-110">Эта команда отправляет запросы на добавление ТАБЛИЦ в кластер с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="4115c-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4115c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4115c-111">PARAMETERS</span></span>

### <span data-ttu-id="4115c-112">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="4115c-112">-Arguments</span></span>
<span data-ttu-id="4115c-113">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="4115c-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="4115c-114">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="4115c-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="4115c-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="4115c-115">-DefaultContainer</span></span>
<span data-ttu-id="4115c-116">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который используется кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4115c-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4115c-117">-DefaultProfile</span></span>
<span data-ttu-id="4115c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4115c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4115c-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4115c-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4115c-120">Указывает ключ учетной записи хранения, используемой по умолчанию, которую использует кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4115c-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4115c-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4115c-122">Указывает имя учетной записи хранения по умолчанию, используемой в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4115c-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-123">-Определение</span><span class="sxs-lookup"><span data-stu-id="4115c-123">-Defines</span></span>
<span data-ttu-id="4115c-124">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="4115c-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="4115c-125">-Файл</span><span class="sxs-lookup"><span data-stu-id="4115c-125">-File</span></span>
<span data-ttu-id="4115c-126">Задает путь к файлу в хранилище Azure, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="4115c-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="4115c-127">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="4115c-127">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-128">-Файлы</span><span class="sxs-lookup"><span data-stu-id="4115c-128">-Files</span></span>
<span data-ttu-id="4115c-129">Указывает набор файлов, необходимых для задания куста.</span><span class="sxs-lookup"><span data-stu-id="4115c-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="4115c-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="4115c-130">-JobName</span></span>
<span data-ttu-id="4115c-131">Указывает имя задания куста.</span><span class="sxs-lookup"><span data-stu-id="4115c-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="4115c-132">Если этот параметр не указан, используется значение по умолчанию: "куст: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="4115c-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-133">-Query</span><span class="sxs-lookup"><span data-stu-id="4115c-133">-Query</span></span>
<span data-ttu-id="4115c-134">Указывает запрос Hive.</span><span class="sxs-lookup"><span data-stu-id="4115c-134">Specifies the Hive query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="4115c-135">-RunAsFileJob</span></span>
<span data-ttu-id="4115c-136">Указывает на то, что этот командлет создает файл в учетной записи хранения Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="4115c-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="4115c-137">Этот командлет отправляет задание, которое ссылается на этот файл, как сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="4115c-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="4115c-138">С помощью этой функции можно обрабатывать специальные символы, такие как знак процента (%) Это может привести к сбою отправки задания через Templeton, поскольку Templeton интерпретирует запрос с символом процента в качестве параметра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="4115c-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="4115c-139">-StatusFolder</span></span>
<span data-ttu-id="4115c-140">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="4115c-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4115c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4115c-141">CommonParameters</span></span>
<span data-ttu-id="4115c-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4115c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4115c-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4115c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4115c-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4115c-144">INPUTS</span></span>

### <span data-ttu-id="4115c-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="4115c-145">None</span></span>

## <span data-ttu-id="4115c-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4115c-146">OUTPUTS</span></span>

### <span data-ttu-id="4115c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4115c-147">System.String</span></span>

## <span data-ttu-id="4115c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="4115c-148">NOTES</span></span>

## <span data-ttu-id="4115c-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4115c-149">RELATED LINKS</span></span>

[<span data-ttu-id="4115c-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4115c-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


