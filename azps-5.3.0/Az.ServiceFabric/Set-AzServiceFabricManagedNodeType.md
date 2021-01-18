---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505947"
---
# <span data-ttu-id="85185-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="85185-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="85185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85185-102">SYNOPSIS</span></span>
<span data-ttu-id="85185-103">Задает свойства ресурсов типа узла или запуск действий повторного действия повторного действия в определенных точках типа узла с параметром -Reimage.</span><span class="sxs-lookup"><span data-stu-id="85185-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="85185-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85185-104">SYNTAX</span></span>

### <span data-ttu-id="85185-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85185-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85185-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="85185-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85185-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="85185-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85185-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="85185-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85185-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="85185-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85185-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="85185-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85185-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85185-111">DESCRIPTION</span></span>
<span data-ttu-id="85185-112">Задает свойства ресурсов типа узла или запуск действий повторного действия повторного действия в определенных точках типа узла с параметром -Reimage.</span><span class="sxs-lookup"><span data-stu-id="85185-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="85185-113">При повторном перенастройке узлы сслуживной тканью будут отключены перед повторной сборкой vms и снова включены после их повторного включения.</span><span class="sxs-lookup"><span data-stu-id="85185-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="85185-114">Если это делается для основных типов узлов, может потребоваться некоторое время, так как может потребоваться не переумногание всех узлов одновременно.</span><span class="sxs-lookup"><span data-stu-id="85185-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="85185-115">Используйте -ForceReimage принудительно, даже если сервисный материал не может отключить узлы, но используйте с осторожностью, так как это может привести к потере данных, если на узле работают рабочие нагрузки с состоянием.</span><span class="sxs-lookup"><span data-stu-id="85185-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="85185-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85185-116">EXAMPLES</span></span>

### <span data-ttu-id="85185-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85185-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="85185-118">Обновив количество экземпляров для типа узла.</span><span class="sxs-lookup"><span data-stu-id="85185-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="85185-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="85185-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="85185-120">Обновите соответствующие узлы для размещения узлов.</span><span class="sxs-lookup"><span data-stu-id="85185-120">Update placement properites of the node type.</span></span> <span data-ttu-id="85185-121">При этом будут переописываться старые при размещении, если они есть.</span><span class="sxs-lookup"><span data-stu-id="85185-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="85185-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="85185-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="85185-123">Reimage node 0 and 3 on the node type.</span><span class="sxs-lookup"><span data-stu-id="85185-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="85185-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="85185-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="85185-125">Обновив количество экземпляров для типа узла, обновив тип piping.</span><span class="sxs-lookup"><span data-stu-id="85185-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="85185-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85185-126">PARAMETERS</span></span>

### <span data-ttu-id="85185-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="85185-127">-ApplicationEndPort</span></span>
<span data-ttu-id="85185-128">Порт окончания приложения для диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="85185-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="85185-129">-ApplicationStartPort</span></span>
<span data-ttu-id="85185-130">Начальный порт приложения для диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="85185-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85185-131">-AsJob</span></span>
<span data-ttu-id="85185-132">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="85185-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="85185-133">-Capacity</span><span class="sxs-lookup"><span data-stu-id="85185-133">-Capacity</span></span>
<span data-ttu-id="85185-134">Теги емкости, примененные к узлам в типе узла в качестве пар ключа и значения, диспетчер ресурсов кластера использует эти теги, чтобы понять, сколько ресурсов имеет узел.</span><span class="sxs-lookup"><span data-stu-id="85185-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="85185-135">При обновлении значения будут переопределяться.</span><span class="sxs-lookup"><span data-stu-id="85185-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="85185-136">-ClusterName</span></span>
<span data-ttu-id="85185-137">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="85185-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85185-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85185-138">-DefaultProfile</span></span>
<span data-ttu-id="85185-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85185-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85185-140">-EpenderalEndPort</span><span class="sxs-lookup"><span data-stu-id="85185-140">-EphemeralEndPort</span></span>
<span data-ttu-id="85185-141">Конечный порт в диапазоне портов.</span><span class="sxs-lookup"><span data-stu-id="85185-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-142">-EpисерalStartPort</span><span class="sxs-lookup"><span data-stu-id="85185-142">-EphemeralStartPort</span></span>
<span data-ttu-id="85185-143">Эперитеральный начните порт диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="85185-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="85185-144">-ForceReimage</span></span>
<span data-ttu-id="85185-145">Если этот флажок используется, удаление будет принудительно удалено, даже если сервисная ткань не может отключить узлы.</span><span class="sxs-lookup"><span data-stu-id="85185-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="85185-146">Используйте с осторожностью, так как это может привести к потере данных, если на узле работают рабочие нагрузки с состоянием.</span><span class="sxs-lookup"><span data-stu-id="85185-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85185-147">-InputObject</span></span>
<span data-ttu-id="85185-148">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="85185-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85185-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="85185-149">-InstanceCount</span></span>
<span data-ttu-id="85185-150">Количество узлов в типе узла.</span><span class="sxs-lookup"><span data-stu-id="85185-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-151">-Name</span><span class="sxs-lookup"><span data-stu-id="85185-151">-Name</span></span>
<span data-ttu-id="85185-152">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="85185-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85185-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="85185-153">-NodeName</span></span>
<span data-ttu-id="85185-154">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="85185-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85185-155">-PassThru</span></span>
<span data-ttu-id="85185-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="85185-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="85185-157">-PlacementProperty</span></span>
<span data-ttu-id="85185-158">Теги размещения, применяемые к узлам в типе узла в качестве пар ключа и значения, которые могут использоваться для того, чтобы указать, где должны запускаться определенные службы (рабочая нагрузка).</span><span class="sxs-lookup"><span data-stu-id="85185-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="85185-159">При обновлении значения будут переопределяться.</span><span class="sxs-lookup"><span data-stu-id="85185-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="85185-160">-Reimage</span></span>
<span data-ttu-id="85185-161">Укажите, нужно ли переустанавлить узлы для типа узла.</span><span class="sxs-lookup"><span data-stu-id="85185-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85185-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85185-162">-ResourceGroupName</span></span>
<span data-ttu-id="85185-163">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85185-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85185-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85185-164">-ResourceId</span></span>
<span data-ttu-id="85185-165">ИД ресурса "Тип узла"</span><span class="sxs-lookup"><span data-stu-id="85185-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85185-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85185-166">-Confirm</span></span>
<span data-ttu-id="85185-167">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="85185-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85185-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85185-168">-WhatIf</span></span>
<span data-ttu-id="85185-169">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85185-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85185-170">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="85185-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85185-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85185-171">CommonParameters</span></span>
<span data-ttu-id="85185-172">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85185-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85185-173">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85185-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85185-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85185-174">INPUTS</span></span>

### <span data-ttu-id="85185-175">System.String</span><span class="sxs-lookup"><span data-stu-id="85185-175">System.String</span></span>

## <span data-ttu-id="85185-176">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85185-176">OUTPUTS</span></span>

### <span data-ttu-id="85185-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85185-177">System.Boolean</span></span>

## <span data-ttu-id="85185-178">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85185-178">NOTES</span></span>

## <span data-ttu-id="85185-179">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85185-179">RELATED LINKS</span></span>
