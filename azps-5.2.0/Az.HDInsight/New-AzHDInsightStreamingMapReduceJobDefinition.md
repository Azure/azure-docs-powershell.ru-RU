---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: adfa71fb251950f1946b3a43f030ff32b656ec50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412535"
---
# <span data-ttu-id="77b84-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="77b84-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="77b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77b84-102">SYNOPSIS</span></span>
<span data-ttu-id="77b84-103">Создает объект задания Streaming MapReduce.</span><span class="sxs-lookup"><span data-stu-id="77b84-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="77b84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77b84-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77b84-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77b84-105">DESCRIPTION</span></span>
<span data-ttu-id="77b84-106">Cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** определяет объект задания Streaming MapReduce для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="77b84-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="77b84-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77b84-107">EXAMPLES</span></span>

### <span data-ttu-id="77b84-108">Пример 1. Создание определения задания Streaming MapReduce</span><span class="sxs-lookup"><span data-stu-id="77b84-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="77b84-109">Эта команда создает задание Streaming MapReduce.</span><span class="sxs-lookup"><span data-stu-id="77b84-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="77b84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77b84-110">PARAMETERS</span></span>

### <span data-ttu-id="77b84-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="77b84-111">-Arguments</span></span>
<span data-ttu-id="77b84-112">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="77b84-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="77b84-113">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="77b84-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="77b84-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="77b84-114">-CommandEnvironment</span></span>
<span data-ttu-id="77b84-115">Определяет массив переменных среды командной строки, заданный при запуске задания на узлах рабочих узлов.</span><span class="sxs-lookup"><span data-stu-id="77b84-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="77b84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b84-116">-DefaultProfile</span></span>
<span data-ttu-id="77b84-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77b84-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77b84-118">-Определяет</span><span class="sxs-lookup"><span data-stu-id="77b84-118">-Defines</span></span>
<span data-ttu-id="77b84-119">Определяет значения конфигурации Hadoop, заданные для работы задания.</span><span class="sxs-lookup"><span data-stu-id="77b84-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="77b84-120">-File</span><span class="sxs-lookup"><span data-stu-id="77b84-120">-File</span></span>
<span data-ttu-id="77b84-121">Путь к файлу, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="77b84-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="77b84-122">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="77b84-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="77b84-123">-Файлы</span><span class="sxs-lookup"><span data-stu-id="77b84-123">-Files</span></span>
<span data-ttu-id="77b84-124">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="77b84-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="77b84-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="77b84-125">-InputPath</span></span>
<span data-ttu-id="77b84-126">Путь к входным файлам.</span><span class="sxs-lookup"><span data-stu-id="77b84-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="77b84-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="77b84-127">-Mapper</span></span>
<span data-ttu-id="77b84-128">Указывает имя файла Mapper.</span><span class="sxs-lookup"><span data-stu-id="77b84-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="77b84-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="77b84-129">-OutputPath</span></span>
<span data-ttu-id="77b84-130">Путь к выходным данным задания.</span><span class="sxs-lookup"><span data-stu-id="77b84-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="77b84-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="77b84-131">-Reducer</span></span>
<span data-ttu-id="77b84-132">Указывает имя файла с более низой размером.</span><span class="sxs-lookup"><span data-stu-id="77b84-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="77b84-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="77b84-133">-StatusFolder</span></span>
<span data-ttu-id="77b84-134">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="77b84-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="77b84-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b84-135">CommonParameters</span></span>
<span data-ttu-id="77b84-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b84-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b84-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b84-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b84-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77b84-138">INPUTS</span></span>

### <span data-ttu-id="77b84-139">Нет</span><span class="sxs-lookup"><span data-stu-id="77b84-139">None</span></span>

## <span data-ttu-id="77b84-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77b84-140">OUTPUTS</span></span>

### <span data-ttu-id="77b84-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="77b84-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="77b84-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77b84-142">NOTES</span></span>

## <span data-ttu-id="77b84-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77b84-143">RELATED LINKS</span></span>

[<span data-ttu-id="77b84-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="77b84-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


