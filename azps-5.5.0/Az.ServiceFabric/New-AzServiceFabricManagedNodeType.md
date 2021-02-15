---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242080"
---
# <span data-ttu-id="fbf09-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fbf09-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="fbf09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbf09-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf09-103">Создать ресурс нового типа узла.</span><span class="sxs-lookup"><span data-stu-id="fbf09-103">Create new node type resource.</span></span>

## <span data-ttu-id="fbf09-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fbf09-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbf09-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf09-105">DESCRIPTION</span></span>
<span data-ttu-id="fbf09-106">Создайте ресурс нового типа узла для определенного кластера.</span><span class="sxs-lookup"><span data-stu-id="fbf09-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="fbf09-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fbf09-107">EXAMPLES</span></span>

### <span data-ttu-id="fbf09-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbf09-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="fbf09-109">Создание основного типа узла с 3 узлами.</span><span class="sxs-lookup"><span data-stu-id="fbf09-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="fbf09-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fbf09-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="fbf09-111">Создайте основной тип узла с 5 узлами и укажите свойства размещения, области, порты приложений и эпсисерных портов.</span><span class="sxs-lookup"><span data-stu-id="fbf09-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="fbf09-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbf09-112">PARAMETERS</span></span>

### <span data-ttu-id="fbf09-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="fbf09-113">-ApplicationEndPort</span></span>
<span data-ttu-id="fbf09-114">Порт окончания приложения для диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="fbf09-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="fbf09-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="fbf09-115">-ApplicationStartPort</span></span>
<span data-ttu-id="fbf09-116">Начальный порт приложения для диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="fbf09-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="fbf09-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbf09-117">-AsJob</span></span>
<span data-ttu-id="fbf09-118">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fbf09-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fbf09-119">-Capacity</span><span class="sxs-lookup"><span data-stu-id="fbf09-119">-Capacity</span></span>
<span data-ttu-id="fbf09-120">Теги емкости, примененные к узлам в типе узла в качестве пар ключа и значения, диспетчер ресурсов кластера использует эти теги, чтобы понять, сколько ресурсов имеет узел.</span><span class="sxs-lookup"><span data-stu-id="fbf09-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="fbf09-121">При обновлении значения будут переопределяться.</span><span class="sxs-lookup"><span data-stu-id="fbf09-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="fbf09-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fbf09-122">-ClusterName</span></span>
<span data-ttu-id="fbf09-123">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="fbf09-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fbf09-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf09-124">-DefaultProfile</span></span>
<span data-ttu-id="fbf09-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf09-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbf09-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="fbf09-126">-DiskSize</span></span>
<span data-ttu-id="fbf09-127">Размер диска для каждого VM-узла в GBs.</span><span class="sxs-lookup"><span data-stu-id="fbf09-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="fbf09-128">Значение по умолчанию: 100.</span><span class="sxs-lookup"><span data-stu-id="fbf09-128">Default 100.</span></span>

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

### <span data-ttu-id="fbf09-129">-EpenderalEndPort</span><span class="sxs-lookup"><span data-stu-id="fbf09-129">-EphemeralEndPort</span></span>
<span data-ttu-id="fbf09-130">Конечный порт в диапазоне портов.</span><span class="sxs-lookup"><span data-stu-id="fbf09-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="fbf09-131">-EpисерalStartPort</span><span class="sxs-lookup"><span data-stu-id="fbf09-131">-EphemeralStartPort</span></span>
<span data-ttu-id="fbf09-132">Эперитеральный начните порт диапазона портов.</span><span class="sxs-lookup"><span data-stu-id="fbf09-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="fbf09-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fbf09-133">-InstanceCount</span></span>
<span data-ttu-id="fbf09-134">Количество узлов в типе узла.</span><span class="sxs-lookup"><span data-stu-id="fbf09-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="fbf09-135">-Name</span><span class="sxs-lookup"><span data-stu-id="fbf09-135">-Name</span></span>
<span data-ttu-id="fbf09-136">Укажите имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="fbf09-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="fbf09-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="fbf09-137">-PlacementProperty</span></span>
<span data-ttu-id="fbf09-138">Теги размещения, применяемые к узлам в типе узла в качестве пар ключа и значения, которые могут использоваться для указать, где должны запускаться определенные службы (рабочая нагрузка).</span><span class="sxs-lookup"><span data-stu-id="fbf09-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="fbf09-139">При обновлении значения будут переопределяться.</span><span class="sxs-lookup"><span data-stu-id="fbf09-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="fbf09-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="fbf09-140">-Primary</span></span>
<span data-ttu-id="fbf09-141">Укажите, является ли тип узла основным.</span><span class="sxs-lookup"><span data-stu-id="fbf09-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="fbf09-142">Для этого типа узла будут запускаться системные службы.</span><span class="sxs-lookup"><span data-stu-id="fbf09-142">On this node type will run system services.</span></span>
<span data-ttu-id="fbf09-143">Только один тип узла должен быть помечен как основной.</span><span class="sxs-lookup"><span data-stu-id="fbf09-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="fbf09-144">Тип основного узла нельзя удалить или изменить для существующих кластеров.</span><span class="sxs-lookup"><span data-stu-id="fbf09-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="fbf09-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf09-145">-ResourceGroupName</span></span>
<span data-ttu-id="fbf09-146">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbf09-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fbf09-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="fbf09-147">-VmImageOffer</span></span>
<span data-ttu-id="fbf09-148">Тип предложения изображения Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fbf09-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="fbf09-149">По умолчанию: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="fbf09-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="fbf09-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fbf09-150">-VmImagePublisher</span></span>
<span data-ttu-id="fbf09-151">Изображение издателя виртуальной машины Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fbf09-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="fbf09-152">По умолчанию: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="fbf09-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="fbf09-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="fbf09-153">-VmImageSku</span></span>
<span data-ttu-id="fbf09-154">SKU виртуальной машины Azure Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fbf09-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="fbf09-155">По умолчанию: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="fbf09-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="fbf09-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="fbf09-156">-VmImageVersion</span></span>
<span data-ttu-id="fbf09-157">Изображение версии Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fbf09-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="fbf09-158">По умолчанию: последняя версия.</span><span class="sxs-lookup"><span data-stu-id="fbf09-158">Default: latest.</span></span>

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

### <span data-ttu-id="fbf09-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fbf09-159">-VmSize</span></span>
<span data-ttu-id="fbf09-160">Размер виртуальных машин в пуле.</span><span class="sxs-lookup"><span data-stu-id="fbf09-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="fbf09-161">Все виртуальные машины в пуле имеют одинаковый размер.</span><span class="sxs-lookup"><span data-stu-id="fbf09-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="fbf09-162">По умолчанию: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="fbf09-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="fbf09-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbf09-163">-Confirm</span></span>
<span data-ttu-id="fbf09-164">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbf09-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbf09-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbf09-165">-WhatIf</span></span>
<span data-ttu-id="fbf09-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbf09-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbf09-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fbf09-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbf09-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf09-168">CommonParameters</span></span>
<span data-ttu-id="fbf09-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf09-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf09-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbf09-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf09-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbf09-171">INPUTS</span></span>

### <span data-ttu-id="fbf09-172">System.String</span><span class="sxs-lookup"><span data-stu-id="fbf09-172">System.String</span></span>

## <span data-ttu-id="fbf09-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fbf09-173">OUTPUTS</span></span>

### <span data-ttu-id="fbf09-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fbf09-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="fbf09-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fbf09-175">NOTES</span></span>

## <span data-ttu-id="fbf09-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbf09-176">RELATED LINKS</span></span>
