---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517170"
---
# <span data-ttu-id="cd85a-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd85a-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="cd85a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd85a-102">SYNOPSIS</span></span>
<span data-ttu-id="cd85a-103">Обновив приложение с тканью службы.</span><span class="sxs-lookup"><span data-stu-id="cd85a-103">Update a service fabric application.</span></span> <span data-ttu-id="cd85a-104">Это позволяет обновить параметры приложения и (или) версию типа приложения, которая активирует обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="cd85a-105">Поддерживаются ARM только развернутые приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="cd85a-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd85a-106">SYNTAX</span></span>

### <span data-ttu-id="cd85a-107">ByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd85a-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="cd85a-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cd85a-108">ByResourceId</span></span>
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

### <span data-ttu-id="cd85a-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd85a-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd85a-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd85a-110">DESCRIPTION</span></span>
<span data-ttu-id="cd85a-111">Этот cmdlet может использоваться для обновления параметров приложения и обновления версии типа приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="cd85a-112">При обновлении параметра модель будет изменяться только ARM стороне, только если используется новая версия типа, команда будет запускать обновление приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="cd85a-113">Указанная версия типа уже должна быть создана в кластере с помощью **New-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="cd85a-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="cd85a-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd85a-114">EXAMPLES</span></span>

### <span data-ttu-id="cd85a-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd85a-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="cd85a-116">В этом примере начнется обновление приложения до версии v2, созданной с помощью **new-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="cd85a-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="cd85a-117">Используемые параметры приложения должны быть определены в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="cd85a-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cd85a-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="cd85a-119">В этом примере обновляется ограничение на минимальное и максимальное количество узлов для приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="cd85a-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cd85a-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="cd85a-121">В этом примере начнется обновление приложения до версии v2, а также заданы некоторые параметры политики обновления, которые будут действовать после текущего обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="cd85a-122">Пример 4</span><span class="sxs-lookup"><span data-stu-id="cd85a-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="cd85a-123">В этом примере параметры приложения обновляются, но в силу эти изменения вступает в силу только до следующей версии приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="cd85a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd85a-124">PARAMETERS</span></span>

### <span data-ttu-id="cd85a-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="cd85a-125">-ApplicationParameter</span></span>
<span data-ttu-id="cd85a-126">Укажите параметры приложения в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="cd85a-127">Эти параметры должны существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="cd85a-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd85a-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="cd85a-129">Указание версии типа приложения</span><span class="sxs-lookup"><span data-stu-id="cd85a-129">Specify the application type version</span></span>

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

### <span data-ttu-id="cd85a-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cd85a-130">-ClusterName</span></span>
<span data-ttu-id="cd85a-131">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="cd85a-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cd85a-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="cd85a-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="cd85a-133">Указывает, следует ли рассматривать предупреждающие медицинские события как ошибки во время оценки здоровья.</span><span class="sxs-lookup"><span data-stu-id="cd85a-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="cd85a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd85a-134">-DefaultProfile</span></span>
<span data-ttu-id="cd85a-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd85a-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd85a-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="cd85a-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="cd85a-137">Указывает максимальный процент бесполезных разделов для службы, разрешенный политикой здравоохранения для используемого по умолчанию типа службы для отслеживаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="cd85a-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="cd85a-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="cd85a-139">Указывает максимальный процент бесполезных реплик для службы, разрешенный политикой здравоохранения для типа службы, используемого по умолчанию для отслеживаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="cd85a-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="cd85a-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="cd85a-141">Указывает максимальный процент бесполезных служб, разрешенный политикой здравоохранения для типа службы, используемого по умолчанию для отслеживаемого обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="cd85a-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="cd85a-142">-FailureAction</span></span>
<span data-ttu-id="cd85a-143">Указывает действие, необходимое в случае сбой обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="cd85a-144">Допустимыми значениями для этого параметра являются "Откат" или "Вручную".</span><span class="sxs-lookup"><span data-stu-id="cd85a-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="cd85a-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="cd85a-145">-ForceRestart</span></span>
<span data-ttu-id="cd85a-146">Указывает на перезапуск хоста службы даже при изменении конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cd85a-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="cd85a-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="cd85a-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="cd85a-148">Определяет длительность (в секундах), после которой "Служебная ткань" получает проверку на состояние, если предыдущая проверка невозмогодна.</span><span class="sxs-lookup"><span data-stu-id="cd85a-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="cd85a-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="cd85a-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="cd85a-150">Определяет длительность (в секундах), в течение указанной в служивом материале, чтобы убедиться, что приложение надежно перед переходом на следующий домен или завершением обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="cd85a-151">Эта длительность ожидания предотвращает незащищенные изменения состояния сразу после проверки.</span><span class="sxs-lookup"><span data-stu-id="cd85a-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="cd85a-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="cd85a-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="cd85a-153">Определяет длительность (в секундах), которую "Сервисная ткань" ждет перед выполнением начальной проверки ее состояния после завершения обновления до домена обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="cd85a-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd85a-154">-InputObject</span></span>
<span data-ttu-id="cd85a-155">Ресурс приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-155">The application resource.</span></span>

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

