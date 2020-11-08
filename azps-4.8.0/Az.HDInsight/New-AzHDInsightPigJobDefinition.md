---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: B9BA5FD1-A4F8-4E24-8FCB-847649B82AB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightpigjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightPigJobDefinition.md
ms.openlocfilehash: d9ea9152844db82d345ba1f6f50305b33975ced4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079061"
---
# <span data-ttu-id="3f9d3-101">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3f9d3-101">New-AzHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="3f9d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9d3-103">Создает объект задания свинья.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-103">Creates a Pig job object.</span></span>

## <span data-ttu-id="3f9d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f9d3-104">SYNTAX</span></span>

```
New-AzHDInsightPigJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-File <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f9d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f9d3-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9d3-106">Командлет **New-AzHDInsightPigJobDefinition** определяет объект задания свинья для использования с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-106">The **New-AzHDInsightPigJobDefinition** cmdlet defines a Pig job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3f9d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f9d3-107">EXAMPLES</span></span>

### <span data-ttu-id="3f9d3-108">Пример 1: Создание определения задания свинья</span><span class="sxs-lookup"><span data-stu-id="3f9d3-108">Example 1: Create a Pig job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Pig job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightPigJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="3f9d3-109">Эта команда создает определение задания свинья.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-109">This command creates a Pig job definition.</span></span>

## <span data-ttu-id="3f9d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f9d3-110">PARAMETERS</span></span>

### <span data-ttu-id="3f9d3-111">-Аргументы</span><span class="sxs-lookup"><span data-stu-id="3f9d3-111">-Arguments</span></span>
<span data-ttu-id="3f9d3-112">Задает массив аргументов для задания.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="3f9d3-113">Аргументы передаются в качестве аргументов командной строки для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="3f9d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9d3-114">-DefaultProfile</span></span>
<span data-ttu-id="3f9d3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f9d3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f9d3-116">-Файл</span><span class="sxs-lookup"><span data-stu-id="3f9d3-116">-File</span></span>
<span data-ttu-id="3f9d3-117">Задает путь к файлу, содержащему запрос для запуска.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-117">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="3f9d3-118">Файл должен быть доступен в учетной записи хранения, связанной с кластером.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-118">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="3f9d3-119">Вы можете использовать этот параметр вместо параметра *запроса* .</span><span class="sxs-lookup"><span data-stu-id="3f9d3-119">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="3f9d3-120">-Файлы</span><span class="sxs-lookup"><span data-stu-id="3f9d3-120">-Files</span></span>
<span data-ttu-id="3f9d3-121">Указывает набор файлов, связанных с заданием куста.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="3f9d3-122">-Query</span><span class="sxs-lookup"><span data-stu-id="3f9d3-122">-Query</span></span>
<span data-ttu-id="3f9d3-123">Указывает запрос свинья.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-123">Specifies the Pig query.</span></span>

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

### <span data-ttu-id="3f9d3-124">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="3f9d3-124">-StatusFolder</span></span>
<span data-ttu-id="3f9d3-125">Указывает расположение папки, содержащей стандартные выходные данные и выходные ошибки для задания.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-125">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="3f9d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9d3-126">CommonParameters</span></span>
<span data-ttu-id="3f9d3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f9d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9d3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f9d3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9d3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f9d3-129">INPUTS</span></span>

### <span data-ttu-id="3f9d3-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3f9d3-130">None</span></span>

## <span data-ttu-id="3f9d3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f9d3-131">OUTPUTS</span></span>

### <span data-ttu-id="3f9d3-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="3f9d3-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightPigJobDefinition</span></span>

## <span data-ttu-id="3f9d3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f9d3-133">NOTES</span></span>

## <span data-ttu-id="3f9d3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f9d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f9d3-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="3f9d3-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


