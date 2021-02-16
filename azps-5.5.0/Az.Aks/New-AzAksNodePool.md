---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233908"
---
# <span data-ttu-id="240e7-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="240e7-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="240e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="240e7-102">SYNOPSIS</span></span>
<span data-ttu-id="240e7-103">Создайте новый пул узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="240e7-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="240e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="240e7-104">SYNTAX</span></span>

### <span data-ttu-id="240e7-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="240e7-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="240e7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="240e7-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="240e7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="240e7-107">DESCRIPTION</span></span>
<span data-ttu-id="240e7-108">Создайте новый пул узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="240e7-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="240e7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="240e7-109">EXAMPLES</span></span>

### <span data-ttu-id="240e7-110">Создание пула узлов с параметрами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="240e7-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="240e7-111">Создание контейнера Windows Server на сервере AKS</span><span class="sxs-lookup"><span data-stu-id="240e7-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="240e7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="240e7-112">PARAMETERS</span></span>

### <span data-ttu-id="240e7-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="240e7-113">-ClusterName</span></span>
<span data-ttu-id="240e7-114">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="240e7-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="240e7-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="240e7-115">-ClusterObject</span></span>
<span data-ttu-id="240e7-116">Укажите объект кластера, в котором нужно создать пул узлов.</span><span class="sxs-lookup"><span data-stu-id="240e7-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="240e7-117">-Count</span><span class="sxs-lookup"><span data-stu-id="240e7-117">-Count</span></span>
<span data-ttu-id="240e7-118">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="240e7-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="240e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240e7-119">-DefaultProfile</span></span>
<span data-ttu-id="240e7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="240e7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240e7-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="240e7-121">-EnableAutoScaling</span></span>
<span data-ttu-id="240e7-122">Следует ли включить авторе шкалу</span><span class="sxs-lookup"><span data-stu-id="240e7-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="240e7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="240e7-123">-Force</span></span>
<span data-ttu-id="240e7-124">Создание пула узлов, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="240e7-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="240e7-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="240e7-125">-KubernetesVersion</span></span>
<span data-ttu-id="240e7-126">Версия Кубберсетей, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="240e7-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="240e7-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="240e7-127">-MaxCount</span></span>
<span data-ttu-id="240e7-128">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="240e7-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="240e7-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="240e7-129">-MaxPodCount</span></span>
<span data-ttu-id="240e7-130">Максимальное количество pods, которые могут запускаться в узле.</span><span class="sxs-lookup"><span data-stu-id="240e7-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="240e7-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="240e7-131">-MinCount</span></span>
<span data-ttu-id="240e7-132">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="240e7-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="240e7-133">-Name</span><span class="sxs-lookup"><span data-stu-id="240e7-133">-Name</span></span>
<span data-ttu-id="240e7-134">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="240e7-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="240e7-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="240e7-135">-OsDiskSize</span></span>
<span data-ttu-id="240e7-136">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="240e7-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="240e7-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="240e7-137">-OsType</span></span>
<span data-ttu-id="240e7-138">OsType, используемый для указания типа оси.</span><span class="sxs-lookup"><span data-stu-id="240e7-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="240e7-139">Выберите Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="240e7-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="240e7-140">Значение по умолчанию для Linux.</span><span class="sxs-lookup"><span data-stu-id="240e7-140">Default to Linux.</span></span>

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

### <span data-ttu-id="240e7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240e7-141">-ResourceGroupName</span></span>
<span data-ttu-id="240e7-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="240e7-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="240e7-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="240e7-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="240e7-144">ScaleSetEvictionPolicy, которая используется для указания политики разборки для набора виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="240e7-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="240e7-145">Значение по умолчанию для удаления.</span><span class="sxs-lookup"><span data-stu-id="240e7-145">Default to Delete.</span></span>

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

### <span data-ttu-id="240e7-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="240e7-146">-ScaleSetPriority</span></span>
<span data-ttu-id="240e7-147">ScaleSetPriority, используемое для указания приоритета набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="240e7-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="240e7-148">Значение по умолчанию ( обычный).</span><span class="sxs-lookup"><span data-stu-id="240e7-148">Default to regular.</span></span>

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

### <span data-ttu-id="240e7-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="240e7-149">-VmSetType</span></span>
<span data-ttu-id="240e7-150">Представляет типы пула узлов.</span><span class="sxs-lookup"><span data-stu-id="240e7-150">Represents types of an node pool.</span></span>
<span data-ttu-id="240e7-151">Возможные значения: 'VirtualMascaleeScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="240e7-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="240e7-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="240e7-152">-VmSize</span></span>
<span data-ttu-id="240e7-153">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="240e7-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="240e7-154">Значение по умолчанию — Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="240e7-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="240e7-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="240e7-155">-VnetSubnetID</span></span>
<span data-ttu-id="240e7-156">Код подсети VNet указывает идентификатор подсети VNet.</span><span class="sxs-lookup"><span data-stu-id="240e7-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="240e7-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="240e7-157">-Confirm</span></span>
<span data-ttu-id="240e7-158">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="240e7-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="240e7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="240e7-159">-WhatIf</span></span>
<span data-ttu-id="240e7-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="240e7-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="240e7-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="240e7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="240e7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240e7-162">CommonParameters</span></span>
<span data-ttu-id="240e7-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="240e7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240e7-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="240e7-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240e7-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="240e7-165">INPUTS</span></span>

### <span data-ttu-id="240e7-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="240e7-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="240e7-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="240e7-167">OUTPUTS</span></span>

### <span data-ttu-id="240e7-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="240e7-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="240e7-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="240e7-169">NOTES</span></span>

## <span data-ttu-id="240e7-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="240e7-170">RELATED LINKS</span></span>
