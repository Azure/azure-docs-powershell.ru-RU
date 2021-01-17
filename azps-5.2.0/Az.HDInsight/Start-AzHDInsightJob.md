---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328274"
---
# <span data-ttu-id="d97ab-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d97ab-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="d97ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d97ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d97ab-103">Запускает задание Azure HDInsight в заданном кластере.</span><span class="sxs-lookup"><span data-stu-id="d97ab-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="d97ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d97ab-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d97ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d97ab-106">Для запуска задания Azure HDInsight в указанном кластере запускается проектлет **Start-AzHDInsightJob.**</span><span class="sxs-lookup"><span data-stu-id="d97ab-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="d97ab-107">Это может быть задание MapReduce, задание Streaming MapReduce, задание "Кот" или задание "Порося".</span><span class="sxs-lookup"><span data-stu-id="d97ab-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="d97ab-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d97ab-108">EXAMPLES</span></span>

### <span data-ttu-id="d97ab-109">Пример 1. Запуск задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="d97ab-109">Example 1: Start a job on the specified cluster</span></span>
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

<span data-ttu-id="d97ab-110">Эта команда запускает задание на кластере "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="d97ab-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d97ab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d97ab-111">PARAMETERS</span></span>

### <span data-ttu-id="d97ab-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d97ab-112">-ClusterName</span></span>
<span data-ttu-id="d97ab-113">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="d97ab-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d97ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97ab-114">-DefaultProfile</span></span>
<span data-ttu-id="d97ab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d97ab-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d97ab-116">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="d97ab-116">-HttpCredential</span></span>
<span data-ttu-id="d97ab-117">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="d97ab-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d97ab-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="d97ab-118">-JobDefinition</span></span>
<span data-ttu-id="d97ab-119">Задание начинается с кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d97ab-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

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

### <span data-ttu-id="d97ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d97ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="d97ab-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d97ab-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d97ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97ab-122">CommonParameters</span></span>
<span data-ttu-id="d97ab-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97ab-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97ab-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97ab-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d97ab-125">INPUTS</span></span>

### <span data-ttu-id="d97ab-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d97ab-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="d97ab-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d97ab-127">OUTPUTS</span></span>

### <span data-ttu-id="d97ab-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d97ab-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="d97ab-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d97ab-129">NOTES</span></span>

## <span data-ttu-id="d97ab-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d97ab-130">RELATED LINKS</span></span>

[<span data-ttu-id="d97ab-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d97ab-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="d97ab-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d97ab-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="d97ab-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d97ab-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="d97ab-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d97ab-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


