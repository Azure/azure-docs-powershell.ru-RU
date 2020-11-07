---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/wait-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Wait-AzHDInsightJob.md
ms.openlocfilehash: b603be88ffa89f730cfaaa2f67738cdadc2d4d25
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720790"
---
# <span data-ttu-id="1a04c-101">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1a04c-101">Wait-AzHDInsightJob</span></span>

## <span data-ttu-id="1a04c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a04c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a04c-103">Ожидание завершения или сбоя указанного задания.</span><span class="sxs-lookup"><span data-stu-id="1a04c-103">Waits for the completion or failure of a specified job.</span></span>

## <span data-ttu-id="1a04c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a04c-104">SYNTAX</span></span>

```
Wait-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a04c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a04c-105">DESCRIPTION</span></span>
<span data-ttu-id="1a04c-106">Командлет **Wait-AzHDInsightJob** ожидает завершения или сбоя задания Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1a04c-106">The **Wait-AzHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="1a04c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a04c-107">EXAMPLES</span></span>

### <span data-ttu-id="1a04c-108">Пример 1: ожидание завершения или сбоя задания</span><span class="sxs-lookup"><span data-stu-id="1a04c-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="1a04c-109">Эта команда ожидает завершения или сбоя задания.</span><span class="sxs-lookup"><span data-stu-id="1a04c-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="1a04c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a04c-110">PARAMETERS</span></span>

### <span data-ttu-id="1a04c-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="1a04c-111">-ClusterName</span></span>
<span data-ttu-id="1a04c-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1a04c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1a04c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a04c-113">-DefaultProfile</span></span>
<span data-ttu-id="1a04c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a04c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a04c-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="1a04c-115">-HttpCredential</span></span>
<span data-ttu-id="1a04c-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="1a04c-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="1a04c-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="1a04c-117">-JobId</span></span>
<span data-ttu-id="1a04c-118">Указывает код задания для задания.</span><span class="sxs-lookup"><span data-stu-id="1a04c-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="1a04c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a04c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a04c-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a04c-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1a04c-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1a04c-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="1a04c-122">Общее время ожидания завершения задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="1a04c-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="1a04c-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1a04c-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="1a04c-124">Время ожидания между проверками состояния задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="1a04c-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="1a04c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a04c-125">CommonParameters</span></span>
<span data-ttu-id="1a04c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a04c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a04c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a04c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a04c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a04c-128">INPUTS</span></span>

### <span data-ttu-id="1a04c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1a04c-129">System.String</span></span>

## <span data-ttu-id="1a04c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a04c-130">OUTPUTS</span></span>

### <span data-ttu-id="1a04c-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1a04c-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="1a04c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a04c-132">NOTES</span></span>

## <span data-ttu-id="1a04c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a04c-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a04c-134">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1a04c-134">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="1a04c-135">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1a04c-135">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="1a04c-136">Остановить-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1a04c-136">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)


