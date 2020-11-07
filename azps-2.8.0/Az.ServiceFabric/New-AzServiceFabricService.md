---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 5a17b7197399ac51afccfbc5b00a77e0d2bca727
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903757"
---
# <span data-ttu-id="24718-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="24718-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="24718-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24718-102">SYNOPSIS</span></span>
<span data-ttu-id="24718-103">Создание новой службы Service Fabric в указанном приложении и кластере.</span><span class="sxs-lookup"><span data-stu-id="24718-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="24718-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24718-104">SYNTAX</span></span>

### <span data-ttu-id="24718-105">Stateless-Singleton (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24718-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24718-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="24718-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24718-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="24718-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24718-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="24718-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24718-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="24718-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24718-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="24718-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24718-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24718-111">DESCRIPTION</span></span>
<span data-ttu-id="24718-112">Этот командлет позволяет создавать службы без сохранения состояния или состояния в указанном приложении.</span><span class="sxs-lookup"><span data-stu-id="24718-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="24718-113">Служба должна выйти из манифеста приложения, а тип должен совпадать с типом в манифесте.</span><span class="sxs-lookup"><span data-stu-id="24718-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="24718-114">Имя приложения должно быть префиксом имени службы.</span><span class="sxs-lookup"><span data-stu-id="24718-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="24718-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24718-115">EXAMPLES</span></span>

### <span data-ttu-id="24718-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24718-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="24718-117">В этом примере создается новая служба без сохранения состояния "testApp ~ testService1" с количеством экземпляров 1 (на всех узлах).</span><span class="sxs-lookup"><span data-stu-id="24718-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="24718-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="24718-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="24718-119">В этом примере будет создана новая служба отслеживания состояния "testApp ~ testService2" с целью 5 узлов.</span><span class="sxs-lookup"><span data-stu-id="24718-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="24718-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24718-120">PARAMETERS</span></span>

### <span data-ttu-id="24718-121">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="24718-121">-ApplicationName</span></span>
<span data-ttu-id="24718-122">Укажите имя приложения.</span><span class="sxs-lookup"><span data-stu-id="24718-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="24718-123">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="24718-123">-ClusterName</span></span>
<span data-ttu-id="24718-124">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="24718-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="24718-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="24718-125">-DefaultMoveCost</span></span>
<span data-ttu-id="24718-126">Укажите стоимость по умолчанию для перемещения.</span><span class="sxs-lookup"><span data-stu-id="24718-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="24718-127">Чем выше стоимость, тем меньше вероятность того, что диспетчер ресурсов кластера переместит реплику при попытке сбалансировать кластер.</span><span class="sxs-lookup"><span data-stu-id="24718-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

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

### <span data-ttu-id="24718-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24718-128">-DefaultProfile</span></span>
<span data-ttu-id="24718-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24718-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24718-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="24718-130">-InstanceCount</span></span>
<span data-ttu-id="24718-131">Указание количества экземпляров службы</span><span class="sxs-lookup"><span data-stu-id="24718-131">Specify the instance count for the service</span></span>

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

### <span data-ttu-id="24718-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="24718-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="24718-133">Указание минимального размера наборов реплик для службы</span><span class="sxs-lookup"><span data-stu-id="24718-133">Specify the min replica set size for the service</span></span>

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

### <span data-ttu-id="24718-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24718-134">-Name</span></span>
<span data-ttu-id="24718-135">Укажите имя службы.</span><span class="sxs-lookup"><span data-stu-id="24718-135">Specify the name of the service.</span></span>

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

### <span data-ttu-id="24718-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="24718-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="24718-137">Указывает, что служба использует именованную схему секционирования.</span><span class="sxs-lookup"><span data-stu-id="24718-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="24718-138">У служб, использующих эту модель, обычно есть данные, которые могут быть сегментированы в рамках ограниченного множества.</span><span class="sxs-lookup"><span data-stu-id="24718-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="24718-139">Наиболее распространенными примерами полей данных, используемых в качестве именованных ключей секционирования, являются регионы, почтовые индексы, группы клиентов и другие границы бизнеса.</span><span class="sxs-lookup"><span data-stu-id="24718-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

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

### <span data-ttu-id="24718-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="24718-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="24718-141">Указывает, что служба использует одноэлементную схему секционирования.</span><span class="sxs-lookup"><span data-stu-id="24718-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="24718-142">Одноэлементные разделы обычно используются, если службе не требуется дополнительная маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="24718-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

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

### <span data-ttu-id="24718-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="24718-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="24718-144">Указывает, что служба использует схему секционирования UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="24718-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="24718-145">Это означает, что каждый раздел владеет диапазоном из Int64.</span><span class="sxs-lookup"><span data-stu-id="24718-145">This means that each partition owns a range of int64 keys.</span></span>

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

### <span data-ttu-id="24718-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="24718-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="24718-147">Указание длительности ожидания при потере кворума для службы</span><span class="sxs-lookup"><span data-stu-id="24718-147">Specify the quorum loss wait duration for the service</span></span>

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

### <span data-ttu-id="24718-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="24718-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="24718-149">Укажите период ожидания повторного запуска реплики для службы</span><span class="sxs-lookup"><span data-stu-id="24718-149">Specify the replica restart wait duration for the service</span></span>

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

### <span data-ttu-id="24718-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24718-150">-ResourceGroupName</span></span>
<span data-ttu-id="24718-151">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24718-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="24718-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="24718-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="24718-153">Указание времени ожидания реплики для службы</span><span class="sxs-lookup"><span data-stu-id="24718-153">Specify the stand by replica duration for the service</span></span>

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

### <span data-ttu-id="24718-154">-Состояние</span><span class="sxs-lookup"><span data-stu-id="24718-154">-Stateful</span></span>
<span data-ttu-id="24718-155">Использование службы с ведением базы данных</span><span class="sxs-lookup"><span data-stu-id="24718-155">Use for stateful service</span></span>

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

### <span data-ttu-id="24718-156">-Без состояния</span><span class="sxs-lookup"><span data-stu-id="24718-156">-Stateless</span></span>
<span data-ttu-id="24718-157">Использование службы без сохранения состояния</span><span class="sxs-lookup"><span data-stu-id="24718-157">Use for stateless service</span></span>

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

### <span data-ttu-id="24718-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="24718-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="24718-159">Указание размера целевого задания реплики для службы</span><span class="sxs-lookup"><span data-stu-id="24718-159">Specify the target replica set size for the service</span></span>

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

### <span data-ttu-id="24718-160">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="24718-160">-Type</span></span>
<span data-ttu-id="24718-161">Укажите имя типа службы для приложения, которое должно существовать в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="24718-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

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

### <span data-ttu-id="24718-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24718-162">-Confirm</span></span>
<span data-ttu-id="24718-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24718-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24718-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24718-164">-WhatIf</span></span>
<span data-ttu-id="24718-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24718-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24718-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24718-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24718-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24718-167">CommonParameters</span></span>
<span data-ttu-id="24718-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24718-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24718-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24718-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24718-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24718-170">INPUTS</span></span>

### <span data-ttu-id="24718-171">System. String</span><span class="sxs-lookup"><span data-stu-id="24718-171">System.String</span></span>

## <span data-ttu-id="24718-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24718-172">OUTPUTS</span></span>

### <span data-ttu-id="24718-173">Microsoft. Azure. Commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="24718-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="24718-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="24718-174">NOTES</span></span>

## <span data-ttu-id="24718-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24718-175">RELATED LINKS</span></span>
