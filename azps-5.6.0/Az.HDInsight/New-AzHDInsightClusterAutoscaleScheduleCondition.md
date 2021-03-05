---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: c2fcc4112bb2fb62b73531bd6bd580ba3bcd7648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009032"
---
# <span data-ttu-id="33585-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="33585-101">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>

## <span data-ttu-id="33585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33585-102">SYNOPSIS</span></span>
<span data-ttu-id="33585-103">Создание условия автоматической шкалы на основе календарного плана.</span><span class="sxs-lookup"><span data-stu-id="33585-103">Creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="33585-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33585-104">SYNTAX</span></span>

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33585-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33585-105">DESCRIPTION</span></span>
<span data-ttu-id="33585-106">Для создания условия автоматической шкалы на основе календаря создается **cmdlet New-AzHDInsightClusterAutoscaleScheduleCondition.**</span><span class="sxs-lookup"><span data-stu-id="33585-106">The **New-AzHDInsightClusterAutoscaleScheduleCondition** cmdlet creates Schedule-based autoscale condition.</span></span>

## <span data-ttu-id="33585-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33585-107">EXAMPLES</span></span>

### <span data-ttu-id="33585-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33585-108">Example 1</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

<span data-ttu-id="33585-109">Эта команда создает условие для автоматической шкалы кластера до 5 узлов рабочих мест в 09:00 каждый понедельник, среда.</span><span class="sxs-lookup"><span data-stu-id="33585-109">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

### <span data-ttu-id="33585-110">Пример 2. Включить автоматическую шкалу на основе календарного плана для кластера с условием автоматической шкалы.</span><span class="sxs-lookup"><span data-stu-id="33585-110">Example 2: Enable Schedule-based autoscale of a cluster with autoscale condition.</span></span>
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

<span data-ttu-id="33585-111">Эта команда создает условие для автоматической шкалы кластера до 5 узлов рабочих мест в 09:00 каждый понедельник, среда.</span><span class="sxs-lookup"><span data-stu-id="33585-111">This command creates a condition where cluster autoscale to 5 worker nodes at 09:00 every Monday, Wednesday.</span></span>

## <span data-ttu-id="33585-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33585-112">PARAMETERS</span></span>

### <span data-ttu-id="33585-113">-Day</span><span class="sxs-lookup"><span data-stu-id="33585-113">-Day</span></span>
<span data-ttu-id="33585-114">Возвращает или задает дни, на которые настраивается расписание для автоматической шкалы.</span><span class="sxs-lookup"><span data-stu-id="33585-114">Gets or sets the days of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="33585-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33585-115">-DefaultProfile</span></span>
<span data-ttu-id="33585-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33585-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33585-117">-Time</span><span class="sxs-lookup"><span data-stu-id="33585-117">-Time</span></span>
<span data-ttu-id="33585-118">Возвращает или задает время для условия расписания с автоматическим масштабом.</span><span class="sxs-lookup"><span data-stu-id="33585-118">Gets or sets the time of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="33585-119">-WorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="33585-119">-WorkerNodeCount</span></span>
<span data-ttu-id="33585-120">Возвращает или задает количество сотрудников по расписанию при автоматической шкале.</span><span class="sxs-lookup"><span data-stu-id="33585-120">Gets or sets the schedule workernode count of Autoscale schedule condition.</span></span>

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

### <span data-ttu-id="33585-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33585-121">CommonParameters</span></span>
<span data-ttu-id="33585-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33585-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33585-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33585-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33585-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33585-124">INPUTS</span></span>

### <span data-ttu-id="33585-125">Нет</span><span class="sxs-lookup"><span data-stu-id="33585-125">None</span></span>

## <span data-ttu-id="33585-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33585-126">OUTPUTS</span></span>

### <span data-ttu-id="33585-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span><span class="sxs-lookup"><span data-stu-id="33585-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition</span></span>

## <span data-ttu-id="33585-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33585-128">NOTES</span></span>

## <span data-ttu-id="33585-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33585-129">RELATED LINKS</span></span>

<span data-ttu-id="33585-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="33585-130">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
