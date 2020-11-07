---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 677E19F2-CC6C-4C16-B1FD-3A15D0FF1ECA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Wait-AzureRmHDInsightJob.md
ms.openlocfilehash: 6e19594cfcd79c6be82373af6245ea2154296b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735176"
---
# <span data-ttu-id="7d38d-101">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d38d-101">Wait-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="7d38d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d38d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d38d-103">Ожидание завершения или сбоя указанного задания.</span><span class="sxs-lookup"><span data-stu-id="7d38d-103">Waits for the completion or failure of a specified job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d38d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d38d-104">SYNTAX</span></span>

```
Wait-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-TimeoutInSeconds <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d38d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d38d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d38d-106">Командлет **Wait-AzureRmHDInsightJob** ожидает завершения или сбоя задания Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7d38d-106">The **Wait-AzureRmHDInsightJob** cmdlet awaits the completion or failure of an Azure HDInsight job.</span></span>

## <span data-ttu-id="7d38d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d38d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d38d-108">Пример 1: ожидание завершения или сбоя задания</span><span class="sxs-lookup"><span data-stu-id="7d38d-108">Example 1: Wait for the completion or failure of a job</span></span>
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

<span data-ttu-id="7d38d-109">Эта команда ожидает завершения или сбоя задания.</span><span class="sxs-lookup"><span data-stu-id="7d38d-109">This command waits for the completion or failure of a job.</span></span>

## <span data-ttu-id="7d38d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d38d-110">PARAMETERS</span></span>

### <span data-ttu-id="7d38d-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="7d38d-111">-ClusterName</span></span>
<span data-ttu-id="7d38d-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="7d38d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7d38d-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="7d38d-113">-HttpCredential</span></span>
<span data-ttu-id="7d38d-114">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="7d38d-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="7d38d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="7d38d-115">-JobId</span></span>
<span data-ttu-id="7d38d-116">Указывает код задания для задания.</span><span class="sxs-lookup"><span data-stu-id="7d38d-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="7d38d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d38d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d38d-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d38d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7d38d-119">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="7d38d-119">-TimeoutInSeconds</span></span>
<span data-ttu-id="7d38d-120">Общее время ожидания завершения задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="7d38d-120">The total time to wait for job completion, in seconds.</span></span>

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

### <span data-ttu-id="7d38d-121">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7d38d-121">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="7d38d-122">Время ожидания между проверками состояния задания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="7d38d-122">The time to wait between job status checks, in seconds.</span></span>

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

### <span data-ttu-id="7d38d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d38d-123">-DefaultProfile</span></span>
<span data-ttu-id="7d38d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d38d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d38d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d38d-125">CommonParameters</span></span>
<span data-ttu-id="7d38d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d38d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d38d-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d38d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d38d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d38d-128">INPUTS</span></span>

### <span data-ttu-id="7d38d-129">Подстрок</span><span class="sxs-lookup"><span data-stu-id="7d38d-129">String</span></span>
<span data-ttu-id="7d38d-130">Параметр "JobId" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7d38d-130">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7d38d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d38d-131">OUTPUTS</span></span>

### <span data-ttu-id="7d38d-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d38d-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="7d38d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d38d-133">NOTES</span></span>

## <span data-ttu-id="7d38d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d38d-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d38d-135">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d38d-135">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="7d38d-136">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d38d-136">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="7d38d-137">Остановить-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="7d38d-137">Stop-AzureRmHDInsightJob</span></span>](./Stop-AzureRmHDInsightJob.md)


