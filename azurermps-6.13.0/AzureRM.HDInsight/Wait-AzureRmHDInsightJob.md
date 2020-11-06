---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/wait-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: de7df9417e617f88c61e75c64dd42f32b83fc66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565436"
---
# <span data-ttu-id="c8132-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8132-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="c8132-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8132-102">SYNOPSIS</span></span>
<span data-ttu-id="c8132-103">Ожидание завершения или сбоя указанного задания.</span><span class="sxs-lookup"><span data-stu-id="c8132-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8132-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8132-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8132-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8132-105">DESCRIPTION</span></span>
<span data-ttu-id="c8132-106">Командлет **Wait-AzureRmHDInsightJob** ожидает завершения или сбоя задания Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c8132-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="c8132-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8132-107">EXAMPLES</span></span>

### <span data-ttu-id="c8132-108">Пример 1: ожидание завершения или сбоя задания</span><span class="sxs-lookup"><span data-stu-id="c8132-108">Example 1: Wait for the completion or failure of a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Wait-AzureRmHDInsightJob -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="c8132-109">Эта команда ожидает завершения или сбоя задания.</span><span class="sxs-lookup"><span data-stu-id="c8132-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="c8132-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8132-110">PARAMETERS</span></span>

### <span data-ttu-id="c8132-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="c8132-111">-ClusterName</span></span>
<span data-ttu-id="c8132-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c8132-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c8132-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8132-113">-DefaultProfile</span></span>
<span data-ttu-id="c8132-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8132-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8132-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c8132-115">-HttpCredential</span></span>
<span data-ttu-id="c8132-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="c8132-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="c8132-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c8132-117">-JobId</span></span>
<span data-ttu-id="c8132-118">Указывает код задания для задания.</span><span class="sxs-lookup"><span data-stu-id="c8132-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="c8132-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8132-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8132-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8132-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c8132-121">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="c8132-121">-TimeoutInSeconds</span></span>
<span data-ttu-id="c8132-122">Общее время ожидания завершения задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c8132-122">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="c8132-123">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="c8132-123">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="c8132-124">Время ожидания между проверками состояния задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="c8132-124">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="c8132-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8132-125">CommonParameters</span></span>
<span data-ttu-id="c8132-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8132-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8132-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8132-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8132-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8132-128">INPUTS</span></span>

### <span data-ttu-id="c8132-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c8132-129">System.String</span></span>
<span data-ttu-id="c8132-130">Параметры: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8132-130">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="c8132-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8132-131">OUTPUTS</span></span>

### <span data-ttu-id="c8132-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8132-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="c8132-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8132-133">NOTES</span></span>

## <span data-ttu-id="c8132-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8132-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8132-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8132-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="c8132-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8132-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="c8132-137">Остановить-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="c8132-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


