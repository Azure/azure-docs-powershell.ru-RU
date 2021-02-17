---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 4f9fe1ef3ab16812553eb6ea22909ce37bd5ee69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234281"
---
# <span data-ttu-id="ca78c-101">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ca78c-101">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="ca78c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca78c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca78c-103">Создает объект задания Streaming MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ca78c-103">Creates a Streaming MapReduce job object.</span></span>

## <span data-ttu-id="ca78c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca78c-104">SYNTAX</span></span>

```
New-AzHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>] [-Files <String[]>]
 [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>] -InputPath <String>
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca78c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca78c-105">DESCRIPTION</span></span>
<span data-ttu-id="ca78c-106">Cmdlet **New-AzHDInsightStreamingMapReduceJobDefinition** определяет объект задания Streaming MapReduce для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ca78c-106">The **New-AzHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ca78c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca78c-107">EXAMPLES</span></span>

### <span data-ttu-id="ca78c-108">Пример 1. Создание определения задания Streaming MapReduce</span><span class="sxs-lookup"><span data-stu-id="ca78c-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="ca78c-109">Эта команда создает задание Streaming MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ca78c-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="ca78c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca78c-110">PARAMETERS</span></span>

### <span data-ttu-id="ca78c-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="ca78c-111">-Arguments</span></span>
<span data-ttu-id="ca78c-112">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="ca78c-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="ca78c-113">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="ca78c-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="ca78c-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="ca78c-114">-CommandEnvironment</span></span>
<span data-ttu-id="ca78c-115">Определяет массив переменных среды командной строки, заданный при запуске задания на узлах рабочих узлов.</span><span class="sxs-lookup"><span data-stu-id="ca78c-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="ca78c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca78c-116">-DefaultProfile</span></span>
<span data-ttu-id="ca78c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ca78c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca78c-118">-Определяет</span><span class="sxs-lookup"><span data-stu-id="ca78c-118">-Defines</span></span>
<span data-ttu-id="ca78c-119">Определяет значения конфигурации Hadoop, заданные для работы задания.</span><span class="sxs-lookup"><span data-stu-id="ca78c-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="ca78c-120">-File</span><span class="sxs-lookup"><span data-stu-id="ca78c-120">-File</span></span>
<span data-ttu-id="ca78c-121">Путь к файлу, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="ca78c-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="ca78c-122">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="ca78c-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="ca78c-123">-Файлы</span><span class="sxs-lookup"><span data-stu-id="ca78c-123">-Files</span></span>
<span data-ttu-id="ca78c-124">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="ca78c-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="ca78c-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="ca78c-125">-InputPath</span></span>
<span data-ttu-id="ca78c-126">Путь к входным файлам.</span><span class="sxs-lookup"><span data-stu-id="ca78c-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="ca78c-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="ca78c-127">-Mapper</span></span>
<span data-ttu-id="ca78c-128">Указывает имя файла Mapper.</span><span class="sxs-lookup"><span data-stu-id="ca78c-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="ca78c-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ca78c-129">-OutputPath</span></span>
<span data-ttu-id="ca78c-130">Путь к выходным данным задания.</span><span class="sxs-lookup"><span data-stu-id="ca78c-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="ca78c-131">-Reducer</span><span class="sxs-lookup"><span data-stu-id="ca78c-131">-Reducer</span></span>
<span data-ttu-id="ca78c-132">Указывает имя файла с более низой размером.</span><span class="sxs-lookup"><span data-stu-id="ca78c-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="ca78c-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ca78c-133">-StatusFolder</span></span>
<span data-ttu-id="ca78c-134">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="ca78c-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="ca78c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca78c-135">CommonParameters</span></span>
<span data-ttu-id="ca78c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca78c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca78c-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca78c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca78c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca78c-138">INPUTS</span></span>

### <span data-ttu-id="ca78c-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ca78c-139">None</span></span>

## <span data-ttu-id="ca78c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca78c-140">OUTPUTS</span></span>

### <span data-ttu-id="ca78c-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ca78c-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="ca78c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca78c-142">NOTES</span></span>

## <span data-ttu-id="ca78c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca78c-143">RELATED LINKS</span></span>

[<span data-ttu-id="ca78c-144">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ca78c-144">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


