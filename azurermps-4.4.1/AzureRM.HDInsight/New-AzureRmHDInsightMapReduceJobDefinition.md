---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569436"
---
# <span data-ttu-id="ddb44-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ddb44-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="ddb44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddb44-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb44-103">Создает объект задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ddb44-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddb44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddb44-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb44-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddb44-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb44-106">Командлет **New-AzureRmHDInsightMapReduceJobDefinition** определяет новое задание MapReduce для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ddb44-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ddb44-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddb44-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb44-108">Пример 1: Создание определения задания MapReduce</span><span class="sxs-lookup"><span data-stu-id="ddb44-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="ddb44-109">Эта команда создает определение задания MapReduce.</span><span class="sxs-lookup"><span data-stu-id="ddb44-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="ddb44-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddb44-110">PARAMETERS</span></span>

### <span data-ttu-id="ddb44-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="ddb44-111">-Arguments</span></span>
<span data-ttu-id="ddb44-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="ddb44-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="ddb44-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="ddb44-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="ddb44-114">-ClassName</span><span class="sxs-lookup"><span data-stu-id="ddb44-114">-ClassName</span></span>
<span data-ttu-id="ddb44-115">Указывает класс задания в JAR – файле.</span><span class="sxs-lookup"><span data-stu-id="ddb44-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="ddb44-116">-Определение</span><span class="sxs-lookup"><span data-stu-id="ddb44-116">-Defines</span></span>
<span data-ttu-id="ddb44-117">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="ddb44-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="ddb44-118">-Файлы</span><span class="sxs-lookup"><span data-stu-id="ddb44-118">-Files</span></span>
<span data-ttu-id="ddb44-119">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="ddb44-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="ddb44-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="ddb44-120">-JarFile</span></span>
<span data-ttu-id="ddb44-121">Указывает JAR — файл, который будет использоваться для задания.</span><span class="sxs-lookup"><span data-stu-id="ddb44-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="ddb44-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="ddb44-122">-JobName</span></span>
<span data-ttu-id="ddb44-123">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="ddb44-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="ddb44-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="ddb44-124">-LibJars</span></span>
<span data-ttu-id="ddb44-125">Указывает для задания JARS lib.</span><span class="sxs-lookup"><span data-stu-id="ddb44-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="ddb44-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="ddb44-126">-StatusFolder</span></span>
<span data-ttu-id="ddb44-127">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="ddb44-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="ddb44-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb44-128">-DefaultProfile</span></span>
<span data-ttu-id="ddb44-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb44-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb44-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb44-130">CommonParameters</span></span>
<span data-ttu-id="ddb44-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddb44-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb44-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb44-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb44-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddb44-133">INPUTS</span></span>

## <span data-ttu-id="ddb44-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddb44-134">OUTPUTS</span></span>

### <span data-ttu-id="ddb44-135">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="ddb44-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="ddb44-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddb44-136">NOTES</span></span>

## <span data-ttu-id="ddb44-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddb44-137">RELATED LINKS</span></span>

[<span data-ttu-id="ddb44-138">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="ddb44-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


