---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJob.md
ms.openlocfilehash: b2ba2144eccd3069453daa1ada15527539400c22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245369"
---
# <span data-ttu-id="494d9-101">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="494d9-101">Get-AzHDInsightJob</span></span>

## <span data-ttu-id="494d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="494d9-102">SYNOPSIS</span></span>
<span data-ttu-id="494d9-103">Получает список заданий из кластера и перечисляет их в обратном хронологическом порядке или извлекает конкретное задание.</span><span class="sxs-lookup"><span data-stu-id="494d9-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

## <span data-ttu-id="494d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="494d9-104">SYNTAX</span></span>

```
Get-AzHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="494d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="494d9-105">DESCRIPTION</span></span>
<span data-ttu-id="494d9-106">Командлет **Get-AzHDInsightJob** получает последние задания для указанного кластера Azure HDInsight в обратном хронологическом порядке, но самое последнее задание в верхней части списка.</span><span class="sxs-lookup"><span data-stu-id="494d9-106">The **Get-AzHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="494d9-107">Чтобы получить определенное задание, предоставьте параметр *JOBID* .</span><span class="sxs-lookup"><span data-stu-id="494d9-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="494d9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="494d9-108">EXAMPLES</span></span>

### <span data-ttu-id="494d9-109">Пример 1: получение недавних заданий для указанного кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="494d9-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
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

<span data-ttu-id="494d9-110">Эта команда получает все недавние задания для кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="494d9-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="494d9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="494d9-111">PARAMETERS</span></span>

### <span data-ttu-id="494d9-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="494d9-112">-ClusterName</span></span>
<span data-ttu-id="494d9-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="494d9-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="494d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="494d9-114">-DefaultProfile</span></span>
<span data-ttu-id="494d9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="494d9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="494d9-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="494d9-116">-HttpCredential</span></span>
<span data-ttu-id="494d9-117">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="494d9-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="494d9-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="494d9-118">-JobId</span></span>
<span data-ttu-id="494d9-119">Указывает код задания для задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="494d9-119">Specifies the job ID of the job to get.</span></span>

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

### <span data-ttu-id="494d9-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="494d9-120">-NumOfJobs</span></span>
<span data-ttu-id="494d9-121">Указывает количество извлекаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="494d9-121">Specifies the number of jobs to retrieve.</span></span>

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

### <span data-ttu-id="494d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="494d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="494d9-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="494d9-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="494d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="494d9-124">CommonParameters</span></span>
<span data-ttu-id="494d9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="494d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="494d9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="494d9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="494d9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="494d9-127">INPUTS</span></span>

### <span data-ttu-id="494d9-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="494d9-128">None</span></span>

## <span data-ttu-id="494d9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="494d9-129">OUTPUTS</span></span>

### <span data-ttu-id="494d9-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="494d9-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="494d9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="494d9-131">NOTES</span></span>

## <span data-ttu-id="494d9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="494d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="494d9-133">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="494d9-133">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="494d9-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="494d9-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="494d9-135">Остановить-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="494d9-135">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="494d9-136">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="494d9-136">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)

