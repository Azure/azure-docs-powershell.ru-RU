---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: d6ab15fffd71776188291c58f2e21bbee5f27423
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234292"
---
# <span data-ttu-id="45833-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="45833-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="45833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45833-102">SYNOPSIS</span></span>
<span data-ttu-id="45833-103">Создание объекта задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="45833-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="45833-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45833-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45833-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45833-105">DESCRIPTION</span></span>
<span data-ttu-id="45833-106">Для использования с кластером Azure **HDInsightMapReduceJobDefinition** определено новое задание MapReduce.</span><span class="sxs-lookup"><span data-stu-id="45833-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="45833-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45833-107">EXAMPLES</span></span>

### <span data-ttu-id="45833-108">Пример 1. Создание определения задания MapReduce</span><span class="sxs-lookup"><span data-stu-id="45833-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="45833-109">Эта команда создает определение задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="45833-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="45833-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45833-110">PARAMETERS</span></span>

### <span data-ttu-id="45833-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="45833-111">-Arguments</span></span>
<span data-ttu-id="45833-112">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="45833-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="45833-113">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="45833-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="45833-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="45833-114">-ClassName</span></span>
<span data-ttu-id="45833-115">Класс задания в JAR-файле.</span><span class="sxs-lookup"><span data-stu-id="45833-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="45833-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45833-116">-DefaultProfile</span></span>
<span data-ttu-id="45833-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="45833-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45833-118">-Определяет</span><span class="sxs-lookup"><span data-stu-id="45833-118">-Defines</span></span>
<span data-ttu-id="45833-119">Определяет значения конфигурации Hadoop, заданные для работы задания.</span><span class="sxs-lookup"><span data-stu-id="45833-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="45833-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="45833-120">-Files</span></span>
<span data-ttu-id="45833-121">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="45833-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="45833-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="45833-122">-JarFile</span></span>
<span data-ttu-id="45833-123">Указывает JAR-файл, который будет использовать для задания.</span><span class="sxs-lookup"><span data-stu-id="45833-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="45833-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="45833-124">-JobName</span></span>
<span data-ttu-id="45833-125">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="45833-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="45833-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="45833-126">-LibJars</span></span>
<span data-ttu-id="45833-127">Определяет, является ли lib JARS для задания.</span><span class="sxs-lookup"><span data-stu-id="45833-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="45833-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="45833-128">-StatusFolder</span></span>
<span data-ttu-id="45833-129">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="45833-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="45833-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45833-130">CommonParameters</span></span>
<span data-ttu-id="45833-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45833-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45833-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45833-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45833-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45833-133">INPUTS</span></span>

### <span data-ttu-id="45833-134">Нет</span><span class="sxs-lookup"><span data-stu-id="45833-134">None</span></span>

## <span data-ttu-id="45833-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45833-135">OUTPUTS</span></span>

### <span data-ttu-id="45833-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="45833-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="45833-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45833-137">NOTES</span></span>

## <span data-ttu-id="45833-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45833-138">RELATED LINKS</span></span>

[<span data-ttu-id="45833-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="45833-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


