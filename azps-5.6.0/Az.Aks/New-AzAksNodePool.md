---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 07944177b7c92ff4c515b6d9dcd01d11d3c5a888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962563"
---
# <span data-ttu-id="1b782-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="1b782-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="1b782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b782-102">SYNOPSIS</span></span>
<span data-ttu-id="1b782-103">Создайте новый пул узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="1b782-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="1b782-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b782-104">SYNTAX</span></span>

### <span data-ttu-id="1b782-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b782-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b782-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b782-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b782-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b782-107">DESCRIPTION</span></span>
<span data-ttu-id="1b782-108">Создайте новый пул узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="1b782-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="1b782-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b782-109">EXAMPLES</span></span>

### <span data-ttu-id="1b782-110">Создание пула узлов с параметрами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1b782-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="1b782-111">Создание контейнера Windows Server на сервере AKS</span><span class="sxs-lookup"><span data-stu-id="1b782-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="1b782-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b782-112">PARAMETERS</span></span>

### <span data-ttu-id="1b782-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1b782-113">-ClusterName</span></span>
<span data-ttu-id="1b782-114">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="1b782-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="1b782-115">-ClusterObject</span></span>
<span data-ttu-id="1b782-116">Укажите объект кластера, в котором нужно создать пул узлов.</span><span class="sxs-lookup"><span data-stu-id="1b782-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-117">-Count</span><span class="sxs-lookup"><span data-stu-id="1b782-117">-Count</span></span>
<span data-ttu-id="1b782-118">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="1b782-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1b782-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b782-119">-DefaultProfile</span></span>
<span data-ttu-id="1b782-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b782-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b782-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="1b782-121">-EnableAutoScaling</span></span>
<span data-ttu-id="1b782-122">Следует ли включить авторе шкалу</span><span class="sxs-lookup"><span data-stu-id="1b782-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="1b782-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1b782-123">-Force</span></span>
<span data-ttu-id="1b782-124">Создание пула узлов, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="1b782-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="1b782-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="1b782-125">-KubernetesVersion</span></span>
<span data-ttu-id="1b782-126">Версия Кубберсетей, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="1b782-126">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1b782-127">-MaxCount</span></span>
<span data-ttu-id="1b782-128">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="1b782-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="1b782-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="1b782-129">-MaxPodCount</span></span>
<span data-ttu-id="1b782-130">Максимальное количество pods, которые могут запускаться в узле.</span><span class="sxs-lookup"><span data-stu-id="1b782-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="1b782-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="1b782-131">-MinCount</span></span>
<span data-ttu-id="1b782-132">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1b782-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="1b782-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1b782-133">-Name</span></span>
<span data-ttu-id="1b782-134">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="1b782-134">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="1b782-135">-OsDiskSize</span></span>
<span data-ttu-id="1b782-136">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="1b782-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="1b782-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="1b782-137">-OsType</span></span>
<span data-ttu-id="1b782-138">OsType, используемый для указания типа оси.</span><span class="sxs-lookup"><span data-stu-id="1b782-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="1b782-139">Выберите Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="1b782-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="1b782-140">Значение по умолчанию для Linux.</span><span class="sxs-lookup"><span data-stu-id="1b782-140">Default to Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b782-141">-ResourceGroupName</span></span>
<span data-ttu-id="1b782-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b782-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="1b782-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="1b782-144">ScaleSetEvictionPolicy, которая используется для указания политики разборки для набора виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="1b782-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="1b782-145">Значение по умолчанию для удаления.</span><span class="sxs-lookup"><span data-stu-id="1b782-145">Default to Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="1b782-146">-ScaleSetPriority</span></span>
<span data-ttu-id="1b782-147">ScaleSetPriority, используемое для указания приоритета набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b782-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="1b782-148">Значение по умолчанию ( обычный).</span><span class="sxs-lookup"><span data-stu-id="1b782-148">Default to regular.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="1b782-149">-VmSetType</span></span>
<span data-ttu-id="1b782-150">Представляет типы пула узлов.</span><span class="sxs-lookup"><span data-stu-id="1b782-150">Represents types of an node pool.</span></span>
<span data-ttu-id="1b782-151">Возможные значения: 'VirtualMachineScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="1b782-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="1b782-152">-VmSize</span></span>
<span data-ttu-id="1b782-153">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1b782-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="1b782-154">Значение по умолчанию — Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="1b782-154">Default value is Standard_D2_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="1b782-155">-VnetSubnetID</span></span>
<span data-ttu-id="1b782-156">Код подсети VNet указывает идентификатор подсети VNet.</span><span class="sxs-lookup"><span data-stu-id="1b782-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b782-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b782-157">-Confirm</span></span>
<span data-ttu-id="1b782-158">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b782-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b782-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b782-159">-WhatIf</span></span>
<span data-ttu-id="1b782-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b782-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b782-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b782-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b782-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b782-162">CommonParameters</span></span>
<span data-ttu-id="1b782-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b782-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b782-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b782-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b782-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b782-165">INPUTS</span></span>

### <span data-ttu-id="1b782-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="1b782-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="1b782-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b782-167">OUTPUTS</span></span>

### <span data-ttu-id="1b782-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="1b782-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="1b782-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b782-169">NOTES</span></span>

## <span data-ttu-id="1b782-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b782-170">RELATED LINKS</span></span>
