---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 54fb8305b14272fb34b6329cf057372da7c42a88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720796"
---
# <span data-ttu-id="b8d89-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b8d89-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="b8d89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8d89-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d89-103">Запускает определенное задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="b8d89-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="b8d89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8d89-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8d89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8d89-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d89-106">Командлет **Start-AzHDInsightJob** запускает определенное задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="b8d89-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="b8d89-107">Это может быть задание MapReduce, Потоковая обработка MapReduce, задание куста или задание свинья.</span><span class="sxs-lookup"><span data-stu-id="b8d89-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="b8d89-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8d89-108">EXAMPLES</span></span>

### <span data-ttu-id="b8d89-109">Пример 1: запуск задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="b8d89-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b8d89-110">Эта команда запускает задание в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b8d89-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b8d89-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8d89-111">PARAMETERS</span></span>

### <span data-ttu-id="b8d89-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="b8d89-112">-ClusterName</span></span>
<span data-ttu-id="b8d89-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b8d89-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b8d89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d89-114">-DefaultProfile</span></span>
<span data-ttu-id="b8d89-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8d89-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8d89-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="b8d89-116">-HttpCredential</span></span>
<span data-ttu-id="b8d89-117">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="b8d89-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d89-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="b8d89-118">-JobDefinition</span></span>
<span data-ttu-id="b8d89-119">Указывает задание для запуска в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d89-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d89-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d89-120">-ResourceGroupName</span></span>
<span data-ttu-id="b8d89-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8d89-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b8d89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d89-122">CommonParameters</span></span>
<span data-ttu-id="b8d89-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8d89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d89-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8d89-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d89-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8d89-125">INPUTS</span></span>

### <span data-ttu-id="b8d89-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b8d89-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="b8d89-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8d89-127">OUTPUTS</span></span>

### <span data-ttu-id="b8d89-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b8d89-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="b8d89-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8d89-129">NOTES</span></span>

## <span data-ttu-id="b8d89-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8d89-130">RELATED LINKS</span></span>

[<span data-ttu-id="b8d89-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b8d89-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="b8d89-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b8d89-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="b8d89-133">Остановить-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b8d89-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="b8d89-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b8d89-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


