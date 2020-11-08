---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246537"
---
# <span data-ttu-id="f6dd5-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f6dd5-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="f6dd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="f6dd5-103">Создайте ресурс нового типа узла.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-103">Create new node type resource.</span></span>

## <span data-ttu-id="f6dd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6dd5-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6dd5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="f6dd5-106">Создание ресурса типа нового узла для определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="f6dd5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="f6dd5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6dd5-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="f6dd5-109">Создание типа основного узла с тремя узлами.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="f6dd5-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f6dd5-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="f6dd5-111">Создать тип основного узла с 5 узлами и задать свойства размещения, емкость, приложение и временные порты.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="f6dd5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6dd5-112">PARAMETERS</span></span>

### <span data-ttu-id="f6dd5-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="f6dd5-113">-ApplicationEndPort</span></span>
<span data-ttu-id="f6dd5-114">Конечный порт приложения диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="f6dd5-115">-ApplicationStartPort</span></span>
<span data-ttu-id="f6dd5-116">Порт запуска приложения в диапазоне портов.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6dd5-117">-AsJob</span></span>
<span data-ttu-id="f6dd5-118">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f6dd5-119">-Capacity</span><span class="sxs-lookup"><span data-stu-id="f6dd5-119">-Capacity</span></span>
<span data-ttu-id="f6dd5-120">Теги производственных мощностей, примененные к узлам в типе узла в виде пар "ключ-значение", диспетчер ресурсов кластера использует эти теги для понимания того, сколько ресурсов имеет узел.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="f6dd5-121">После обновления текущие значения будут переопределены.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-122">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="f6dd5-122">-ClusterName</span></span>
<span data-ttu-id="f6dd5-123">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f6dd5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6dd5-124">-DefaultProfile</span></span>
<span data-ttu-id="f6dd5-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6dd5-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="f6dd5-126">-DiskSize</span></span>
<span data-ttu-id="f6dd5-127">Размер диска для каждой виртуальной машины в типе узла ГБ.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="f6dd5-128">100 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-128">Default 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="f6dd5-129">-EphemeralEndPort</span></span>
<span data-ttu-id="f6dd5-130">Эфемерный конечный порт диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="f6dd5-131">-EphemeralStartPort</span></span>
<span data-ttu-id="f6dd5-132">Временный начальный порт диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="f6dd5-133">-InstanceCount</span></span>
<span data-ttu-id="f6dd5-134">Количество узлов в типе узла.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6dd5-135">-Name</span></span>
<span data-ttu-id="f6dd5-136">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="f6dd5-137">-PlacementProperty</span></span>
<span data-ttu-id="f6dd5-138">Теги размещения применяются к узлам в типе узла в виде пар "ключ-значение", которые можно использовать, чтобы указать, где должны выполняться определенные службы (рабочей нагрузки).</span><span class="sxs-lookup"><span data-stu-id="f6dd5-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="f6dd5-139">После обновления текущие значения будут переопределены.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="f6dd5-140">-Primary</span></span>
<span data-ttu-id="f6dd5-141">Укажите, является ли тип узла основным.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="f6dd5-142">На этом типе узла будут запущены системные службы.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-142">On this node type will run system services.</span></span>
<span data-ttu-id="f6dd5-143">Только один тип узла должен быть помечен как основной.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="f6dd5-144">Тип основного узла нельзя удалить или изменить для существующих кластеров.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="f6dd5-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6dd5-145">-ResourceGroupName</span></span>
<span data-ttu-id="f6dd5-146">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f6dd5-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="f6dd5-147">-VmImageOffer</span></span>
<span data-ttu-id="f6dd5-148">Тип предложения для образа магазина виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="f6dd5-149">По умолчанию: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f6dd5-150">-VmImagePublisher</span></span>
<span data-ttu-id="f6dd5-151">Издатель образа Marketplace для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="f6dd5-152">По умолчанию: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="f6dd5-153">-VmImageSku</span></span>
<span data-ttu-id="f6dd5-154">SKU образа рынка виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="f6dd5-155">По умолчанию: 2019 — центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="f6dd5-156">-VmImageVersion</span></span>
<span data-ttu-id="f6dd5-157">Версия образа Marketplace для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="f6dd5-158">По умолчанию: latest.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="f6dd5-159">-VmSize</span></span>
<span data-ttu-id="f6dd5-160">Размер виртуальных машин в пуле.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="f6dd5-161">Все виртуальные машины в пуле имеют одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="f6dd5-162">По умолчанию: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6dd5-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6dd5-163">-Confirm</span></span>
<span data-ttu-id="f6dd5-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6dd5-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6dd5-165">-WhatIf</span></span>
<span data-ttu-id="f6dd5-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6dd5-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6dd5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6dd5-168">CommonParameters</span></span>
<span data-ttu-id="f6dd5-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6dd5-170">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6dd5-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6dd5-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6dd5-171">INPUTS</span></span>

### <span data-ttu-id="f6dd5-172">System. String</span><span class="sxs-lookup"><span data-stu-id="f6dd5-172">System.String</span></span>

## <span data-ttu-id="f6dd5-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6dd5-173">OUTPUTS</span></span>

### <span data-ttu-id="f6dd5-174">Microsoft. Azure. Commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="f6dd5-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="f6dd5-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6dd5-175">NOTES</span></span>

## <span data-ttu-id="f6dd5-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6dd5-176">RELATED LINKS</span></span>
