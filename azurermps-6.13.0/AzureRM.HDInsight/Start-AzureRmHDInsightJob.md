---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/start-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Start-AzureRmHDInsightJob.md
ms.openlocfilehash: 38eb1a7468b56507c5e5f2c0f68f04f1a1d2020d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734407"
---
# <span data-ttu-id="6f426-101">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6f426-101">Start-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="6f426-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f426-102">SYNOPSIS</span></span>
<span data-ttu-id="6f426-103">Запускает определенное задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="6f426-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f426-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f426-104">SYNTAX</span></span>

```
Start-AzureRmHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f426-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f426-105">DESCRIPTION</span></span>
<span data-ttu-id="6f426-106">Командлет **Start-AzureRMHDInsightJob** запускает определенное задание Azure HDInsight в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="6f426-106">The **Start-AzureRMHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="6f426-107">Это может быть задание MapReduce, Потоковая обработка MapReduce, задание куста или задание свинья.</span><span class="sxs-lookup"><span data-stu-id="6f426-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="6f426-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f426-108">EXAMPLES</span></span>

### <span data-ttu-id="6f426-109">Пример 1: запуск задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="6f426-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="6f426-110">Эта команда запускает задание в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="6f426-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6f426-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f426-111">PARAMETERS</span></span>

### <span data-ttu-id="6f426-112">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="6f426-112">-ClusterName</span></span>
<span data-ttu-id="6f426-113">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6f426-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6f426-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f426-114">-DefaultProfile</span></span>
<span data-ttu-id="6f426-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6f426-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f426-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="6f426-116">-HttpCredential</span></span>
<span data-ttu-id="6f426-117">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="6f426-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="6f426-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="6f426-118">-JobDefinition</span></span>
<span data-ttu-id="6f426-119">Указывает задание для запуска в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="6f426-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="6f426-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f426-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f426-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f426-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6f426-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f426-122">CommonParameters</span></span>
<span data-ttu-id="6f426-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f426-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f426-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f426-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f426-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f426-125">INPUTS</span></span>

### <span data-ttu-id="6f426-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6f426-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>
<span data-ttu-id="6f426-127">Параметры: JobDefinition (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6f426-127">Parameters: JobDefinition (ByValue)</span></span>

## <span data-ttu-id="6f426-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f426-128">OUTPUTS</span></span>

### <span data-ttu-id="6f426-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6f426-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="6f426-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f426-130">NOTES</span></span>

## <span data-ttu-id="6f426-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f426-131">RELATED LINKS</span></span>

[<span data-ttu-id="6f426-132">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6f426-132">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="6f426-133">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="6f426-133">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="6f426-134">Остановить-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6f426-134">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)

[<span data-ttu-id="6f426-135">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="6f426-135">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


