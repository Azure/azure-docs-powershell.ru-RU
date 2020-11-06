---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/stop-azurermhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 7247a4f5e23bc4f0f3c520f909cec221ee03e1ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563031"
---
# <span data-ttu-id="81cb4-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81cb4-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="81cb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="81cb4-103">Останавливает указанное запущенное задание в кластере.</span><span class="sxs-lookup"><span data-stu-id="81cb4-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81cb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81cb4-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81cb4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="81cb4-106">Командлет **Stop-AzureRmHDInsightJob** останавливает указанное запущенное задание в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="81cb4-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="81cb4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="81cb4-108">Пример 1: Остановка задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="81cb4-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="81cb4-109">Эта команда останавливает задание в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="81cb4-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="81cb4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81cb4-110">PARAMETERS</span></span>

### <span data-ttu-id="81cb4-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="81cb4-111">-ClusterName</span></span>
<span data-ttu-id="81cb4-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="81cb4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="81cb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cb4-113">-DefaultProfile</span></span>
<span data-ttu-id="81cb4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="81cb4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81cb4-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="81cb4-115">-HttpCredential</span></span>
<span data-ttu-id="81cb4-116">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="81cb4-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="81cb4-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="81cb4-117">-JobId</span></span>
<span data-ttu-id="81cb4-118">Указывает код задания для задания.</span><span class="sxs-lookup"><span data-stu-id="81cb4-118">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="81cb4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81cb4-119">-ResourceGroupName</span></span>
<span data-ttu-id="81cb4-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81cb4-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="81cb4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cb4-121">CommonParameters</span></span>
<span data-ttu-id="81cb4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81cb4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cb4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81cb4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cb4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81cb4-124">INPUTS</span></span>

### <span data-ttu-id="81cb4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="81cb4-125">System.String</span></span>
<span data-ttu-id="81cb4-126">Параметры: JobId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="81cb4-126">Parameters: JobId (ByValue)</span></span>

## <span data-ttu-id="81cb4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81cb4-127">OUTPUTS</span></span>

### <span data-ttu-id="81cb4-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81cb4-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="81cb4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="81cb4-129">NOTES</span></span>

## <span data-ttu-id="81cb4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81cb4-130">RELATED LINKS</span></span>

[<span data-ttu-id="81cb4-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81cb4-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="81cb4-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81cb4-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="81cb4-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="81cb4-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


