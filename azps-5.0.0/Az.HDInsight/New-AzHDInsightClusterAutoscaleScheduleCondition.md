---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245363"
---
# <span data-ttu-id="b8626-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="b8626-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="b8626-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8626-102">SYNOPSIS</span></span>
<span data-ttu-id="b8626-103">Создает условие автомасштабирования на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="b8626-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="b8626-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8626-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8626-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8626-105">DESCRIPTION</span></span>
<span data-ttu-id="b8626-106">Командлет **New-AzHDInsightClusterAutoscaleScheduleCondition** создает условие автомасштабирования на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="b8626-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="b8626-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8626-107">EXAMPLES</span></span>

### <span data-ttu-id="b8626-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8626-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="b8626-109">Эта команда создает условие для автоматического масштабирования кластеров до 5 рабочих узлов в 09:00 каждый понедельник в среду.</span><span class="sxs-lookup"><span data-stu-id="b8626-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="b8626-110">Пример 2: Включите автомасштабирование на основе расписания для кластера с условием автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8626-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="b8626-111">Эта команда создает условие для автоматического масштабирования кластеров до 5 рабочих узлов в 09:00 каждый понедельник в среду.</span><span class="sxs-lookup"><span data-stu-id="b8626-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="b8626-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8626-112">PARAMETERS</span></span>

### <span data-ttu-id="b8626-113">-День</span><span class="sxs-lookup"><span data-stu-id="b8626-113">-Day</span></span>
<span data-ttu-id="b8626-114">Возвращает или задает количество дней для условия расписания автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8626-114">Gets or sets the days of Autoscale schedule condition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8626-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8626-115">-DefaultProfile</span></span>
<span data-ttu-id="b8626-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8626-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8626-117">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="b8626-117">-Time</span></span>
<span data-ttu-id="b8626-118">Возвращает или задает время выполнения условия расписания автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8626-118">Gets or sets the time of Autoscale schedule condition.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8626-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="b8626-119">-WorkerNodeCount</span></span>
<span data-ttu-id="b8626-120">Возвращает или задает количество workernode расписания для условия расписания автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8626-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8626-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8626-121">CommonParameters</span></span>
<span data-ttu-id="b8626-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8626-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8626-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8626-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8626-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8626-124">INPUTS</span></span>

### <span data-ttu-id="b8626-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8626-125">None</span></span>

## <span data-ttu-id="b8626-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8626-126">OUTPUTS</span></span>

### <span data-ttu-id="b8626-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="b8626-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="b8626-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8626-128">NOTES</span></span>

## <span data-ttu-id="b8626-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8626-129">RELATED LINKS</span></span>

<span data-ttu-id="b8626-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b8626-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