### <span data-ttu-id="cd85a-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="cd85a-156">-MaximumNodeCount</span></span>
<span data-ttu-id="cd85a-157">Указывает максимальное количество узлов, на которых нужно разместить приложение.</span><span class="sxs-lookup"><span data-stu-id="cd85a-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="cd85a-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="cd85a-158">-MinimumNodeCount</span></span>
<span data-ttu-id="cd85a-159">Определяет минимальное количество узлов, где "Служивная ткань" будет резервировать мощность для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="cd85a-160">-Name</span><span class="sxs-lookup"><span data-stu-id="cd85a-160">-Name</span></span>
<span data-ttu-id="cd85a-161">Укажите имя приложения</span><span class="sxs-lookup"><span data-stu-id="cd85a-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="cd85a-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd85a-162">-ResourceGroupName</span></span>
<span data-ttu-id="cd85a-163">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd85a-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cd85a-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd85a-164">-ResourceId</span></span>
<span data-ttu-id="cd85a-165">Arm ResourceId приложения.</span><span class="sxs-lookup"><span data-stu-id="cd85a-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="cd85a-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="cd85a-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="cd85a-167">Карта политики здравоохранения, используемой для различных типов служб в качестве хеш-таблицы, в следующем формате: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="cd85a-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="cd85a-168">Например: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="cd85a-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="cd85a-169">-НеработоспособноеDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="cd85a-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="cd85a-170">Указывает максимальный процент экземпляров приложений, развернутых на узлах в кластере, которые имеют состояние ошибки "Состояние здоровья" до ошибки состояния "Состояние состояния приложения" для кластера.</span><span class="sxs-lookup"><span data-stu-id="cd85a-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="cd85a-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="cd85a-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="cd85a-172">Определяет максимальное время (в секундах), необходимое для обновления домена "Служивная ткань".</span><span class="sxs-lookup"><span data-stu-id="cd85a-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="cd85a-173">После этого периода обновление не будет обновлено.</span><span class="sxs-lookup"><span data-stu-id="cd85a-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="cd85a-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="cd85a-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="cd85a-175">Определяет максимальное время, в течение которое служба "Ткань" будет перенастрояться в безопасное состояние (если еще не указано в безопасном состоянии) до переподдержки "Служивая ткань" после обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="cd85a-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="cd85a-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="cd85a-177">Определяет максимальное время (в секундах), которое "Служивная ткань" занимает до обновления.</span><span class="sxs-lookup"><span data-stu-id="cd85a-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="cd85a-178">После этого периода обновление не будет обновлено.</span><span class="sxs-lookup"><span data-stu-id="cd85a-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="cd85a-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd85a-179">-Confirm</span></span>
<span data-ttu-id="cd85a-180">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cd85a-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd85a-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd85a-181">-WhatIf</span></span>
<span data-ttu-id="cd85a-182">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd85a-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd85a-183">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd85a-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd85a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd85a-184">CommonParameters</span></span>
<span data-ttu-id="cd85a-185">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd85a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd85a-186">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd85a-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd85a-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd85a-187">INPUTS</span></span>

### <span data-ttu-id="cd85a-188">System.String</span><span class="sxs-lookup"><span data-stu-id="cd85a-188">System.String</span></span>

### <span data-ttu-id="cd85a-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="cd85a-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="cd85a-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd85a-190">OUTPUTS</span></span>

### <span data-ttu-id="cd85a-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="cd85a-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="cd85a-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd85a-192">NOTES</span></span>

## <span data-ttu-id="cd85a-193">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd85a-193">RELATED LINKS</span></span>
