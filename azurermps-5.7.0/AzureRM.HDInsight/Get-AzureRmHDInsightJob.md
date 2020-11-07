---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: AFE90092-8B25-4897-8D3A-3E732CC5CBA6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJob.md
ms.openlocfilehash: 2fa3ae6cd48887f377ea4bdb6ce36001afe29b5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732526"
---
# <span data-ttu-id="9c313-101">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9c313-101">Get-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="9c313-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c313-102">SYNOPSIS</span></span>
<span data-ttu-id="9c313-103">Получает список заданий из кластера и перечисляет их в обратном хронологическом порядке или извлекает конкретное задание.</span><span class="sxs-lookup"><span data-stu-id="9c313-103">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c313-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c313-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJob [-ClusterName] <String> [-HttpCredential] <PSCredential> [[-JobId] <String>]
 [-NumOfJobs <Int32>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c313-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c313-105">DESCRIPTION</span></span>
<span data-ttu-id="9c313-106">Командлет **Get-AzureRmHDInsightJob** получает последние задания для указанного кластера Azure HDInsight в обратном хронологическом порядке, но самое последнее задание в верхней части списка.</span><span class="sxs-lookup"><span data-stu-id="9c313-106">The **Get-AzureRmHDInsightJob** cmdlet gets recent jobs for a specified Azure HDInsight cluster in reverse chronological order, with the most recent job at the top of the list.</span></span>
<span data-ttu-id="9c313-107">Чтобы получить определенное задание, предоставьте параметр *JOBID* .</span><span class="sxs-lookup"><span data-stu-id="9c313-107">Get a specific job by providing the *JobId* parameter.</span></span>

## <span data-ttu-id="9c313-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c313-108">EXAMPLES</span></span>

### <span data-ttu-id="9c313-109">Пример 1: получение недавних заданий для указанного кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="9c313-109">Example 1: Get recent jobs for a specified Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="9c313-110">Эта команда получает все недавние задания для кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9c313-110">This command gets all recent jobs for the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9c313-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c313-111">PARAMETERS</span></span>

### <span data-ttu-id="9c313-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="9c313-112">-ClusterName</span></span>
<span data-ttu-id="9c313-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9c313-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c313-114">-DefaultProfile</span></span>
<span data-ttu-id="9c313-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9c313-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c313-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="9c313-116">-HttpCredential</span></span>
<span data-ttu-id="9c313-117">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="9c313-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c313-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="9c313-118">-JobId</span></span>
<span data-ttu-id="9c313-119">Указывает код задания для задания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9c313-119">Specifies the job ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c313-120">-NumOfJobs</span><span class="sxs-lookup"><span data-stu-id="9c313-120">-NumOfJobs</span></span>
<span data-ttu-id="9c313-121">Указывает количество извлекаемых заданий.</span><span class="sxs-lookup"><span data-stu-id="9c313-121">Specifies the number of jobs to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c313-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c313-122">-ResourceGroupName</span></span>
<span data-ttu-id="9c313-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c313-123">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c313-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c313-124">CommonParameters</span></span>
<span data-ttu-id="9c313-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c313-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c313-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c313-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c313-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c313-127">INPUTS</span></span>

### <span data-ttu-id="9c313-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c313-128">None</span></span>
<span data-ttu-id="9c313-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c313-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c313-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c313-130">OUTPUTS</span></span>

### <span data-ttu-id="9c313-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9c313-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="9c313-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c313-132">NOTES</span></span>

## <span data-ttu-id="9c313-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c313-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c313-134">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="9c313-134">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="9c313-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9c313-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="9c313-136">Остановить-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9c313-136">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="9c313-137">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="9c313-137">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


