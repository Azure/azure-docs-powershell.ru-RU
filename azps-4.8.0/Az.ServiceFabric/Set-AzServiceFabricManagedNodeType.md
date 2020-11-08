---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243304"
---
# <span data-ttu-id="472e8-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="472e8-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="472e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="472e8-102">SYNOPSIS</span></span>
<span data-ttu-id="472e8-103">Задает свойства ресурса типа Node или выполняет действия по переобразу для определенного NDES с параметром-Reimage.</span><span class="sxs-lookup"><span data-stu-id="472e8-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="472e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="472e8-104">SYNTAX</span></span>

### <span data-ttu-id="472e8-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="472e8-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="472e8-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="472e8-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="472e8-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="472e8-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="472e8-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="472e8-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="472e8-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="472e8-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="472e8-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="472e8-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="472e8-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="472e8-111">DESCRIPTION</span></span>
<span data-ttu-id="472e8-112">Задает свойства ресурса типа Node или выполняет действия по переобразу для определенного NDES с параметром-Reimage.</span><span class="sxs-lookup"><span data-stu-id="472e8-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="472e8-113">В операции reimgae узлы структуры служб будут отключены, прежде чем reimaging виртуальные машины и снова включить их снова после возврата.</span><span class="sxs-lookup"><span data-stu-id="472e8-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="472e8-114">Если это делается для основных типов узлов, это может занять некоторое время, так как это может привести к тому, что вы не перемещаете сразу все узлы.</span><span class="sxs-lookup"><span data-stu-id="472e8-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="472e8-115">Функция-ForceReimage принудительно выполняет операцию, даже если фабрика служб не может отключить узлы, но используется с осторожностью, так как это может привести к потере данных, если на узле выполняются нагрузки с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="472e8-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="472e8-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="472e8-116">EXAMPLES</span></span>

### <span data-ttu-id="472e8-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="472e8-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="472e8-118">Обновите количество экземпляров типа узла.</span><span class="sxs-lookup"><span data-stu-id="472e8-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="472e8-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="472e8-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="472e8-120">Обновите properites размещения для типа узла.</span><span class="sxs-lookup"><span data-stu-id="472e8-120">Update placement properites of the node type.</span></span> <span data-ttu-id="472e8-121">Это приведет к перезаписи более ранних properites размещения, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="472e8-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="472e8-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="472e8-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="472e8-123">Переобразировать узлы 0 и 3 на типе узла.</span><span class="sxs-lookup"><span data-stu-id="472e8-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="472e8-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="472e8-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="472e8-125">Обновите количество экземпляров типа узла с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="472e8-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="472e8-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="472e8-126">PARAMETERS</span></span>

### <span data-ttu-id="472e8-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="472e8-127">-ApplicationEndPort</span></span>
<span data-ttu-id="472e8-128">Конечный порт приложения диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="472e8-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="472e8-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="472e8-129">-ApplicationStartPort</span></span>
<span data-ttu-id="472e8-130">Порт запуска приложения в диапазоне портов.</span><span class="sxs-lookup"><span data-stu-id="472e8-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="472e8-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="472e8-131">-AsJob</span></span>
<span data-ttu-id="472e8-132">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="472e8-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="472e8-133">-Capacity</span><span class="sxs-lookup"><span data-stu-id="472e8-133">-Capacity</span></span>
<span data-ttu-id="472e8-134">Теги производственных мощностей, примененные к узлам в типе узла в виде пар "ключ-значение", диспетчер ресурсов кластера использует эти теги для понимания того, сколько ресурсов имеет узел.</span><span class="sxs-lookup"><span data-stu-id="472e8-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="472e8-135">После обновления текущие значения будут переопределены.</span><span class="sxs-lookup"><span data-stu-id="472e8-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="472e8-136">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="472e8-136">-ClusterName</span></span>
<span data-ttu-id="472e8-137">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="472e8-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="472e8-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="472e8-138">-DefaultProfile</span></span>
<span data-ttu-id="472e8-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="472e8-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="472e8-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="472e8-140">-EphemeralEndPort</span></span>
<span data-ttu-id="472e8-141">Эфемерный конечный порт диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="472e8-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="472e8-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="472e8-142">-EphemeralStartPort</span></span>
<span data-ttu-id="472e8-143">Временный начальный порт диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="472e8-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="472e8-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="472e8-144">-ForceReimage</span></span>
<span data-ttu-id="472e8-145">Использование этого флага приведет к принудительному удалению, даже если фабрика служб не может отключить узлы.</span><span class="sxs-lookup"><span data-stu-id="472e8-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="472e8-146">Используйте с осторожностью, так как это может привести к потере данных, если на узле запущены рабочие нагрузки с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="472e8-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="472e8-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="472e8-147">-InputObject</span></span>
<span data-ttu-id="472e8-148">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="472e8-148">Node type resource</span></span>

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

### <span data-ttu-id="472e8-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="472e8-149">-InstanceCount</span></span>
<span data-ttu-id="472e8-150">Количество узлов в типе узла.</span><span class="sxs-lookup"><span data-stu-id="472e8-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="472e8-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="472e8-151">-Name</span></span>
<span data-ttu-id="472e8-152">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="472e8-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="472e8-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="472e8-153">-NodeName</span></span>
<span data-ttu-id="472e8-154">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="472e8-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="472e8-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="472e8-155">-PassThru</span></span>
<span data-ttu-id="472e8-156">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="472e8-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="472e8-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="472e8-157">-PlacementProperty</span></span>
<span data-ttu-id="472e8-158">Теги размещения применяются к узлам в типе узла в виде пар "ключ-значение", которые можно использовать, чтобы указать, где должны выполняться определенные службы (рабочей нагрузки).</span><span class="sxs-lookup"><span data-stu-id="472e8-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="472e8-159">После обновления текущие значения будут переопределены.</span><span class="sxs-lookup"><span data-stu-id="472e8-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="472e8-160">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="472e8-160">-Reimage</span></span>
<span data-ttu-id="472e8-161">Укажите, как переобразировать узлы на типе узла.</span><span class="sxs-lookup"><span data-stu-id="472e8-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="472e8-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="472e8-162">-ResourceGroupName</span></span>
<span data-ttu-id="472e8-163">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="472e8-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="472e8-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="472e8-164">-ResourceId</span></span>
<span data-ttu-id="472e8-165">Идентификатор ресурса типа Node</span><span class="sxs-lookup"><span data-stu-id="472e8-165">Node type resource id</span></span>

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

### <span data-ttu-id="472e8-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="472e8-166">-Confirm</span></span>
<span data-ttu-id="472e8-167">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="472e8-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="472e8-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="472e8-168">-WhatIf</span></span>
<span data-ttu-id="472e8-169">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="472e8-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="472e8-170">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="472e8-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="472e8-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="472e8-171">CommonParameters</span></span>
<span data-ttu-id="472e8-172">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="472e8-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="472e8-173">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="472e8-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="472e8-174">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="472e8-174">INPUTS</span></span>

### <span data-ttu-id="472e8-175">System. String</span><span class="sxs-lookup"><span data-stu-id="472e8-175">System.String</span></span>

## <span data-ttu-id="472e8-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="472e8-176">OUTPUTS</span></span>

### <span data-ttu-id="472e8-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="472e8-177">System.Boolean</span></span>

## <span data-ttu-id="472e8-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="472e8-178">NOTES</span></span>

## <span data-ttu-id="472e8-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="472e8-179">RELATED LINKS</span></span>
