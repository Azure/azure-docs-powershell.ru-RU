---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079062"
---
# <span data-ttu-id="c26f1-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c26f1-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="c26f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c26f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c26f1-103">Создает объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="c26f1-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="c26f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c26f1-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c26f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26f1-105">DESCRIPTION</span></span>
<span data-ttu-id="c26f1-106">Командлет **New-AzHDInsightMapReduceJobDefinition** определяет новое задание MapReduce для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c26f1-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c26f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c26f1-107">EXAMPLES</span></span>

### <span data-ttu-id="c26f1-108">Пример 1: Создание определения задания MapReduce</span><span class="sxs-lookup"><span data-stu-id="c26f1-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="c26f1-109">Эта команда создает определение задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="c26f1-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="c26f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c26f1-110">PARAMETERS</span></span>

### <span data-ttu-id="c26f1-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="c26f1-111">-Arguments</span></span>
<span data-ttu-id="c26f1-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="c26f1-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="c26f1-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="c26f1-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="c26f1-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="c26f1-114">-ClassName</span></span>
<span data-ttu-id="c26f1-115">Указывает класс задания в JAR – файле.</span><span class="sxs-lookup"><span data-stu-id="c26f1-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="c26f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26f1-116">-DefaultProfile</span></span>
<span data-ttu-id="c26f1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c26f1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c26f1-118">-Определение</span><span class="sxs-lookup"><span data-stu-id="c26f1-118">-Defines</span></span>
<span data-ttu-id="c26f1-119">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="c26f1-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="c26f1-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="c26f1-120">-Files</span></span>
<span data-ttu-id="c26f1-121">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="c26f1-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="c26f1-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="c26f1-122">-JarFile</span></span>
<span data-ttu-id="c26f1-123">Указывает JAR — файл, который будет использоваться для задания.</span><span class="sxs-lookup"><span data-stu-id="c26f1-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="c26f1-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="c26f1-124">-JobName</span></span>
<span data-ttu-id="c26f1-125">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="c26f1-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="c26f1-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="c26f1-126">-LibJars</span></span>
<span data-ttu-id="c26f1-127">Указывает для задания JARS lib.</span><span class="sxs-lookup"><span data-stu-id="c26f1-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="c26f1-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c26f1-128">-StatusFolder</span></span>
<span data-ttu-id="c26f1-129">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="c26f1-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="c26f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26f1-130">CommonParameters</span></span>
<span data-ttu-id="c26f1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c26f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26f1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26f1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26f1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c26f1-133">INPUTS</span></span>

### <span data-ttu-id="c26f1-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="c26f1-134">None</span></span>

## <span data-ttu-id="c26f1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26f1-135">OUTPUTS</span></span>

### <span data-ttu-id="c26f1-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="c26f1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="c26f1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c26f1-137">NOTES</span></span>

## <span data-ttu-id="c26f1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c26f1-138">RELATED LINKS</span></span>

[<span data-ttu-id="c26f1-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c26f1-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

