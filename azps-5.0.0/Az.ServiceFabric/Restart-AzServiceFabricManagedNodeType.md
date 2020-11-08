---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245853"
---
# <span data-ttu-id="8f730-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="8f730-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="8f730-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f730-102">SYNOPSIS</span></span>
<span data-ttu-id="8f730-103">Перезагрузите определенные узлы из типа узла.</span><span class="sxs-lookup"><span data-stu-id="8f730-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="8f730-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f730-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f730-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f730-105">DESCRIPTION</span></span>
<span data-ttu-id="8f730-106">Перезагрузите определенные узлы из типа узла.</span><span class="sxs-lookup"><span data-stu-id="8f730-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="8f730-107">После повторного запуска виртуальных компьютеров они будут отключены и снова включены после обратного.</span><span class="sxs-lookup"><span data-stu-id="8f730-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="8f730-108">Если это делается для основных типов узлов, может потребоваться некоторое время, так как может не перезапускаться сразу все узлы.</span><span class="sxs-lookup"><span data-stu-id="8f730-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="8f730-109">Функция-ForceRestart принудительно выполняет операцию, даже если фабрика служб не может отключить узлы, но используется с осторожностью, так как это может привести к потере данных, если на узле выполняются нагрузки с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="8f730-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="8f730-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f730-110">EXAMPLES</span></span>

### <span data-ttu-id="8f730-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f730-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="8f730-112">Перезапустите узлы 0 и 3 для типа узла.</span><span class="sxs-lookup"><span data-stu-id="8f730-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="8f730-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f730-113">PARAMETERS</span></span>

### <span data-ttu-id="8f730-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f730-114">-AsJob</span></span>
<span data-ttu-id="8f730-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="8f730-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8f730-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="8f730-116">-ClusterName</span></span>
<span data-ttu-id="8f730-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="8f730-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8f730-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f730-118">-DefaultProfile</span></span>
<span data-ttu-id="8f730-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f730-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f730-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="8f730-120">-ForceRestart</span></span>
<span data-ttu-id="8f730-121">Использование этого флага приводит к принудительному перезапуску узла, даже если не удалось отключить узлы в структуре служб.</span><span class="sxs-lookup"><span data-stu-id="8f730-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="8f730-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f730-122">-Name</span></span>
<span data-ttu-id="8f730-123">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="8f730-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="8f730-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="8f730-124">-NodeName</span></span>
<span data-ttu-id="8f730-125">Список имен узлов для операции.</span><span class="sxs-lookup"><span data-stu-id="8f730-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="8f730-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f730-126">-PassThru</span></span>
<span data-ttu-id="8f730-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="8f730-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8f730-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f730-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f730-129">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f730-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8f730-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f730-130">-Confirm</span></span>
<span data-ttu-id="8f730-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f730-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f730-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f730-132">-WhatIf</span></span>
<span data-ttu-id="8f730-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f730-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f730-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f730-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f730-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f730-135">CommonParameters</span></span>
<span data-ttu-id="8f730-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f730-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f730-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f730-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f730-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f730-138">INPUTS</span></span>

### <span data-ttu-id="8f730-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8f730-139">System.String</span></span>

## <span data-ttu-id="8f730-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f730-140">OUTPUTS</span></span>

### <span data-ttu-id="8f730-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f730-141">System.Boolean</span></span>

## <span data-ttu-id="8f730-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f730-142">NOTES</span></span>

## <span data-ttu-id="8f730-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f730-143">RELATED LINKS</span></span>
