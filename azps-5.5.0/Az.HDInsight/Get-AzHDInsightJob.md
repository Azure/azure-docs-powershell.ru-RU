---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: dc7f69ef29d7e5396ad57346380decc672f83db5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219948"
---
# <span data-ttu-id="9ce45-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ce45-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="9ce45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ce45-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce45-103">Возвращает список заданий из кластера и перечислены в обратном хронологическом порядке или получают определенное задание.</span><span class="sxs-lookup"><span data-stu-id="9ce45-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="9ce45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ce45-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ce45-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ce45-105">DESCRIPTION</span></span>
<span data-ttu-id="9ce45-106">С **помощью cmdlet Get-AzHDInsightJob** можно получить последние задания для указанного кластера Azure HDInsight в обратном хронологическом порядке (последнее задание выведется вверху списка).</span><span class="sxs-lookup"><span data-stu-id="9ce45-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="9ce45-107">Получите задание, задав параметр *JobId.*</span><span class="sxs-lookup"><span data-stu-id="9ce45-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="9ce45-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ce45-108">EXAMPLES</span></span>

### <span data-ttu-id="9ce45-109">Пример 1. Получить последние задания для указанного кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="9ce45-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="9ce45-110">Эта команда получает все последние задания для кластера hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9ce45-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9ce45-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ce45-111">PARAMETERS</span></span>

### <span data-ttu-id="9ce45-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9ce45-112">-ClusterName</span></span>
<span data-ttu-id="9ce45-113">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="9ce45-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce45-114">-DefaultProfile</span></span>
<span data-ttu-id="9ce45-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ce45-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ce45-116">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="9ce45-116">-HttpCredential</span></span>
<span data-ttu-id="9ce45-117">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="9ce45-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce45-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="9ce45-118">-JobId</span></span>
<span data-ttu-id="9ce45-119">Определяет ИД задания, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="9ce45-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce45-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="9ce45-120">-NumOfJobs</span></span>
<span data-ttu-id="9ce45-121">Количество извлечения заданий.</span><span class="sxs-lookup"><span data-stu-id="9ce45-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce45-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce45-122">-ResourceGroupName</span></span>
<span data-ttu-id="9ce45-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ce45-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9ce45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce45-124">CommonParameters</span></span>
<span data-ttu-id="9ce45-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce45-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ce45-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce45-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ce45-127">INPUTS</span></span>

### <span data-ttu-id="9ce45-128">Нет</span><span class="sxs-lookup"><span data-stu-id="9ce45-128">None</span></span>

## <span data-ttu-id="9ce45-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ce45-129">OUTPUTS</span></span>

### <span data-ttu-id="9ce45-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ce45-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="9ce45-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ce45-131">NOTES</span></span>

## <span data-ttu-id="9ce45-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ce45-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ce45-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9ce45-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="9ce45-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ce45-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="9ce45-135">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ce45-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="9ce45-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9ce45-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


