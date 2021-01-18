---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: 4c1d991d3236c8e631b2b5c7f0026e91af2f8cf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506279"
---
# <span data-ttu-id="5ffab-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5ffab-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="5ffab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ffab-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffab-103">Ожидание завершения или сбоя определенного задания.</span><span class="sxs-lookup"><span data-stu-id="5ffab-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="5ffab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ffab-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ffab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ffab-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffab-106">Для выполнения задания Azure HDInsight вы ожидаете завершения или сбоя задания **Wait-AzHDInsightJob.**</span><span class="sxs-lookup"><span data-stu-id="5ffab-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="5ffab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ffab-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffab-108">Пример 1. Ожидание завершения или сбоя задания</span><span class="sxs-lookup"><span data-stu-id="5ffab-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="5ffab-109">Эта команда ждет завершения или сбоя задания.</span><span class="sxs-lookup"><span data-stu-id="5ffab-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="5ffab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ffab-110">PARAMETERS</span></span>

### <span data-ttu-id="5ffab-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5ffab-111">-ClusterName</span></span>
<span data-ttu-id="5ffab-112">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="5ffab-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5ffab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffab-113">-DefaultProfile</span></span>
<span data-ttu-id="5ffab-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ffab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ffab-115">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="5ffab-115">-HttpCredential</span></span>
<span data-ttu-id="5ffab-116">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="5ffab-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="5ffab-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="5ffab-117">-JobId</span></span>
<span data-ttu-id="5ffab-118">Определяет ИД задания.</span><span class="sxs-lookup"><span data-stu-id="5ffab-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="5ffab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffab-119">-ResourceGroupName</span></span>
<span data-ttu-id="5ffab-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ffab-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5ffab-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5ffab-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="5ffab-122">Общее время, необходимое для завершения задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5ffab-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="5ffab-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5ffab-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="5ffab-124">Время, необходимое для проверки состояния задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5ffab-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="5ffab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffab-125">CommonParameters</span></span>
<span data-ttu-id="5ffab-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ffab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffab-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ffab-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffab-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffab-128">INPUTS</span></span>

### <span data-ttu-id="5ffab-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5ffab-129">System.String</span></span>

## <span data-ttu-id="5ffab-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ffab-130">OUTPUTS</span></span>

### <span data-ttu-id="5ffab-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5ffab-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="5ffab-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ffab-132">NOTES</span></span>

## <span data-ttu-id="5ffab-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ffab-133">RELATED LINKS</span></span>

[<span data-ttu-id="5ffab-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5ffab-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="5ffab-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5ffab-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="5ffab-136">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5ffab-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


