---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311840"
---
# <span data-ttu-id="70bf5-101">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="70bf5-101">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="70bf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="70bf5-103">Задает конфигурацию автомасштабирования для кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="70bf5-103">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70bf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70bf5-104">SYNTAX</span></span>

### <span data-ttu-id="70bf5-105">LoadAutoscaleByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70bf5-105">LoadAutoscaleByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-106">ScheduleAutoscaleByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-106">ScheduleAutoscaleByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-107">AutoscaleConfigurationByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-107">AutoscaleConfigurationByNameParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-108">LoadAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-108">LoadAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70bf5-109">ScheduleAutoscaleByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-109">ScheduleAutoscaleByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-110">AutoscaleConfigurationByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-110">AutoscaleConfigurationByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-111">LoadAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-111">LoadAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-112">ScheduleAutoscaleByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-112">ScheduleAutoscaleByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bf5-113">AutoscaleConfigurationByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70bf5-113">AutoscaleConfigurationByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70bf5-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70bf5-114">DESCRIPTION</span></span>
<span data-ttu-id="70bf5-115">Этот командлет **Set-AzHDInsightClusterAutoscaleConfiguration** задает конфигурацию автомасштабирования для кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="70bf5-115">This cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="70bf5-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70bf5-116">EXAMPLES</span></span>

### <span data-ttu-id="70bf5-117">Пример 1: Настройка конфигурации автомасштабирования на основе загрузки для кластера HDInsight</span><span class="sxs-lookup"><span data-stu-id="70bf5-117">Example 1: Set the Load-based autoscale configuration of the HDInsight cluster</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

<span data-ttu-id="70bf5-118">Эта команда задает конфигурацию автомасштабирования на основе нагрузки для кластера HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="70bf5-118">This command sets the Load-based autoscale configuration of an Azure HDInsight cluster.</span></span>

### <span data-ttu-id="70bf5-119">Пример 2: Настройка автомасштабирования на основе расписания для кластера HDInsight</span><span class="sxs-lookup"><span data-stu-id="70bf5-119">Example 2: Set the Schedule-based autoscale of the HDInsight cluster</span></span>
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

<span data-ttu-id="70bf5-120">Эта команда задает конфигурацию автомасштабирования в соответствии с расписанием для кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70bf5-120">This command sets the Schedule-based autoscale configuration of the HDInsight cluster.</span></span>

### <span data-ttu-id="70bf5-121">Пример 3: Настройка конфигурации автомасштабирования в кластере HDInsight на другом кластере с установленной конфигурацией автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="70bf5-121">Example 3: Set the autoscale configuration of the HDInsight cluster based another cluster which has set autoscale configuration</span></span>
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

<span data-ttu-id="70bf5-122">Эта команда задает конфигурацию автомасштабирования кластера HDInsight на другом кластере.</span><span class="sxs-lookup"><span data-stu-id="70bf5-122">This command sets the autoscale configuration of the HDInsight cluster based another cluster.</span></span>

## <span data-ttu-id="70bf5-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70bf5-123">PARAMETERS</span></span>

### <span data-ttu-id="70bf5-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70bf5-124">-AsJob</span></span>
<span data-ttu-id="70bf5-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="70bf5-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70bf5-126">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="70bf5-126">-AutoscaleConfiguration</span></span>
<span data-ttu-id="70bf5-127">Возвращает или задает конфигурацию автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="70bf5-127">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="70bf5-128">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="70bf5-128">-ClusterName</span></span>
<span data-ttu-id="70bf5-129">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="70bf5-129">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="70bf5-130">-Условие</span><span class="sxs-lookup"><span data-stu-id="70bf5-130">-Condition</span></span>
<span data-ttu-id="70bf5-131">Возвращает или задает условие автомасштабирования на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="70bf5-131">Gets or sets the condition of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="70bf5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bf5-132">-DefaultProfile</span></span>
<span data-ttu-id="70bf5-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70bf5-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70bf5-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70bf5-134">-InputObject</span></span>
<span data-ttu-id="70bf5-135">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="70bf5-135">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="70bf5-136">-MaxWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="70bf5-136">-MaxWorkerNodeCount</span></span>
<span data-ttu-id="70bf5-137">Возвращает или задает максимальное workernode число автомасштабирования на основе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="70bf5-137">Gets or sets the maximal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="70bf5-138">-MinWorkerNodeCount</span><span class="sxs-lookup"><span data-stu-id="70bf5-138">-MinWorkerNodeCount</span></span>
<span data-ttu-id="70bf5-139">Возвращает или задает минимальное число workernode для автомасштабирования на основе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="70bf5-139">Gets or sets the minimal workernode count of load-based autoscale.</span></span>

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

### <span data-ttu-id="70bf5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70bf5-140">-ResourceGroupName</span></span>
<span data-ttu-id="70bf5-141">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70bf5-141">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="70bf5-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70bf5-142">-ResourceId</span></span>
<span data-ttu-id="70bf5-143">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="70bf5-143">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="70bf5-144">-Планирование</span><span class="sxs-lookup"><span data-stu-id="70bf5-144">-Schedule</span></span>
<span data-ttu-id="70bf5-145">Установка параметров, основанных на расписании</span><span class="sxs-lookup"><span data-stu-id="70bf5-145">Set schedule-based parameters</span></span>

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

### <span data-ttu-id="70bf5-146">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="70bf5-146">-TimeZone</span></span>
<span data-ttu-id="70bf5-147">Возвращает или задает часовой пояс для автомасштабирования на основе расписания.</span><span class="sxs-lookup"><span data-stu-id="70bf5-147">Gets or sets the time zone of schedule-based autoscale.</span></span>

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

### <span data-ttu-id="70bf5-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70bf5-148">-Confirm</span></span>
<span data-ttu-id="70bf5-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70bf5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70bf5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70bf5-150">-WhatIf</span></span>
<span data-ttu-id="70bf5-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70bf5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70bf5-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70bf5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70bf5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bf5-153">CommonParameters</span></span>
<span data-ttu-id="70bf5-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70bf5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bf5-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70bf5-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bf5-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70bf5-156">INPUTS</span></span>

### <span data-ttu-id="70bf5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="70bf5-157">System.String</span></span>

### <span data-ttu-id="70bf5-158">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70bf5-158">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="70bf5-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70bf5-159">OUTPUTS</span></span>

### <span data-ttu-id="70bf5-160">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="70bf5-160">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="70bf5-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="70bf5-161">NOTES</span></span>

## <span data-ttu-id="70bf5-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70bf5-162">RELATED LINKS</span></span>

<span data-ttu-id="70bf5-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="70bf5-163">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
