---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: d96a26e4f37d565ac03d8585a803c355aff53b19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905261"
---
# <span data-ttu-id="d16c6-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d16c6-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="d16c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d16c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d16c6-103">Обновите приложение фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="d16c6-103">Update a service fabric application.</span></span> <span data-ttu-id="d16c6-104">Это позволит обновить параметры приложения и (или) обновить версию типа приложения, которая вызывает обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="d16c6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d16c6-105">SYNTAX</span></span>

### <span data-ttu-id="d16c6-106">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d16c6-106">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d16c6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d16c6-107">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d16c6-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d16c6-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d16c6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d16c6-109">DESCRIPTION</span></span>
<span data-ttu-id="d16c6-110">Этот командлет можно использовать для обновления параметров приложения и обновления версии типа приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="d16c6-111">Если вы обновляете этот параметр, модель будет изменена только на стороне ARM, но только при использовании новой версии типа она инициирует обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="d16c6-112">Указанная версия Type должна быть уже создана в кластере с помощью **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="d16c6-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="d16c6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d16c6-113">EXAMPLES</span></span>

### <span data-ttu-id="d16c6-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d16c6-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d16c6-115">В этом примере начнется обновление приложения, чтобы обновить версию Type до версии v2, созданной с помощью **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="d16c6-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="d16c6-116">Используемые параметры приложения должны быть определены в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="d16c6-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d16c6-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="d16c6-118">В этом примере будет обновляться минимальное и максимальное количество ограничений на узлы для приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="d16c6-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d16c6-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="d16c6-120">В этом примере начнется обновление приложения, чтобы изменить версию Type на "v2", а также задать некоторые параметры политики обновления, которые вступят в силу при текущем обновлении.</span><span class="sxs-lookup"><span data-stu-id="d16c6-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="d16c6-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d16c6-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d16c6-122">В этом примере обновляются параметры приложения, но эти изменения вступят в силу только в том случае, если вы обновите приложение до следующей версии.</span><span class="sxs-lookup"><span data-stu-id="d16c6-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="d16c6-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d16c6-123">PARAMETERS</span></span>

