---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517234"
---
# <span data-ttu-id="65d44-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="65d44-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="65d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d44-102">SYNOPSIS</span></span>
<span data-ttu-id="65d44-103">Создайте новую службу выкладок обслуживания в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="65d44-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="65d44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65d44-104">SYNTAX</span></span>

### <span data-ttu-id="65d44-105">Stateless-Singleton (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65d44-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65d44-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="65d44-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65d44-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="65d44-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d44-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="65d44-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d44-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="65d44-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65d44-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="65d44-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65d44-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65d44-111">DESCRIPTION</span></span>
<span data-ttu-id="65d44-112">Этот cmdlet позволяет создавать службы без состояния или состояния в указанном приложении.</span><span class="sxs-lookup"><span data-stu-id="65d44-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="65d44-113">Служба должна выйти из манифеста приложения и использовать тот же тип, что и в манифесте.</span><span class="sxs-lookup"><span data-stu-id="65d44-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="65d44-114">Имя приложения должно быть префиксом имени службы.</span><span class="sxs-lookup"><span data-stu-id="65d44-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="65d44-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65d44-115">EXAMPLES</span></span>

### <span data-ttu-id="65d44-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65d44-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="65d44-117">В этом примере создается новая служба без состояния "testApp~testService1" с количеством экземпляров -1 (на всех узлах).</span><span class="sxs-lookup"><span data-stu-id="65d44-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="65d44-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="65d44-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="65d44-119">В этом примере создается новая служба testApp~testService2 с целевым количеством узлов (5).</span><span class="sxs-lookup"><span data-stu-id="65d44-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="65d44-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65d44-120">PARAMETERS</span></span>

### <span data-ttu-id="65d44-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="65d44-121">-ApplicationName</span></span>
<span data-ttu-id="65d44-122">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="65d44-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="65d44-123">-ClusterName</span></span>
<span data-ttu-id="65d44-124">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="65d44-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="65d44-125">-DefaultMoveCost</span></span>
<span data-ttu-id="65d44-126">Укажите затраты по умолчанию для перемещения.</span><span class="sxs-lookup"><span data-stu-id="65d44-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="65d44-127">Чем выше затраты, тем меньше вероятность того, что диспетчер ресурсов кластера переместит репликацию при попытке сбалансировать кластер.</span><span class="sxs-lookup"><span data-stu-id="65d44-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d44-128">-DefaultProfile</span></span>
<span data-ttu-id="65d44-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65d44-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d44-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="65d44-130">-InstanceCount</span></span>
<span data-ttu-id="65d44-131">Укажите количество экземпляров для службы</span><span class="sxs-lookup"><span data-stu-id="65d44-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="65d44-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="65d44-133">Указание размера набора мин-реплик для службы</span><span class="sxs-lookup"><span data-stu-id="65d44-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-134">-Name</span><span class="sxs-lookup"><span data-stu-id="65d44-134">-Name</span></span>
<span data-ttu-id="65d44-135">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="65d44-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="65d44-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="65d44-137">Указывает на то, что в службе используется именоваемая схема секционной схемы.</span><span class="sxs-lookup"><span data-stu-id="65d44-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="65d44-138">Службы, использующие эту модель, обычно имеют данные, которые можно сегментровать в связанном наборе.</span><span class="sxs-lookup"><span data-stu-id="65d44-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="65d44-139">Некоторые распространенные примеры полей данных, используемых в качестве именных ключей раздела, — регионы, почтовые индексы, группы клиентов или другие границы бизнеса.</span><span class="sxs-lookup"><span data-stu-id="65d44-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="65d44-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="65d44-141">Указывает на то, что в службе используется схема секционной схемы однотонов.</span><span class="sxs-lookup"><span data-stu-id="65d44-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="65d44-142">Разделы одного тона обычно используются, если для службы не требуется дополнительная маршрутия.</span><span class="sxs-lookup"><span data-stu-id="65d44-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="65d44-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="65d44-144">Указывает на то, что в службе используется схема секционной схемы UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="65d44-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="65d44-145">Это означает, что каждый раздел имеет диапазон ключей int64.</span><span class="sxs-lookup"><span data-stu-id="65d44-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="65d44-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="65d44-147">Указание длительности ожидания потери каворки для службы</span><span class="sxs-lookup"><span data-stu-id="65d44-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="65d44-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="65d44-149">Указание длительности ожидания перезагрузки репликации для службы</span><span class="sxs-lookup"><span data-stu-id="65d44-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d44-150">-ResourceGroupName</span></span>
<span data-ttu-id="65d44-151">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65d44-151">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="65d44-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="65d44-153">Указание длительности stand by replica для службы</span><span class="sxs-lookup"><span data-stu-id="65d44-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="65d44-154">-Stateful</span></span>
<span data-ttu-id="65d44-155">Используется для собслужив</span><span class="sxs-lookup"><span data-stu-id="65d44-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-156">-Stateless</span><span class="sxs-lookup"><span data-stu-id="65d44-156">-Stateless</span></span>
<span data-ttu-id="65d44-157">Использование для службы без состояния</span><span class="sxs-lookup"><span data-stu-id="65d44-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="65d44-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="65d44-159">Указание размера целевого набора реплик для службы</span><span class="sxs-lookup"><span data-stu-id="65d44-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-160">-Type</span><span class="sxs-lookup"><span data-stu-id="65d44-160">-Type</span></span>
<span data-ttu-id="65d44-161">Укажите имя типа службы приложения, которое должно существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="65d44-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d44-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65d44-162">-Confirm</span></span>
<span data-ttu-id="65d44-163">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d44-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d44-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d44-164">-WhatIf</span></span>
<span data-ttu-id="65d44-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65d44-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d44-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="65d44-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d44-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d44-167">CommonParameters</span></span>
<span data-ttu-id="65d44-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d44-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d44-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65d44-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d44-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65d44-170">INPUTS</span></span>

### <span data-ttu-id="65d44-171">System.String</span><span class="sxs-lookup"><span data-stu-id="65d44-171">System.String</span></span>

## <span data-ttu-id="65d44-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65d44-172">OUTPUTS</span></span>

### <span data-ttu-id="65d44-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="65d44-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="65d44-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65d44-174">NOTES</span></span>

## <span data-ttu-id="65d44-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65d44-175">RELATED LINKS</span></span>
