---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247835"
---
# <span data-ttu-id="780ff-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="780ff-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="780ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="780ff-102">SYNOPSIS</span></span>
<span data-ttu-id="780ff-103">Создает потоковый объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="780ff-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="780ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="780ff-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="780ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="780ff-105">DESCRIPTION</span></span>
<span data-ttu-id="780ff-106">Командлет **New-AzHDInsightStreamingMapReduceJobDefinition** определяет объект задания для потоковой передачи MapReduce для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="780ff-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="780ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="780ff-107">EXAMPLES</span></span>

### <span data-ttu-id="780ff-108">Пример 1: Создание определения задания для потоковой MapReduce</span><span class="sxs-lookup"><span data-stu-id="780ff-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="780ff-109">Эта команда создает определение задания для потоковой передачи MapReduce.</span><span class="sxs-lookup"><span data-stu-id="780ff-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="780ff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="780ff-110">PARAMETERS</span></span>

### <span data-ttu-id="780ff-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="780ff-111">-Arguments</span></span>
<span data-ttu-id="780ff-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="780ff-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="780ff-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="780ff-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="780ff-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="780ff-114">-CommandEnvironment</span></span>
<span data-ttu-id="780ff-115">Задает массив переменных среды командной строки, которые должны быть заданы при запуске задания на рабочих узлах.</span><span class="sxs-lookup"><span data-stu-id="780ff-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="780ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780ff-116">-DefaultProfile</span></span>
<span data-ttu-id="780ff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="780ff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="780ff-118">-Определение</span><span class="sxs-lookup"><span data-stu-id="780ff-118">-Defines</span></span>
<span data-ttu-id="780ff-119">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="780ff-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="780ff-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="780ff-120">-File</span></span>
<span data-ttu-id="780ff-121">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="780ff-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="780ff-122">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="780ff-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="780ff-123">-Файлы</span><span class="sxs-lookup"><span data-stu-id="780ff-123">-Files</span></span>
<span data-ttu-id="780ff-124">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="780ff-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="780ff-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="780ff-125">-InputPath</span></span>
<span data-ttu-id="780ff-126">Задает путь к входным файлам.</span><span class="sxs-lookup"><span data-stu-id="780ff-126">Specifies the path to the input files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780ff-127">-Сопоставитель</span><span class="sxs-lookup"><span data-stu-id="780ff-127">-Mapper</span></span>
<span data-ttu-id="780ff-128">Указывает имя файла сопоставителя.</span><span class="sxs-lookup"><span data-stu-id="780ff-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="780ff-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="780ff-129">-OutputPath</span></span>
<span data-ttu-id="780ff-130">Указывает путь для выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="780ff-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="780ff-131">-Reduce</span><span class="sxs-lookup"><span data-stu-id="780ff-131">-Reducer</span></span>
<span data-ttu-id="780ff-132">Указывает имя файла сокращения.</span><span class="sxs-lookup"><span data-stu-id="780ff-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="780ff-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="780ff-133">-StatusFolder</span></span>
<span data-ttu-id="780ff-134">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="780ff-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="780ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780ff-135">CommonParameters</span></span>
<span data-ttu-id="780ff-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="780ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780ff-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780ff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780ff-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="780ff-138">INPUTS</span></span>

### <span data-ttu-id="780ff-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="780ff-139">None</span></span>

## <span data-ttu-id="780ff-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="780ff-140">OUTPUTS</span></span>

### <span data-ttu-id="780ff-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="780ff-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="780ff-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="780ff-142">NOTES</span></span>

## <span data-ttu-id="780ff-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="780ff-143">RELATED LINKS</span></span>

[<span data-ttu-id="780ff-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="780ff-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


