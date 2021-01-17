---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322983"
---
# <span data-ttu-id="191a7-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="191a7-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="191a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="191a7-102">SYNOPSIS</span></span>
<span data-ttu-id="191a7-103">Создает объект задания "Вирус".</span><span class="sxs-lookup"><span data-stu-id="191a7-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="191a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="191a7-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="191a7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="191a7-105">DESCRIPTION</span></span>
<span data-ttu-id="191a7-106">Для использования с кластером Azure **HDInsightJobDefinition используется объект задания New-AzHDInsightJobDefinition.**</span><span class="sxs-lookup"><span data-stu-id="191a7-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="191a7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="191a7-107">EXAMPLES</span></span>

### <span data-ttu-id="191a7-108">Пример 1. Создание определения задания "Задания " в качестве примера"</span><span class="sxs-lookup"><span data-stu-id="191a7-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="191a7-109">Эта команда создает определение задания "Вирус".</span><span class="sxs-lookup"><span data-stu-id="191a7-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="191a7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="191a7-110">PARAMETERS</span></span>

### <span data-ttu-id="191a7-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="191a7-111">-Arguments</span></span>
<span data-ttu-id="191a7-112">Указывает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="191a7-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="191a7-113">Аргументы передаются каждой задаче в качестве аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="191a7-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="191a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191a7-114">-DefaultProfile</span></span>
<span data-ttu-id="191a7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="191a7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="191a7-116">-Определяет</span><span class="sxs-lookup"><span data-stu-id="191a7-116">-Defines</span></span>
<span data-ttu-id="191a7-117">Определяет значения конфигурации Hadoop, заданные для работы задания.</span><span class="sxs-lookup"><span data-stu-id="191a7-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="191a7-118">-File</span><span class="sxs-lookup"><span data-stu-id="191a7-118">-File</span></span>
<span data-ttu-id="191a7-119">Путь к файлу, который содержит запрос, который нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="191a7-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="191a7-120">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="191a7-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="191a7-121">Этот параметр можно использовать вместо *параметра Query.*</span><span class="sxs-lookup"><span data-stu-id="191a7-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="191a7-122">-Файлы</span><span class="sxs-lookup"><span data-stu-id="191a7-122">-Files</span></span>
<span data-ttu-id="191a7-123">Набор файлов, связанных с заданием "Файл".</span><span class="sxs-lookup"><span data-stu-id="191a7-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="191a7-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="191a7-124">-JobName</span></span>
<span data-ttu-id="191a7-125">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="191a7-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="191a7-126">-Query</span><span class="sxs-lookup"><span data-stu-id="191a7-126">-Query</span></span>
<span data-ttu-id="191a7-127">Указывает запрос на это.</span><span class="sxs-lookup"><span data-stu-id="191a7-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="191a7-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="191a7-128">-RunAsFileJob</span></span>
<span data-ttu-id="191a7-129">Указывает на то, что этот cmdlet создает файл в учетной записи хранилища Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="191a7-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="191a7-130">Этот cmdlet submits the job that references this file as a script to run.</span><span class="sxs-lookup"><span data-stu-id="191a7-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="191a7-131">Эта функция позволяет обрабатывать специальные знаки, например знак процента (%). которые не будут работать при отправке задания через Templeton, так как Templeton интерпретирует запрос со знаком процента как URL-параметр.</span><span class="sxs-lookup"><span data-stu-id="191a7-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="191a7-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="191a7-132">-StatusFolder</span></span>
<span data-ttu-id="191a7-133">Определяет расположение папки, которая содержит стандартные выходные данные и результаты ошибок для задания.</span><span class="sxs-lookup"><span data-stu-id="191a7-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="191a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191a7-134">CommonParameters</span></span>
<span data-ttu-id="191a7-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191a7-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191a7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191a7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="191a7-137">INPUTS</span></span>

### <span data-ttu-id="191a7-138">Нет</span><span class="sxs-lookup"><span data-stu-id="191a7-138">None</span></span>

## <span data-ttu-id="191a7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="191a7-139">OUTPUTS</span></span>

### <span data-ttu-id="191a7-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="191a7-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="191a7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="191a7-141">NOTES</span></span>

## <span data-ttu-id="191a7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="191a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="191a7-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="191a7-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


