---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504818"
---
# <span data-ttu-id="f73f8-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="f73f8-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="f73f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f73f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f73f8-103">Создание условия автоматической шкалы на основе календарного плана.</span><span class="sxs-lookup"><span data-stu-id="f73f8-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="f73f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f73f8-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f73f8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f73f8-105">DESCRIPTION</span></span>
<span data-ttu-id="f73f8-106">Для создания условия автоматической шкалы на основе календаря создается **cmdlet New-AzHDInsightClusterAutoscaleScheduleCondition.**</span><span class="sxs-lookup"><span data-stu-id="f73f8-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="f73f8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f73f8-107">EXAMPLES</span></span>

### <span data-ttu-id="f73f8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f73f8-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="f73f8-109">Эта команда создает условие для автоматической шкалы кластера до 5 узлов рабочих групп в 09:00 каждый понедельник, среда.</span><span class="sxs-lookup"><span data-stu-id="f73f8-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="f73f8-110">Пример 2. В этом примере можно включить автоматическую шкалу на основе календарного плана для кластера с условием автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="f73f8-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="f73f8-111">Эта команда создает условие для автоматической шкалы кластера до 5 узлов рабочих групп в 09:00 каждый понедельник, среда.</span><span class="sxs-lookup"><span data-stu-id="f73f8-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="f73f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f73f8-112">PARAMETERS</span></span>

### <span data-ttu-id="f73f8-113">-Day</span><span class="sxs-lookup"><span data-stu-id="f73f8-113">-Day</span></span>
<span data-ttu-id="f73f8-114">Возвращает или задает дни, на которые настраивается расписание для автоматической шкалы.</span><span class="sxs-lookup"><span data-stu-id="f73f8-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="f73f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73f8-115">-DefaultProfile</span></span>
<span data-ttu-id="f73f8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f73f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f73f8-117">-Time</span><span class="sxs-lookup"><span data-stu-id="f73f8-117">-Time</span></span>
<span data-ttu-id="f73f8-118">Возвращает или задает время для условия расписания с автоматическим масштабом.</span><span class="sxs-lookup"><span data-stu-id="f73f8-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="f73f8-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="f73f8-119">-WorkerNodeCount</span></span>
<span data-ttu-id="f73f8-120">Возвращает или задает количество сотрудников по расписанию при автоматической шкале.</span><span class="sxs-lookup"><span data-stu-id="f73f8-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="f73f8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73f8-121">CommonParameters</span></span>
<span data-ttu-id="f73f8-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73f8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73f8-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f73f8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73f8-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f73f8-124">INPUTS</span></span>

### <span data-ttu-id="f73f8-125">Нет</span><span class="sxs-lookup"><span data-stu-id="f73f8-125">None</span></span>

## <span data-ttu-id="f73f8-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f73f8-126">OUTPUTS</span></span>

### <span data-ttu-id="f73f8-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="f73f8-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="f73f8-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f73f8-128">NOTES</span></span>

## <span data-ttu-id="f73f8-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f73f8-129">RELATED LINKS</span></span>

<span data-ttu-id="f73f8-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f73f8-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
