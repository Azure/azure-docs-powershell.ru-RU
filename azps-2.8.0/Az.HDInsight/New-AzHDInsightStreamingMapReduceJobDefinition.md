---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 8fae0a8da7024ed49ee3d69a658431377b4f780f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720813"
---
# <span data-ttu-id="a7832-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a7832-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="a7832-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7832-102">SYNOPSIS</span></span>
<span data-ttu-id="a7832-103">Создает потоковый объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="a7832-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="a7832-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7832-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7832-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7832-105">DESCRIPTION</span></span>
<span data-ttu-id="a7832-106">Командлет **New-AzHDInsightStreamingMapReduceJobDefinition** определяет объект задания для потоковой передачи MapReduce для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="a7832-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a7832-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7832-107">EXAMPLES</span></span>

### <span data-ttu-id="a7832-108">Пример 1: Создание определения задания для потоковой MapReduce</span><span class="sxs-lookup"><span data-stu-id="a7832-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="a7832-109">Эта команда создает определение задания для потоковой передачи MapReduce.</span><span class="sxs-lookup"><span data-stu-id="a7832-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="a7832-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7832-110">PARAMETERS</span></span>

### <span data-ttu-id="a7832-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="a7832-111">-Arguments</span></span>
<span data-ttu-id="a7832-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="a7832-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="a7832-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="a7832-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="a7832-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="a7832-114">-CommandEnvironment</span></span>
<span data-ttu-id="a7832-115">Задает массив переменных среды командной строки, которые должны быть заданы при запуске задания на рабочих узлах.</span><span class="sxs-lookup"><span data-stu-id="a7832-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="a7832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7832-116">-DefaultProfile</span></span>
<span data-ttu-id="a7832-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7832-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7832-118">-Определение</span><span class="sxs-lookup"><span data-stu-id="a7832-118">-Defines</span></span>
<span data-ttu-id="a7832-119">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="a7832-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="a7832-120">-Файл</span><span class="sxs-lookup"><span data-stu-id="a7832-120">-File</span></span>
<span data-ttu-id="a7832-121">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="a7832-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="a7832-122">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="a7832-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="a7832-123">-Файлы</span><span class="sxs-lookup"><span data-stu-id="a7832-123">-Files</span></span>
<span data-ttu-id="a7832-124">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="a7832-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="a7832-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="a7832-125">-InputPath</span></span>
<span data-ttu-id="a7832-126">Задает путь к входным файлам.</span><span class="sxs-lookup"><span data-stu-id="a7832-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="a7832-127">-Сопоставитель</span><span class="sxs-lookup"><span data-stu-id="a7832-127">-Mapper</span></span>
<span data-ttu-id="a7832-128">Указывает имя файла сопоставителя.</span><span class="sxs-lookup"><span data-stu-id="a7832-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="a7832-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a7832-129">-OutputPath</span></span>
<span data-ttu-id="a7832-130">Указывает путь для выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="a7832-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="a7832-131">-Reduce</span><span class="sxs-lookup"><span data-stu-id="a7832-131">-Reducer</span></span>
<span data-ttu-id="a7832-132">Указывает имя файла сокращения.</span><span class="sxs-lookup"><span data-stu-id="a7832-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="a7832-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="a7832-133">-StatusFolder</span></span>
<span data-ttu-id="a7832-134">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="a7832-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="a7832-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7832-135">CommonParameters</span></span>
<span data-ttu-id="a7832-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7832-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7832-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7832-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7832-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7832-138">INPUTS</span></span>

### <span data-ttu-id="a7832-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7832-139">None</span></span>

## <span data-ttu-id="a7832-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7832-140">OUTPUTS</span></span>

### <span data-ttu-id="a7832-141">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="a7832-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="a7832-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7832-142">NOTES</span></span>

## <span data-ttu-id="a7832-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7832-143">RELATED LINKS</span></span>

[<span data-ttu-id="a7832-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="a7832-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


