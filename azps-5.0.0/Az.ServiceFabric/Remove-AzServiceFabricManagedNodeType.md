---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245860"
---
# <span data-ttu-id="ac48a-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="ac48a-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="ac48a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac48a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac48a-103">Удалите тип узла или отдельные узлы в типе узла.</span><span class="sxs-lookup"><span data-stu-id="ac48a-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="ac48a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac48a-104">SYNTAX</span></span>

### <span data-ttu-id="ac48a-105">DeleteNodeTypeByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac48a-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac48a-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="ac48a-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac48a-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="ac48a-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac48a-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="ac48a-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac48a-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="ac48a-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac48a-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="ac48a-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac48a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac48a-111">DESCRIPTION</span></span>
<span data-ttu-id="ac48a-112">Удалите тип узла или отдельные узлы в типе узла.</span><span class="sxs-lookup"><span data-stu-id="ac48a-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="ac48a-113">Если используется paremter-NodeName, будут удалены только указанные узлы.</span><span class="sxs-lookup"><span data-stu-id="ac48a-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="ac48a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac48a-114">EXAMPLES</span></span>

### <span data-ttu-id="ac48a-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac48a-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="ac48a-116">Удалите тип узла.</span><span class="sxs-lookup"><span data-stu-id="ac48a-116">Remove node type.</span></span>

### <span data-ttu-id="ac48a-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ac48a-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="ac48a-118">Удалить тип узла с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="ac48a-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="ac48a-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ac48a-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="ac48a-120">Удаление 2 узлов из типа узла.</span><span class="sxs-lookup"><span data-stu-id="ac48a-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="ac48a-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ac48a-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="ac48a-122">Удалите 2 узла из типа "трубка".</span><span class="sxs-lookup"><span data-stu-id="ac48a-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="ac48a-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac48a-123">PARAMETERS</span></span>

### <span data-ttu-id="ac48a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac48a-124">-AsJob</span></span>
<span data-ttu-id="ac48a-125">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ac48a-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ac48a-126">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ac48a-126">-ClusterName</span></span>
<span data-ttu-id="ac48a-127">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ac48a-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac48a-128">-DefaultProfile</span></span>
<span data-ttu-id="ac48a-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac48a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac48a-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="ac48a-130">-ForceRemoveNode</span></span>
<span data-ttu-id="ac48a-131">Использование этого флага приведет к принудительному удалению, даже если фабрика служб не может отключить узлы.</span><span class="sxs-lookup"><span data-stu-id="ac48a-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="ac48a-132">Используйте с осторожностью, так как это может привести к потере данных, если рабочие нагрузки выполняются на узлах, или может перестать кластером, если после opearion не хватит узлов с заначальными данными.</span><span class="sxs-lookup"><span data-stu-id="ac48a-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac48a-133">-InputObject</span></span>
<span data-ttu-id="ac48a-134">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="ac48a-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac48a-135">-Name</span></span>
<span data-ttu-id="ac48a-136">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="ac48a-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ac48a-137">-NodeName</span></span>
<span data-ttu-id="ac48a-138">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="ac48a-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac48a-139">-PassThru</span></span>
<span data-ttu-id="ac48a-140">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ac48a-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ac48a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac48a-141">-ResourceGroupName</span></span>
<span data-ttu-id="ac48a-142">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac48a-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac48a-143">-ResourceId</span></span>
<span data-ttu-id="ac48a-144">Идентификатор ресурса типа Node</span><span class="sxs-lookup"><span data-stu-id="ac48a-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac48a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac48a-145">-Confirm</span></span>
<span data-ttu-id="ac48a-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac48a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac48a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac48a-147">-WhatIf</span></span>
<span data-ttu-id="ac48a-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac48a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac48a-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac48a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac48a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac48a-150">CommonParameters</span></span>
<span data-ttu-id="ac48a-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac48a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac48a-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac48a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac48a-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac48a-153">INPUTS</span></span>

### <span data-ttu-id="ac48a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ac48a-154">System.String</span></span>

## <span data-ttu-id="ac48a-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac48a-155">OUTPUTS</span></span>

### <span data-ttu-id="ac48a-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac48a-156">System.Boolean</span></span>

## <span data-ttu-id="ac48a-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac48a-157">NOTES</span></span>

## <span data-ttu-id="ac48a-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac48a-158">RELATED LINKS</span></span>
