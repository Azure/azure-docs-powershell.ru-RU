---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079064"
---
# <span data-ttu-id="46985-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="46985-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="46985-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46985-102">SYNOPSIS</span></span>
<span data-ttu-id="46985-103">Создание объекта задания куста.</span><span class="sxs-lookup"><span data-stu-id="46985-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="46985-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46985-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46985-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46985-105">DESCRIPTION</span></span>
<span data-ttu-id="46985-106">Командлет **New-AzHDInsightHiveJobDefinition** определяет объект задания куста для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="46985-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="46985-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46985-107">EXAMPLES</span></span>

### <span data-ttu-id="46985-108">Пример 1: Создание определения задания куста</span><span class="sxs-lookup"><span data-stu-id="46985-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="46985-109">Эта команда создает определение задания куста.</span><span class="sxs-lookup"><span data-stu-id="46985-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="46985-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46985-110">PARAMETERS</span></span>

### <span data-ttu-id="46985-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="46985-111">-Arguments</span></span>
<span data-ttu-id="46985-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="46985-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="46985-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="46985-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="46985-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46985-114">-DefaultProfile</span></span>
<span data-ttu-id="46985-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="46985-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46985-116">-Определение</span><span class="sxs-lookup"><span data-stu-id="46985-116">-Defines</span></span>
<span data-ttu-id="46985-117">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="46985-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="46985-118">-Файл</span><span class="sxs-lookup"><span data-stu-id="46985-118">-File</span></span>
<span data-ttu-id="46985-119">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="46985-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="46985-120">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="46985-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="46985-121">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="46985-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="46985-122">-Файлы</span><span class="sxs-lookup"><span data-stu-id="46985-122">-Files</span></span>
<span data-ttu-id="46985-123">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="46985-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="46985-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="46985-124">-JobName</span></span>
<span data-ttu-id="46985-125">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="46985-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="46985-126">-Query</span><span class="sxs-lookup"><span data-stu-id="46985-126">-Query</span></span>
<span data-ttu-id="46985-127">Указывает запрос Hive.</span><span class="sxs-lookup"><span data-stu-id="46985-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="46985-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="46985-128">-RunAsFileJob</span></span>
<span data-ttu-id="46985-129">Указывает на то, что этот командлет создает файл в учетной записи хранения Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="46985-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="46985-130">Этот командлет отправляет задание, которое ссылается на этот файл, как сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="46985-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="46985-131">С помощью этой функции можно обрабатывать специальные символы, такие как знак процента (%) Это может привести к сбою отправки задания через Templeton, поскольку Templeton интерпретирует запрос с символом процента в качестве параметра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="46985-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="46985-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="46985-132">-StatusFolder</span></span>
<span data-ttu-id="46985-133">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="46985-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="46985-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46985-134">CommonParameters</span></span>
<span data-ttu-id="46985-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46985-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46985-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46985-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46985-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46985-137">INPUTS</span></span>

### <span data-ttu-id="46985-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="46985-138">None</span></span>

## <span data-ttu-id="46985-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46985-139">OUTPUTS</span></span>

### <span data-ttu-id="46985-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="46985-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="46985-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="46985-141">NOTES</span></span>

## <span data-ttu-id="46985-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46985-142">RELATED LINKS</span></span>

[<span data-ttu-id="46985-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="46985-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


