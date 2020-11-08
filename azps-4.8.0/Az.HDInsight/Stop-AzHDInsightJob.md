---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/stop-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Stop-AzHDInsightJob.md
ms.openlocfilehash: d5e38cf3edb89801b630735dee1ce0dbd1d62d41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236457"
---
# <span data-ttu-id="0cfae-101">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0cfae-101">Stop-AzHDInsightJob</span></span>

## <span data-ttu-id="0cfae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0cfae-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfae-103">Останавливает указанное запущенное задание в кластере.</span><span class="sxs-lookup"><span data-stu-id="0cfae-103">Stops a specified running job on a cluster.</span></span>

## <span data-ttu-id="0cfae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0cfae-104">SYNTAX</span></span>

```
Stop-AzHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cfae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cfae-105">DESCRIPTION</span></span>
<span data-ttu-id="0cfae-106">Командлет **Stop-AzHDInsightJob** останавливает указанное запущенное задание в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="0cfae-106">The **Stop-AzHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0cfae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0cfae-107">EXAMPLES</span></span>

### <span data-ttu-id="0cfae-108">Пример 1: Остановка задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="0cfae-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="0cfae-109">Эта команда останавливает задание в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0cfae-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0cfae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0cfae-110">PARAMETERS</span></span>

### <span data-ttu-id="0cfae-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="0cfae-111">-ClusterName</span></span>
<span data-ttu-id="0cfae-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="0cfae-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0cfae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfae-113">-DefaultProfile</span></span>
<span data-ttu-id="0cfae-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0cfae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cfae-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0cfae-115">-HttpCredential</span></span>
<span data-ttu-id="0cfae-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="0cfae-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0cfae-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="0cfae-117">-JobId</span></span>
<span data-ttu-id="0cfae-118">Указывает код задания для задания.</span><span class="sxs-lookup"><span data-stu-id="0cfae-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="0cfae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cfae-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cfae-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0cfae-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0cfae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfae-121">CommonParameters</span></span>
<span data-ttu-id="0cfae-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0cfae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfae-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cfae-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfae-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0cfae-124">INPUTS</span></span>

### <span data-ttu-id="0cfae-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0cfae-125">System.String</span></span>

## <span data-ttu-id="0cfae-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cfae-126">OUTPUTS</span></span>

### <span data-ttu-id="0cfae-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0cfae-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="0cfae-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0cfae-128">NOTES</span></span>

## <span data-ttu-id="0cfae-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cfae-129">RELATED LINKS</span></span>

[<span data-ttu-id="0cfae-130">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0cfae-130">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="0cfae-131">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0cfae-131">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

[<span data-ttu-id="0cfae-132">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0cfae-132">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)

