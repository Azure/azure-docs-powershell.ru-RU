---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912991"
---
# <span data-ttu-id="10c15-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10c15-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="10c15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10c15-102">SYNOPSIS</span></span>
<span data-ttu-id="10c15-103">Создает объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="10c15-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="10c15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10c15-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10c15-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10c15-105">DESCRIPTION</span></span>
<span data-ttu-id="10c15-106">Командлет **New-AzHDInsightMapReduceJobDefinition** определяет новое задание MapReduce для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="10c15-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="10c15-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10c15-107">EXAMPLES</span></span>

### <span data-ttu-id="10c15-108">Пример 1: Создание определения задания MapReduce</span><span class="sxs-lookup"><span data-stu-id="10c15-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="10c15-109">Эта команда создает определение задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="10c15-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="10c15-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10c15-110">PARAMETERS</span></span>

### <span data-ttu-id="10c15-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="10c15-111">-Arguments</span></span>
<span data-ttu-id="10c15-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="10c15-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="10c15-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="10c15-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="10c15-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="10c15-114">-ClassName</span></span>
<span data-ttu-id="10c15-115">Указывает класс задания в JAR – файле.</span><span class="sxs-lookup"><span data-stu-id="10c15-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="10c15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c15-116">-DefaultProfile</span></span>
<span data-ttu-id="10c15-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10c15-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10c15-118">-Определение</span><span class="sxs-lookup"><span data-stu-id="10c15-118">-Defines</span></span>
<span data-ttu-id="10c15-119">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="10c15-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="10c15-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="10c15-120">-Files</span></span>
<span data-ttu-id="10c15-121">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="10c15-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="10c15-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="10c15-122">-JarFile</span></span>
<span data-ttu-id="10c15-123">Указывает JAR — файл, который будет использоваться для задания.</span><span class="sxs-lookup"><span data-stu-id="10c15-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="10c15-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="10c15-124">-JobName</span></span>
<span data-ttu-id="10c15-125">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="10c15-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="10c15-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="10c15-126">-LibJars</span></span>
<span data-ttu-id="10c15-127">Указывает для задания JARS lib.</span><span class="sxs-lookup"><span data-stu-id="10c15-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="10c15-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="10c15-128">-StatusFolder</span></span>
<span data-ttu-id="10c15-129">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="10c15-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="10c15-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c15-130">CommonParameters</span></span>
<span data-ttu-id="10c15-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10c15-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c15-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c15-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c15-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10c15-133">INPUTS</span></span>

### <span data-ttu-id="10c15-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="10c15-134">None</span></span>

## <span data-ttu-id="10c15-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10c15-135">OUTPUTS</span></span>

### <span data-ttu-id="10c15-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="10c15-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="10c15-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="10c15-137">NOTES</span></span>

## <span data-ttu-id="10c15-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10c15-138">RELATED LINKS</span></span>

[<span data-ttu-id="10c15-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="10c15-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


