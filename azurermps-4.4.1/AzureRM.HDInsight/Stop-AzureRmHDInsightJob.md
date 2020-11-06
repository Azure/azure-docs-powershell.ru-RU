---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FD27C755-9AAF-42DA-8425-1661C92B6C68
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Stop-AzureRmHDInsightJob.md
ms.openlocfilehash: 674c8f1cb5fdf8d8c76da36a7bb6d8df06e29c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569432"
---
# <span data-ttu-id="181a2-101">Stop-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="181a2-101">Stop-AzureRmHDInsightJob</span></span>

## <span data-ttu-id="181a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="181a2-102">SYNOPSIS</span></span>
<span data-ttu-id="181a2-103">Останавливает указанное запущенное задание в кластере.</span><span class="sxs-lookup"><span data-stu-id="181a2-103">Stops a specified running job on a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="181a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="181a2-104">SYNTAX</span></span>

```
Stop-AzureRmHDInsightJob [-ClusterName] <String> [-JobId] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="181a2-105">DESCRIPTION</span></span>
<span data-ttu-id="181a2-106">Командлет **Stop-AzureRmHDInsightJob** останавливает указанное запущенное задание в кластере HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="181a2-106">The **Stop-AzureRmHDInsightJob** cmdlet stops a specified running job on an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="181a2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="181a2-107">EXAMPLES</span></span>

### <span data-ttu-id="181a2-108">Пример 1: Остановка задания в указанном кластере</span><span class="sxs-lookup"><span data-stu-id="181a2-108">Example 1: Stop a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential
PS C:\> Stop-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
            -JobId $jobId
```

<span data-ttu-id="181a2-109">Эта команда останавливает задание в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="181a2-109">This command stops a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="181a2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="181a2-110">PARAMETERS</span></span>

### <span data-ttu-id="181a2-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="181a2-111">-ClusterName</span></span>
<span data-ttu-id="181a2-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="181a2-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="181a2-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="181a2-113">-HttpCredential</span></span>
<span data-ttu-id="181a2-114">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="181a2-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="181a2-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="181a2-115">-JobId</span></span>
<span data-ttu-id="181a2-116">Указывает код задания для задания.</span><span class="sxs-lookup"><span data-stu-id="181a2-116">Specifies the job ID of the job.</span></span>

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

### <span data-ttu-id="181a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="181a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="181a2-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="181a2-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="181a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181a2-119">-DefaultProfile</span></span>
<span data-ttu-id="181a2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="181a2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181a2-121">CommonParameters</span></span>
<span data-ttu-id="181a2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="181a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181a2-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181a2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="181a2-124">INPUTS</span></span>

### <span data-ttu-id="181a2-125">Подстрок</span><span class="sxs-lookup"><span data-stu-id="181a2-125">String</span></span>
<span data-ttu-id="181a2-126">Параметр "JobId" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="181a2-126">Parameter 'JobId' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="181a2-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="181a2-127">OUTPUTS</span></span>

### <span data-ttu-id="181a2-128">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="181a2-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="181a2-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="181a2-129">NOTES</span></span>

## <span data-ttu-id="181a2-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="181a2-130">RELATED LINKS</span></span>

[<span data-ttu-id="181a2-131">Get-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="181a2-131">Get-AzureRmHDInsightJob</span></span>](./Get-AzureRmHDInsightJob.md)

[<span data-ttu-id="181a2-132">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="181a2-132">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

[<span data-ttu-id="181a2-133">Wait-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="181a2-133">Wait-AzureRmHDInsightJob</span></span>](./Wait-AzureRmHDInsightJob.md)