### <span data-ttu-id="d16c6-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="d16c6-124">-ApplicationParameter</span></span>
<span data-ttu-id="d16c6-125">Укажите параметры приложения в виде пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d16c6-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="d16c6-126">Эти параметры должны существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-126">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d16c6-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="d16c6-128">Указание версии типа приложения</span><span class="sxs-lookup"><span data-stu-id="d16c6-128">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-129">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="d16c6-129">-ClusterName</span></span>
<span data-ttu-id="d16c6-130">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="d16c6-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="d16c6-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="d16c6-132">Указывает, следует ли обрабатывать событие работоспособности предупреждения как событие ошибки во время оценки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="d16c6-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16c6-133">-DefaultProfile</span></span>
<span data-ttu-id="d16c6-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d16c6-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d16c6-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="d16c6-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="d16c6-136">Указывает максимальный процент unhelthyных секций для каждой службы, разрешенных политикой работоспособности для типа службы по умолчанию, который будет использоваться для наблюдаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="d16c6-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="d16c6-138">Указывает максимальный процент unhelthy реплик для каждой службы, разрешенных политикой работоспособности для типа службы по умолчанию, который будет использоваться для наблюдаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d16c6-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="d16c6-140">Указывает максимальный процент служб unhelthy, разрешенных политикой работоспособности для типа службы по умолчанию, который будет использоваться для наблюдаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-141">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="d16c6-141">-FailureAction</span></span>
<span data-ttu-id="d16c6-142">Указывает действие, которое будет выполнено в случае сбоя наблюдаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="d16c6-143">Допустимые значения этого параметра: ROLLBACK или вручную.</span><span class="sxs-lookup"><span data-stu-id="d16c6-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="d16c6-144">-ForceRestart</span></span>
<span data-ttu-id="d16c6-145">Указывает на то, что узел служб перезапустится даже в том случае, если обновление является изменением только конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d16c6-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d16c6-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="d16c6-147">Указывает продолжительность (в секундах), по истечении которой фабрика служб повторяет проверку работоспособности, если предыдущая проверка работоспособности завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="d16c6-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="d16c6-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="d16c6-149">Указывает продолжительность (в секундах), в течение которого должна выполняться структура служб, чтобы проверить, является ли приложение стабильным перед переходом к следующему домену обновления или завершению обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="d16c6-150">Это время ожидания предотвращает необнаруженные изменения состояния работоспособности сразу после проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="d16c6-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="d16c6-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="d16c6-152">Указывает продолжительность (в секундах), с которой служба Service Builder ожидает перед выполнением начальной проверки работоспособности после завершения обновления домена обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d16c6-153">-InputObject</span></span>
<span data-ttu-id="d16c6-154">Ресурс приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-154">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d16c6-155">-MaximumNodeCount</span></span>
<span data-ttu-id="d16c6-156">Указывает максимальное количество узлов, на которое нужно поместить приложение.</span><span class="sxs-lookup"><span data-stu-id="d16c6-156">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d16c6-157">-MinimumNodeCount</span></span>
<span data-ttu-id="d16c6-158">Указывает минимальное количество узлов, на которое зарезервирована емкость для этого приложения в структуре обслуживания</span><span class="sxs-lookup"><span data-stu-id="d16c6-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d16c6-159">-Name</span></span>
<span data-ttu-id="d16c6-160">Указание имени приложения</span><span class="sxs-lookup"><span data-stu-id="d16c6-160">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16c6-161">-ResourceGroupName</span></span>
<span data-ttu-id="d16c6-162">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d16c6-162">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d16c6-163">-ResourceId</span></span>
<span data-ttu-id="d16c6-164">ИД ресурса ARM приложения.</span><span class="sxs-lookup"><span data-stu-id="d16c6-164">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="d16c6-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="d16c6-166">Указывает карту политики работоспособности, используемую для разных типов служб в качестве хэш-таблицы в следующем формате: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="d16c6-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="d16c6-167">Например: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5; 5; 5"}</span><span class="sxs-lookup"><span data-stu-id="d16c6-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d16c6-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="d16c6-169">Задает максимальный процентное значение количества экземпляров приложения, развернутых на узлах в кластере, которые имеют состояние работоспособности для ошибки, прежде чем состояние работоспособности приложения для кластера будет ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d16c6-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d16c6-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="d16c6-171">Указывает максимальное время (в секундах), которое требуется для выполнения фабрики служб для обновления отдельного домена обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="d16c6-172">По прошествии этого периода обновление завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="d16c6-172">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d16c6-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="d16c6-174">Указывает максимальное время, в течение которого фабрика служб ожидает повторной настройки службы в безопасном состоянии (если она не находится в безопасном состоянии) перед тем, как фабрика служб продолжит работу с обновлением.</span><span class="sxs-lookup"><span data-stu-id="d16c6-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d16c6-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="d16c6-176">Задает максимальное время (в секундах), необходимое для работы фабрики служб для всего обновления.</span><span class="sxs-lookup"><span data-stu-id="d16c6-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="d16c6-177">По прошествии этого периода обновление завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="d16c6-177">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16c6-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d16c6-178">-Confirm</span></span>
<span data-ttu-id="d16c6-179">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d16c6-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d16c6-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d16c6-180">-WhatIf</span></span>
<span data-ttu-id="d16c6-181">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d16c6-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d16c6-182">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d16c6-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d16c6-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16c6-183">CommonParameters</span></span>
<span data-ttu-id="d16c6-184">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d16c6-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16c6-185">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d16c6-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16c6-186">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d16c6-186">INPUTS</span></span>

### <span data-ttu-id="d16c6-187">System. String</span><span class="sxs-lookup"><span data-stu-id="d16c6-187">System.String</span></span>

### <span data-ttu-id="d16c6-188">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d16c6-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d16c6-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d16c6-189">OUTPUTS</span></span>

### <span data-ttu-id="d16c6-190">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d16c6-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d16c6-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="d16c6-191">NOTES</span></span>

## <span data-ttu-id="d16c6-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d16c6-192">RELATED LINKS</span></span>
