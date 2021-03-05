---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5cb0e5bf8dce38a8552514835d2e16d19c3cc833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005475"
---
# <span data-ttu-id="307a6-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="307a6-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="307a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="307a6-102">SYNOPSIS</span></span>
<span data-ttu-id="307a6-103">Удалите тип узла или конкретные узлы для этого типа.</span><span class="sxs-lookup"><span data-stu-id="307a6-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="307a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="307a6-104">SYNTAX</span></span>

### <span data-ttu-id="307a6-105">DeleteNodeTypeByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="307a6-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307a6-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="307a6-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307a6-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="307a6-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307a6-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="307a6-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="307a6-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="307a6-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="307a6-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="307a6-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="307a6-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="307a6-111">DESCRIPTION</span></span>
<span data-ttu-id="307a6-112">Удалите тип узла или конкретные узлы для этого типа.</span><span class="sxs-lookup"><span data-stu-id="307a6-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="307a6-113">Если используется пареметр -NodeName, будут удалены только указанные узлы.</span><span class="sxs-lookup"><span data-stu-id="307a6-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="307a6-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="307a6-114">EXAMPLES</span></span>

### <span data-ttu-id="307a6-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="307a6-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="307a6-116">Удалить тип узла.</span><span class="sxs-lookup"><span data-stu-id="307a6-116">Remove node type.</span></span>

### <span data-ttu-id="307a6-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="307a6-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="307a6-118">Удаление типа узла с помощью перенаноской.</span><span class="sxs-lookup"><span data-stu-id="307a6-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="307a6-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="307a6-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="307a6-120">Удалите 2 узла из типа узла.</span><span class="sxs-lookup"><span data-stu-id="307a6-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="307a6-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="307a6-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="307a6-122">Удалите 2 узла из типа узла с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="307a6-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="307a6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="307a6-123">PARAMETERS</span></span>

### <span data-ttu-id="307a6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="307a6-124">-AsJob</span></span>
<span data-ttu-id="307a6-125">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="307a6-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="307a6-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="307a6-126">-ClusterName</span></span>
<span data-ttu-id="307a6-127">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="307a6-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="307a6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307a6-128">-DefaultProfile</span></span>
<span data-ttu-id="307a6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="307a6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="307a6-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="307a6-130">-ForceRemoveNode</span></span>
<span data-ttu-id="307a6-131">Если использовать этот флажок, удаление будет принудительно, даже если сервисная ткань не сможет отключить узлы.</span><span class="sxs-lookup"><span data-stu-id="307a6-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="307a6-132">Используйте эту задачу с осторожностью, так как это может привести к потере данных, если на узлах запущена рабочая нагрузка с состоянием, или привести к сужением кластера, если после пропадания не хватает узлы с данными.</span><span class="sxs-lookup"><span data-stu-id="307a6-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="307a6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="307a6-133">-InputObject</span></span>
<span data-ttu-id="307a6-134">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="307a6-134">Node type resource</span></span>

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

### <span data-ttu-id="307a6-135">-Name</span><span class="sxs-lookup"><span data-stu-id="307a6-135">-Name</span></span>
<span data-ttu-id="307a6-136">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="307a6-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="307a6-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="307a6-137">-NodeName</span></span>
<span data-ttu-id="307a6-138">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="307a6-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="307a6-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="307a6-139">-PassThru</span></span>
<span data-ttu-id="307a6-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="307a6-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="307a6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="307a6-141">-ResourceGroupName</span></span>
<span data-ttu-id="307a6-142">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="307a6-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="307a6-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="307a6-143">-ResourceId</span></span>
<span data-ttu-id="307a6-144">ИД ресурса "Тип узла"</span><span class="sxs-lookup"><span data-stu-id="307a6-144">Node type resource id</span></span>

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

### <span data-ttu-id="307a6-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="307a6-145">-Confirm</span></span>
<span data-ttu-id="307a6-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="307a6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="307a6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="307a6-147">-WhatIf</span></span>
<span data-ttu-id="307a6-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="307a6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="307a6-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="307a6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="307a6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307a6-150">CommonParameters</span></span>
<span data-ttu-id="307a6-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="307a6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307a6-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="307a6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307a6-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="307a6-153">INPUTS</span></span>

### <span data-ttu-id="307a6-154">System.String</span><span class="sxs-lookup"><span data-stu-id="307a6-154">System.String</span></span>

## <span data-ttu-id="307a6-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="307a6-155">OUTPUTS</span></span>

### <span data-ttu-id="307a6-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="307a6-156">System.Boolean</span></span>

## <span data-ttu-id="307a6-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="307a6-157">NOTES</span></span>

## <span data-ttu-id="307a6-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="307a6-158">RELATED LINKS</span></span>
