---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409599"
---
# <span data-ttu-id="7a0cb-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="7a0cb-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="7a0cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0cb-103">Удалите тип узла или конкретные узлы для этого типа.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="7a0cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a0cb-104">SYNTAX</span></span>

### <span data-ttu-id="7a0cb-105">DeleteNodeTypeByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a0cb-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0cb-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="7a0cb-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0cb-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="7a0cb-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0cb-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="7a0cb-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a0cb-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="7a0cb-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0cb-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="7a0cb-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0cb-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0cb-111">DESCRIPTION</span></span>
<span data-ttu-id="7a0cb-112">Удалите тип узла или конкретные узлы для этого типа.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="7a0cb-113">Если используется паремтер -NodeName, будут удалены только указанные узлы.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="7a0cb-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a0cb-114">EXAMPLES</span></span>

### <span data-ttu-id="7a0cb-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a0cb-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="7a0cb-116">Удалить тип узла.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-116">Remove node type.</span></span>

### <span data-ttu-id="7a0cb-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7a0cb-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="7a0cb-118">Удаление типа узла с помощью перенаноской.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="7a0cb-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7a0cb-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="7a0cb-120">Удалите 2 узла из типа узла.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="7a0cb-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7a0cb-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="7a0cb-122">Удалите 2 узла из типа узла с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="7a0cb-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a0cb-123">PARAMETERS</span></span>

### <span data-ttu-id="7a0cb-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a0cb-124">-AsJob</span></span>
<span data-ttu-id="7a0cb-125">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7a0cb-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7a0cb-126">-ClusterName</span></span>
<span data-ttu-id="7a0cb-127">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7a0cb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0cb-128">-DefaultProfile</span></span>
<span data-ttu-id="7a0cb-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a0cb-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="7a0cb-130">-ForceRemoveNode</span></span>
<span data-ttu-id="7a0cb-131">Если использовать этот флажок, удаление будет принудительно, даже если сервисная ткань не сможет отключить узлы.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="7a0cb-132">Используйте эту задачу с осторожностью, так как это может привести к потере данных, если на узлах запущена рабочая нагрузка с состоянием, или привести к сужением кластера, если после пропадания не хватает узлы с данными.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="7a0cb-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a0cb-133">-InputObject</span></span>
<span data-ttu-id="7a0cb-134">Ресурс типа узла</span><span class="sxs-lookup"><span data-stu-id="7a0cb-134">Node type resource</span></span>

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

### <span data-ttu-id="7a0cb-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7a0cb-135">-Name</span></span>
<span data-ttu-id="7a0cb-136">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="7a0cb-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="7a0cb-137">-NodeName</span></span>
<span data-ttu-id="7a0cb-138">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="7a0cb-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a0cb-139">-PassThru</span></span>
<span data-ttu-id="7a0cb-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="7a0cb-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7a0cb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0cb-141">-ResourceGroupName</span></span>
<span data-ttu-id="7a0cb-142">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7a0cb-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0cb-143">-ResourceId</span></span>
<span data-ttu-id="7a0cb-144">ИД ресурса "Тип узла"</span><span class="sxs-lookup"><span data-stu-id="7a0cb-144">Node type resource id</span></span>

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

### <span data-ttu-id="7a0cb-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a0cb-145">-Confirm</span></span>
<span data-ttu-id="7a0cb-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0cb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0cb-147">-WhatIf</span></span>
<span data-ttu-id="7a0cb-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0cb-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0cb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0cb-150">CommonParameters</span></span>
<span data-ttu-id="7a0cb-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0cb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0cb-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a0cb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0cb-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0cb-153">INPUTS</span></span>

### <span data-ttu-id="7a0cb-154">System.String</span><span class="sxs-lookup"><span data-stu-id="7a0cb-154">System.String</span></span>

## <span data-ttu-id="7a0cb-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0cb-155">OUTPUTS</span></span>

### <span data-ttu-id="7a0cb-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a0cb-156">System.Boolean</span></span>

## <span data-ttu-id="7a0cb-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a0cb-157">NOTES</span></span>

## <span data-ttu-id="7a0cb-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a0cb-158">RELATED LINKS</span></span>
