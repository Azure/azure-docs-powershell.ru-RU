---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: bff9b9d44d8afcbc315293dc07be3592172f1a4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506289"
---
# <span data-ttu-id="176a4-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="176a4-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="176a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176a4-102">SYNOPSIS</span></span>
<span data-ttu-id="176a4-103">Остановка заданного задания в кластере.</span><span class="sxs-lookup"><span data-stu-id="176a4-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="176a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="176a4-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="176a4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="176a4-105">DESCRIPTION</span></span>
<span data-ttu-id="176a4-106">Для запуска указанного задания в кластере Azure **HDInsight** происходит остановка указанного задания.</span><span class="sxs-lookup"><span data-stu-id="176a4-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="176a4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="176a4-107">EXAMPLES</span></span>

### <span data-ttu-id="176a4-108">Пример 1. Остановка задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="176a4-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="176a4-109">Эта команда останавливает задание на кластере "ваш-hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="176a4-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="176a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176a4-110">PARAMETERS</span></span>

### <span data-ttu-id="176a4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="176a4-111">-ClusterName</span></span>
<span data-ttu-id="176a4-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="176a4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="176a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176a4-113">-DefaultProfile</span></span>
<span data-ttu-id="176a4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="176a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="176a4-115">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="176a4-115">-HttpCredential</span></span>
<span data-ttu-id="176a4-116">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="176a4-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="176a4-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="176a4-117">-JobId</span></span>
<span data-ttu-id="176a4-118">Определяет ид задания.</span><span class="sxs-lookup"><span data-stu-id="176a4-118">Specifies the job ID of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="176a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="176a4-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176a4-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="176a4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176a4-121">CommonParameters</span></span>
<span data-ttu-id="176a4-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176a4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176a4-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="176a4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176a4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="176a4-124">INPUTS</span></span>

### <span data-ttu-id="176a4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="176a4-125">System.String</span></span>

## <span data-ttu-id="176a4-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="176a4-126">OUTPUTS</span></span>

### <span data-ttu-id="176a4-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="176a4-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="176a4-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="176a4-128">NOTES</span></span>

## <span data-ttu-id="176a4-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="176a4-129">RELATED LINKS</span></span>

[<span data-ttu-id="176a4-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="176a4-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="176a4-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="176a4-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="176a4-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="176a4-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)


