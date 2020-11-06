---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Invoke-AzureRmHDInsightHiveJob.md
ms.openlocfilehash: 127e949bfaa9d54644f7f690cfefbf095d477374
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569448"
---
# <span data-ttu-id="2b2bc-101">Invoke-AzureRmHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="2b2bc-101">Invoke-AzureRmHDInsightHiveJob</span></span>

## <span data-ttu-id="2b2bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2bc-103">Отправляет запрос на куст в кластер HDInsight и извлекает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b2bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b2bc-104">SYNTAX</span></span>

```
Invoke-AzureRmHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b2bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2bc-106">Командлет **Invoke-AzureRmHDInsightHiveJob** отправляет запрос Hive в кластер Azure HDInsight и извлекает результаты запроса в одной операции.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-106">The **Invoke-AzureRmHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="2b2bc-107">Используйте командлет Use-AzureRmHDInsightCluster перед вызовом **Invoke-AzureRmHDInsightHiveJob** , чтобы указать кластер, который будет использоваться для запроса.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-107">Use the Use-AzureRmHDInsightCluster cmdlet before calling **Invoke-AzureRmHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="2b2bc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b2bc-108">EXAMPLES</span></span>

### <span data-ttu-id="2b2bc-109">Пример 1: Отправка запроса куста в кластер HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="2b2bc-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzureRmHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzureRmHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="2b2bc-110">Эта команда отправляет запросы на добавление ТАБЛИЦ в кластер с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2b2bc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b2bc-111">PARAMETERS</span></span>

### <span data-ttu-id="2b2bc-112">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="2b2bc-112">-Arguments</span></span>
<span data-ttu-id="2b2bc-113">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="2b2bc-114">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="2b2bc-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="2b2bc-115">-DefaultContainer</span></span>
<span data-ttu-id="2b2bc-116">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который используется кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="2b2bc-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2b2bc-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="2b2bc-118">Указывает ключ учетной записи хранения, используемой по умолчанию, которую использует кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-118">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="2b2bc-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2b2bc-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="2b2bc-120">Указывает имя учетной записи хранения по умолчанию, используемой в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-120">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="2b2bc-121">-Определение</span><span class="sxs-lookup"><span data-stu-id="2b2bc-121">-Defines</span></span>
<span data-ttu-id="2b2bc-122">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-122">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="2b2bc-123">-Файл</span><span class="sxs-lookup"><span data-stu-id="2b2bc-123">-File</span></span>
<span data-ttu-id="2b2bc-124">Задает путь к файлу в хранилище Azure, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-124">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="2b2bc-125">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="2b2bc-125">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="2b2bc-126">-Файлы</span><span class="sxs-lookup"><span data-stu-id="2b2bc-126">-Files</span></span>
<span data-ttu-id="2b2bc-127">Указывает набор файлов, необходимых для задания куста.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-127">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="2b2bc-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="2b2bc-128">-JobName</span></span>
<span data-ttu-id="2b2bc-129">Указывает имя задания куста.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-129">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="2b2bc-130">Если этот параметр не указан, используется значение по умолчанию: "куст: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="2b2bc-130">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="2b2bc-131">-Query</span><span class="sxs-lookup"><span data-stu-id="2b2bc-131">-Query</span></span>
<span data-ttu-id="2b2bc-132">Указывает запрос Hive.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-132">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="2b2bc-133">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="2b2bc-133">-RunAsFileJob</span></span>
<span data-ttu-id="2b2bc-134">Указывает на то, что этот командлет создает файл в учетной записи хранения Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-134">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="2b2bc-135">Этот командлет отправляет задание, которое ссылается на этот файл, как сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-135">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="2b2bc-136">С помощью этой функции можно обрабатывать специальные символы, такие как знак процента (%) Это может привести к сбою отправки задания через Templeton, поскольку Templeton интерпретирует запрос с символом процента в качестве параметра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-136">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="2b2bc-137">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2b2bc-137">-StatusFolder</span></span>
<span data-ttu-id="2b2bc-138">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-138">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="2b2bc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2bc-139">-DefaultProfile</span></span>
<span data-ttu-id="2b2bc-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b2bc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2bc-141">CommonParameters</span></span>
<span data-ttu-id="2b2bc-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b2bc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2bc-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b2bc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2bc-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b2bc-144">INPUTS</span></span>

## <span data-ttu-id="2b2bc-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b2bc-145">OUTPUTS</span></span>

### <span data-ttu-id="2b2bc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2b2bc-146">System.String</span></span>

## <span data-ttu-id="2b2bc-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b2bc-147">NOTES</span></span>

## <span data-ttu-id="2b2bc-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b2bc-148">RELATED LINKS</span></span>

[<span data-ttu-id="2b2bc-149">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2b2bc-149">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


