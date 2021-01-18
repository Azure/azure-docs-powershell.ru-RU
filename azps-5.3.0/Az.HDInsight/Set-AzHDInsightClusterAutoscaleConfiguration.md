---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506293"
---
# <span data-ttu-id="c23a4-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c23a4-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="c23a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c23a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c23a4-103">Настраивает автоматическую настройку кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c23a4-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c23a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c23a4-104">SYNTAX</span></span>

### <span data-ttu-id="c23a4-105">LoadAutoscaleByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c23a4-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c23a4-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c23a4-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c23a4-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c23a4-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c23a4-114">DESCRIPTION</span></span>
<span data-ttu-id="c23a4-115">Этот cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** задает настройку автоматической настройки кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c23a4-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c23a4-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c23a4-116">EXAMPLES</span></span>

### <span data-ttu-id="c23a4-117">Пример 1. Настройка конфигурации с автоматическим управлением загрузкой кластера HDInsight</span><span class="sxs-lookup"><span data-stu-id="c23a4-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="c23a4-118">Эта команда задает конфигурацию автоматической шкалы на основе загрузки кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c23a4-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="c23a4-119">Пример 2. Настройка автоматической шкалы на основе расписания для кластера HDInsight</span><span class="sxs-lookup"><span data-stu-id="c23a4-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="c23a4-120">Эта команда задает автоматическую настройку кластера HDInsight на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="c23a4-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="c23a4-121">Пример 3. Настройка конфигурации кластера HDInsight на основе другого кластера, в котором настроена настройка авто шкалы</span><span class="sxs-lookup"><span data-stu-id="c23a4-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

<span data-ttu-id="c23a4-122">Эта команда задает автоматическую настройку кластера HDInsight на основе другого кластера.</span><span class="sxs-lookup"><span data-stu-id="c23a4-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="c23a4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c23a4-123">PARAMETERS</span></span>

### <span data-ttu-id="c23a4-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c23a4-124">-AsJob</span></span>
<span data-ttu-id="c23a4-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c23a4-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c23a4-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="c23a4-127">Получает или настраивает конфигурацию автомасштаби</span><span class="sxs-lookup"><span data-stu-id="c23a4-127">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c23a4-128">-ClusterName</span></span>
<span data-ttu-id="c23a4-129">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c23a4-129">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-130">-Условие</span><span class="sxs-lookup"><span data-stu-id="c23a4-130">-Condition</span></span>
<span data-ttu-id="c23a4-131">Возвращает или задает условие для автоматической шкалы на основе календарного плана.</span><span class="sxs-lookup"><span data-stu-id="c23a4-131">Gets or sets the condition of schedule-based autoscale.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23a4-132">-DefaultProfile</span></span>
<span data-ttu-id="c23a4-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c23a4-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c23a4-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c23a4-134">-InputObject</span></span>
<span data-ttu-id="c23a4-135">Возвращает или устанавливает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="c23a4-135">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c23a4-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="c23a4-137">Получает или задает максимальное количество рабочих подразделов для автоматических шкал с учетом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c23a4-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="c23a4-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="c23a4-139">Получает или задает минимальное количество рабочих нагрузок для автоматической шкалы с учетом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c23a4-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c23a4-140">-ResourceGroupName</span></span>
<span data-ttu-id="c23a4-141">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c23a4-141">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c23a4-142">-ResourceId</span></span>
<span data-ttu-id="c23a4-143">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="c23a4-143">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-144">-Расписание</span><span class="sxs-lookup"><span data-stu-id="c23a4-144">-Schedule</span></span>
<span data-ttu-id="c23a4-145">Настройка параметров на основе расписания</span><span class="sxs-lookup"><span data-stu-id="c23a4-145">Set schedule-based parameters</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-146">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="c23a4-146">-TimeZone</span></span>
<span data-ttu-id="c23a4-147">Возвращает или задает часовой пояс для автоматической шкалы на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="c23a4-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c23a4-148">-Confirm</span></span>
<span data-ttu-id="c23a4-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c23a4-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c23a4-150">-WhatIf</span></span>
<span data-ttu-id="c23a4-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c23a4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c23a4-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c23a4-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23a4-153">CommonParameters</span></span>
<span data-ttu-id="c23a4-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23a4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23a4-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c23a4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23a4-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c23a4-156">INPUTS</span></span>

### <span data-ttu-id="c23a4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="c23a4-157">System.String</span></span>

### <span data-ttu-id="c23a4-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c23a4-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c23a4-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c23a4-159">OUTPUTS</span></span>

### <span data-ttu-id="c23a4-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="c23a4-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="c23a4-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c23a4-161">NOTES</span></span>

## <span data-ttu-id="c23a4-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c23a4-162">RELATED LINKS</span></span>

<span data-ttu-id="c23a4-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c23a4-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
