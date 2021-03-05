---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 2846848394cf6f376bd6b4064e193640806f81b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959640"
---
# <span data-ttu-id="0c7ab-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="0c7ab-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="0c7ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7ab-103">Отправка запроса на вирус в кластер HDInsight и извлечение результатов запроса за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="0c7ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c7ab-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c7ab-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7ab-106">Cmdlet **Invoke-AzHDInsightHiveJob** передает запрос Нагов в кластер Azure HDInsight и извлекает результаты запроса за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="0c7ab-107">Перед вызовом **Invoke-AzHDInsightHiveJob** используйте Use-AzHDInsightCluster, чтобы указать, какой кластер будет использоваться для запроса.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="0c7ab-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c7ab-108">EXAMPLES</span></span>

### <span data-ttu-id="0c7ab-109">Пример 1. Отправка запроса на отправку в кластер Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="0c7ab-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="0c7ab-110">Эта команда передает запрос SHOW TABLES в кластер под названием "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="0c7ab-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0c7ab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7ab-111">PARAMETERS</span></span>

### <span data-ttu-id="0c7ab-112">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="0c7ab-112">-Arguments</span></span>
<span data-ttu-id="0c7ab-113">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="0c7ab-114">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="0c7ab-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="0c7ab-115">-DefaultContainer</span></span>
<span data-ttu-id="0c7ab-116">Имя контейнера по умолчанию в учетной записи хранилища Azure, которая используется для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="0c7ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7ab-117">-DefaultProfile</span></span>
<span data-ttu-id="0c7ab-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0c7ab-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c7ab-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0c7ab-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="0c7ab-120">Указывает ключ учетной записи хранения, которая используется по умолчанию для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="0c7ab-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0c7ab-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="0c7ab-122">Указывает имя учетной записи хранения по умолчанию, которая используется кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="0c7ab-123">-Определяет</span><span class="sxs-lookup"><span data-stu-id="0c7ab-123">-Defines</span></span>
<span data-ttu-id="0c7ab-124">Определяет значения конфигурации Hadoop, заданные при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="0c7ab-125">-File</span><span class="sxs-lookup"><span data-stu-id="0c7ab-125">-File</span></span>
<span data-ttu-id="0c7ab-126">Путь к файлу в хранилище Azure, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="0c7ab-127">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="0c7ab-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="0c7ab-128">-Файлы</span><span class="sxs-lookup"><span data-stu-id="0c7ab-128">-Files</span></span>
<span data-ttu-id="0c7ab-129">Набор файлов, необходимых для задания "Файл".</span><span class="sxs-lookup"><span data-stu-id="0c7ab-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="0c7ab-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="0c7ab-130">-JobName</span></span>
<span data-ttu-id="0c7ab-131">Имя задания "Фамилия".</span><span class="sxs-lookup"><span data-stu-id="0c7ab-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="0c7ab-132">Если этот параметр не задан, для этого cmdlet используется значение по умолчанию: "Окаймь: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="0c7ab-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="0c7ab-133">-Query</span><span class="sxs-lookup"><span data-stu-id="0c7ab-133">-Query</span></span>
<span data-ttu-id="0c7ab-134">Указывает запрос на это.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="0c7ab-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="0c7ab-135">-RunAsFileJob</span></span>
<span data-ttu-id="0c7ab-136">Указывает на то, что этот cmdlet создает файл в учетной записи хранилища Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="0c7ab-137">Этот cmdlet submits the job that references this file as a script to run.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="0c7ab-138">Эта функция позволяет обрабатывать специальные знаки, например знак процента (%). которые не будут работать при отправке задания через Templeton, так как Templeton интерпретирует запрос со знаком процента как URL-параметр.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="0c7ab-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0c7ab-139">-StatusFolder</span></span>
<span data-ttu-id="0c7ab-140">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="0c7ab-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7ab-141">CommonParameters</span></span>
<span data-ttu-id="0c7ab-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7ab-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7ab-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7ab-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7ab-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c7ab-144">INPUTS</span></span>

### <span data-ttu-id="0c7ab-145">Нет</span><span class="sxs-lookup"><span data-stu-id="0c7ab-145">None</span></span>

## <span data-ttu-id="0c7ab-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c7ab-146">OUTPUTS</span></span>

### <span data-ttu-id="0c7ab-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0c7ab-147">System.String</span></span>

## <span data-ttu-id="0c7ab-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c7ab-148">NOTES</span></span>

## <span data-ttu-id="0c7ab-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c7ab-149">RELATED LINKS</span></span>

[<span data-ttu-id="0c7ab-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0c7ab-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


