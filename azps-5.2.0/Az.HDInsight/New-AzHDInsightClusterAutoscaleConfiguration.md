---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c2d8e3c2f3da4ebd2d07d16965a24878af34e262
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323010"
---
# <span data-ttu-id="2674d-101">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2674d-101">New-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="2674d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2674d-102">SYNOPSIS</span></span>
<span data-ttu-id="2674d-103">Создает объект, который не сохраняется, описывая конфигурацию автоматической настройки кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2674d-103">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2674d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2674d-104">SYNTAX</span></span>

### <span data-ttu-id="2674d-105">LoadAutoscaleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2674d-105">LoadAutoscaleParameterSet (Default)</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount <Int32> -MaxWorkerNodeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2674d-106">ScheduleAutoscaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="2674d-106">ScheduleAutoscaleParameterSet</span></span>
```
New-AzHDInsightClusterAutoscaleConfiguration -TimeZone <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2674d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2674d-107">DESCRIPTION</span></span>
<span data-ttu-id="2674d-108">С использованием cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** создается непостояованный объект, который описывает конфигурацию автоматической шкалы кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2674d-108">The cmdlet **New-AzHDInsightClusterAutoscaleConfiguration** creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2674d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2674d-109">EXAMPLES</span></span>

### <span data-ttu-id="2674d-110">Пример 1. Создание объекта, который описывает конфигурацию автомасштабации на основе загрузки</span><span class="sxs-lookup"><span data-stu-id="2674d-110">Example 1: Create an object which describes Load-based autoscale configuration</span></span>
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="2674d-111">Эта команда создает объект, который описывает конфигурацию автомасштабации с учетом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2674d-111">This command creates an object which describes Load-based autoscale configuration.</span></span>

### <span data-ttu-id="2674d-112">Пример 2. Создание объекта, который описывает конфигурацию автоматических шкал на основе календарного плана</span><span class="sxs-lookup"><span data-stu-id="2674d-112">Example 2: Create an object which describes Schedule-based autoscale configuration</span></span>
```powershell
# Create an autoscale condition firstly
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Day Monday -Time 09:00 -WorkerNodeCount 5
PS C:\> New-AzHDInsightClusterAutoscaleConfiguration -TimeZone ([System.TimeZoneInfo]::Local).Id `
        -Condition $condition
```

<span data-ttu-id="2674d-113">Эта команда создает объект, описывая конфигурацию автоматических шкал на основе календарного плана.</span><span class="sxs-lookup"><span data-stu-id="2674d-113">This command creates an object which describes Schedule-based autoscale configuration.</span></span>

## <span data-ttu-id="2674d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2674d-114">PARAMETERS</span></span>

### <span data-ttu-id="2674d-115">-Condition</span><span class="sxs-lookup"><span data-stu-id="2674d-115">-Condition</span></span>
<span data-ttu-id="2674d-116">Возвращает или задает условие для автоматической шкалы на основе календарного плана.</span><span class="sxs-lookup"><span data-stu-id="2674d-116">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2674d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2674d-117">-DefaultProfile</span></span>
<span data-ttu-id="2674d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2674d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2674d-119">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="2674d-119">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="2674d-120">Получает или задает максимальное количество рабочих подразделов для автоматических шкал с учетом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2674d-120">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2674d-121">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="2674d-121">-MinWorkerNodeCount</span></span>
<span data-ttu-id="2674d-122">Получает или задает минимальное количество рабочих нагрузок для автоматической шкалы с учетом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2674d-122">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2674d-123">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="2674d-123">-TimeZone</span></span>
<span data-ttu-id="2674d-124">Возвращает или задает часовой пояс для автоматической шкалы на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="2674d-124">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2674d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2674d-125">CommonParameters</span></span>
<span data-ttu-id="2674d-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2674d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2674d-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2674d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2674d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2674d-128">INPUTS</span></span>

### <span data-ttu-id="2674d-129">Нет</span><span class="sxs-lookup"><span data-stu-id="2674d-129">None</span></span>

## <span data-ttu-id="2674d-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2674d-130">OUTPUTS</span></span>

### <span data-ttu-id="2674d-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="2674d-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="2674d-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2674d-132">NOTES</span></span>

## <span data-ttu-id="2674d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2674d-133">RELATED LINKS</span></span>

<span data-ttu-id="2674d-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2674d-134">[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
