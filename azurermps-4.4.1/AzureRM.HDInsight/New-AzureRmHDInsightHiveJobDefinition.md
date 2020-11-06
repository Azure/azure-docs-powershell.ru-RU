---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: fd933d157748de424aa425179701897772d93569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569443"
---
# <span data-ttu-id="086c1-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="086c1-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="086c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="086c1-102">SYNOPSIS</span></span>
<span data-ttu-id="086c1-103">Создание объекта задания куста.</span><span class="sxs-lookup"><span data-stu-id="086c1-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="086c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="086c1-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="086c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="086c1-105">DESCRIPTION</span></span>
<span data-ttu-id="086c1-106">Командлет **New-AzureRmHDInsightHiveJobDefinition** определяет объект задания куста для использования с кластером Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="086c1-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="086c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="086c1-107">EXAMPLES</span></span>

### <span data-ttu-id="086c1-108">Пример 1: Создание определения задания куста</span><span class="sxs-lookup"><span data-stu-id="086c1-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="086c1-109">Эта команда создает определение задания куста.</span><span class="sxs-lookup"><span data-stu-id="086c1-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="086c1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="086c1-110">PARAMETERS</span></span>

### <span data-ttu-id="086c1-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="086c1-111">-Arguments</span></span>
<span data-ttu-id="086c1-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="086c1-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="086c1-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="086c1-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="086c1-114">-Определение</span><span class="sxs-lookup"><span data-stu-id="086c1-114">-Defines</span></span>
<span data-ttu-id="086c1-115">Задает значения конфигурации Hadoop, которые должны быть заданы при запуске задания.</span><span class="sxs-lookup"><span data-stu-id="086c1-115">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="086c1-116">-Файл</span><span class="sxs-lookup"><span data-stu-id="086c1-116">-File</span></span>
<span data-ttu-id="086c1-117">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="086c1-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="086c1-118">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="086c1-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="086c1-119">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="086c1-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="086c1-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="086c1-120">-Files</span></span>
<span data-ttu-id="086c1-121">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="086c1-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="086c1-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="086c1-122">-JobName</span></span>
<span data-ttu-id="086c1-123">Указывает имя задания.</span><span class="sxs-lookup"><span data-stu-id="086c1-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="086c1-124">-Query</span><span class="sxs-lookup"><span data-stu-id="086c1-124">-Query</span></span>
<span data-ttu-id="086c1-125">Указывает запрос Hive.</span><span class="sxs-lookup"><span data-stu-id="086c1-125">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="086c1-126">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="086c1-126">-RunAsFileJob</span></span>
<span data-ttu-id="086c1-127">Указывает на то, что этот командлет создает файл в учетной записи хранения Azure по умолчанию, в которой будет храниться запрос.</span><span class="sxs-lookup"><span data-stu-id="086c1-127">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="086c1-128">Этот командлет отправляет задание, которое ссылается на этот файл, как сценарий для запуска.</span><span class="sxs-lookup"><span data-stu-id="086c1-128">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="086c1-129">С помощью этой функции можно обрабатывать специальные символы, такие как знак процента (%) Это может привести к сбою отправки задания через Templeton, поскольку Templeton интерпретирует запрос с символом процента в качестве параметра URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="086c1-129">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="086c1-130">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="086c1-130">-StatusFolder</span></span>
<span data-ttu-id="086c1-131">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="086c1-131">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="086c1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086c1-132">-DefaultProfile</span></span>
<span data-ttu-id="086c1-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="086c1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="086c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086c1-134">CommonParameters</span></span>
<span data-ttu-id="086c1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="086c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086c1-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086c1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086c1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="086c1-137">INPUTS</span></span>

## <span data-ttu-id="086c1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="086c1-138">OUTPUTS</span></span>

### <span data-ttu-id="086c1-139">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="086c1-139">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="086c1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="086c1-140">NOTES</span></span>

## <span data-ttu-id="086c1-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="086c1-141">RELATED LINKS</span></span>

[<span data-ttu-id="086c1-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="086c1-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


