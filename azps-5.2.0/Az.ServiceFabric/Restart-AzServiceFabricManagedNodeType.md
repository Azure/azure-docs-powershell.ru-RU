---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391455"
---
# <span data-ttu-id="32831-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="32831-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="32831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32831-102">SYNOPSIS</span></span>
<span data-ttu-id="32831-103">Перезапустите определенные узлы из типа узла.</span><span class="sxs-lookup"><span data-stu-id="32831-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="32831-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32831-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32831-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32831-105">DESCRIPTION</span></span>
<span data-ttu-id="32831-106">Перезапустите определенные узлы из типа узла.</span><span class="sxs-lookup"><span data-stu-id="32831-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="32831-107">Он отключит узлы с тканью службы перед перезапуском vms и снова их снова запустит.</span><span class="sxs-lookup"><span data-stu-id="32831-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="32831-108">Если это делается для основных типов узлов, это может занять некоторое время, так как может не перезапустить все узлы одновременно.</span><span class="sxs-lookup"><span data-stu-id="32831-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="32831-109">Использование -ForceRestart вызывает операцию, даже если сервисный материал не может отключить узлы, но следует соблюдать осторожность, так как это может привести к потере данных, если на узле работают рабочие нагрузки с состоянием.</span><span class="sxs-lookup"><span data-stu-id="32831-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="32831-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32831-110">EXAMPLES</span></span>

### <span data-ttu-id="32831-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32831-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="32831-112">Перезапустите узел 0 и 3 для типа узла.</span><span class="sxs-lookup"><span data-stu-id="32831-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="32831-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32831-113">PARAMETERS</span></span>

### <span data-ttu-id="32831-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32831-114">-AsJob</span></span>
<span data-ttu-id="32831-115">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="32831-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="32831-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="32831-116">-ClusterName</span></span>
<span data-ttu-id="32831-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="32831-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="32831-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32831-118">-DefaultProfile</span></span>
<span data-ttu-id="32831-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32831-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32831-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="32831-120">-ForceRestart</span></span>
<span data-ttu-id="32831-121">При использовании этого флажка узел будет перезагружаться, даже если сервисный материал не сможет отключить узлы.</span><span class="sxs-lookup"><span data-stu-id="32831-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="32831-122">-Name</span><span class="sxs-lookup"><span data-stu-id="32831-122">-Name</span></span>
<span data-ttu-id="32831-123">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="32831-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32831-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="32831-124">-NodeName</span></span>
<span data-ttu-id="32831-125">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="32831-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32831-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32831-126">-PassThru</span></span>
<span data-ttu-id="32831-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="32831-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="32831-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32831-128">-ResourceGroupName</span></span>
<span data-ttu-id="32831-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="32831-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="32831-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32831-130">-Confirm</span></span>
<span data-ttu-id="32831-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32831-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32831-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32831-132">-WhatIf</span></span>
<span data-ttu-id="32831-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32831-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32831-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32831-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32831-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32831-135">CommonParameters</span></span>
<span data-ttu-id="32831-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32831-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32831-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32831-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32831-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32831-138">INPUTS</span></span>

### <span data-ttu-id="32831-139">System.String</span><span class="sxs-lookup"><span data-stu-id="32831-139">System.String</span></span>

## <span data-ttu-id="32831-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32831-140">OUTPUTS</span></span>

### <span data-ttu-id="32831-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32831-141">System.Boolean</span></span>

## <span data-ttu-id="32831-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32831-142">NOTES</span></span>

## <span data-ttu-id="32831-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32831-143">RELATED LINKS</span></span>