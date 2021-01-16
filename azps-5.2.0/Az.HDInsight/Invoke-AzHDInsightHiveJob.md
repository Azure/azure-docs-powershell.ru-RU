---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: be478ff5c5fb6c638a0fc775c7c6787083a182cd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396604"
---
# <span data-ttu-id="14940-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="14940-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="14940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14940-102">SYNOPSIS</span></span>
<span data-ttu-id="14940-103">Отправка запроса на операцию в кластер HDInsight и извлечение результатов запроса за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="14940-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="14940-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14940-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14940-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14940-105">DESCRIPTION</span></span>
<span data-ttu-id="14940-106">Cmdlet **Invoke-AzHDInsightHiveJob** передает запрос Нагов в кластер Azure HDInsight и извлекает результаты запроса за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="14940-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="14940-107">Перед вызовом **Invoke-AzHDInsightHiveJob** используйте Use-AzHDInsightCluster, чтобы указать, какой кластер будет использоваться для запроса.</span><span class="sxs-lookup"><span data-stu-id="14940-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="14940-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14940-108">EXAMPLES</span></span>

### <span data-ttu-id="14940-109">Пример 1. Отправка запроса на отправку в кластер Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="14940-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="14940-110">Эта команда передает запрос SHOW TABLES в кластер под названием "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="14940-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="14940-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14940-111">PARAMETERS</span></span>

### <span data-ttu-id="14940-112">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="14940-112">-Arguments</span></span>
<span data-ttu-id="14940-113">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="14940-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="14940-114">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="14940-114">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="14940-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="14940-115">-DefaultContainer</span></span>
<span data-ttu-id="14940-116">Имя контейнера по умолчанию в учетной записи хранилища Azure, которая используется для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="14940-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="14940-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14940-117">-DefaultProfile</span></span>
<span data-ttu-id="14940-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="14940-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14940-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="14940-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="14940-120">Указывает ключ учетной записи хранения, которая используется по умолчанию для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="14940-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="14940-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14940-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="14940-122">Указывает имя учетной записи хранения по умолчанию, которая используется кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="14940-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

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

### <span data-ttu-id="14940-123">-Определяет</span><span class="sxs-lookup"><span data-stu-id="14940-123">-Defines</span></span>
<span data-ttu-id="14940-124">Определяет значения конфигурации Hadoop, заданные при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="14940-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="14940-125">-File</span><span class="sxs-lookup"><span data-stu-id="14940-125">-File</span></span>
<span data-ttu-id="14940-126">Путь к файлу в хранилище Azure, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="14940-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="14940-127">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="14940-127">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="14940-128">-Файлы</span><span class="sxs-lookup"><span data-stu-id="14940-128">-Files</span></span>
<span data-ttu-id="14940-129">Набор файлов, необходимых для задания "Файл".</span><span class="sxs-lookup"><span data-stu-id="14940-129">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="14940-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="14940-130">-JobName</span></span>
<span data-ttu-id="14940-131">Определяет имя задания".</span><span class="sxs-lookup"><span data-stu-id="14940-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="14940-132">Если этот параметр не задан, этот cmdlet использует значение по умолчанию: "Вися: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="14940-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="14940-133">-Query</span><span class="sxs-lookup"><span data-stu-id="14940-133">-Query</span></span>
<span data-ttu-id="14940-134">Указывает запрос на это.</span><span class="sxs-lookup"><span data-stu-id="14940-134">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="14940-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="14940-135">-RunAsFileJob</span></span>
<span data-ttu-id="14940-136">Указывает на то, что этот cmdlet создает файл в учетной записи хранилища Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="14940-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="14940-137">Этот cmdlet submits the job that references this file as a script to run.</span><span class="sxs-lookup"><span data-stu-id="14940-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="14940-138">Эта функция позволяет обрабатывать специальные знаки, например знак процента (%). которые не будут работать при отправке задания через Templeton, так как Templeton интерпретирует запрос со знаком процента как URL-параметр.</span><span class="sxs-lookup"><span data-stu-id="14940-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="14940-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="14940-139">-StatusFolder</span></span>
<span data-ttu-id="14940-140">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="14940-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="14940-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14940-141">CommonParameters</span></span>
<span data-ttu-id="14940-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14940-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14940-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14940-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14940-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14940-144">INPUTS</span></span>

### <span data-ttu-id="14940-145">Нет</span><span class="sxs-lookup"><span data-stu-id="14940-145">None</span></span>

## <span data-ttu-id="14940-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14940-146">OUTPUTS</span></span>

### <span data-ttu-id="14940-147">System.String</span><span class="sxs-lookup"><span data-stu-id="14940-147">System.String</span></span>

## <span data-ttu-id="14940-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14940-148">NOTES</span></span>

## <span data-ttu-id="14940-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14940-149">RELATED LINKS</span></span>

[<span data-ttu-id="14940-150">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="14940-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

