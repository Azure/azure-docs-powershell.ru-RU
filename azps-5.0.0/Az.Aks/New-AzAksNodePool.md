---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247112"
---
# <span data-ttu-id="76201-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="76201-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="76201-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76201-102">SYNOPSIS</span></span>
<span data-ttu-id="76201-103">Создание пула узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="76201-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="76201-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76201-104">SYNTAX</span></span>

### <span data-ttu-id="76201-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="76201-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76201-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76201-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76201-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76201-107">DESCRIPTION</span></span>
<span data-ttu-id="76201-108">Создание пула узлов в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="76201-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="76201-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76201-109">EXAMPLES</span></span>

### <span data-ttu-id="76201-110">Создание пула узлов с параметрами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="76201-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="76201-111">Создание контейнера Windows Server на AKS</span><span class="sxs-lookup"><span data-stu-id="76201-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="76201-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76201-112">PARAMETERS</span></span>

### <span data-ttu-id="76201-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="76201-113">-ClusterName</span></span>
<span data-ttu-id="76201-114">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="76201-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="76201-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="76201-115">-ClusterObject</span></span>
<span data-ttu-id="76201-116">Укажите объект кластера для создания пула узлов.</span><span class="sxs-lookup"><span data-stu-id="76201-116">Specify cluster object in which to create node pool.</span></span>

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

### <span data-ttu-id="76201-117">— Количество</span><span class="sxs-lookup"><span data-stu-id="76201-117">-Count</span></span>
<span data-ttu-id="76201-118">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="76201-118">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="76201-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76201-119">-DefaultProfile</span></span>
<span data-ttu-id="76201-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76201-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76201-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="76201-121">-EnableAutoScaling</span></span>
<span data-ttu-id="76201-122">Следует ли включить автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="76201-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="76201-123">-Force</span><span class="sxs-lookup"><span data-stu-id="76201-123">-Force</span></span>
<span data-ttu-id="76201-124">Создание пула узлов, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="76201-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="76201-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="76201-125">-KubernetesVersion</span></span>
<span data-ttu-id="76201-126">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="76201-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="76201-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="76201-127">-MaxCount</span></span>
<span data-ttu-id="76201-128">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="76201-128">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="76201-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="76201-129">-MaxPodCount</span></span>
<span data-ttu-id="76201-130">Максимальное количество обыкновенных модулей, которые могут работать на узле.</span><span class="sxs-lookup"><span data-stu-id="76201-130">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="76201-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="76201-131">-MinCount</span></span>
<span data-ttu-id="76201-132">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="76201-132">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="76201-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76201-133">-Name</span></span>
<span data-ttu-id="76201-134">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="76201-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="76201-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="76201-135">-OsDiskSize</span></span>
<span data-ttu-id="76201-136">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="76201-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="76201-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="76201-137">-OsType</span></span>
<span data-ttu-id="76201-138">OsType, который будет использоваться для указания типа ОС.</span><span class="sxs-lookup"><span data-stu-id="76201-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="76201-139">Выберите один из Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="76201-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="76201-140">По умолчанию для Linux.</span><span class="sxs-lookup"><span data-stu-id="76201-140">Default to Linux.</span></span>

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

### <span data-ttu-id="76201-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76201-141">-ResourceGroupName</span></span>
<span data-ttu-id="76201-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76201-142">The name of the resource group.</span></span>

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

### <span data-ttu-id="76201-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="76201-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="76201-144">ScaleSetEvictionPolicy, который будет использоваться для указания политики вытесненности для установленного уровня с низким приоритетом виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="76201-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="76201-145">По умолчанию удалить.</span><span class="sxs-lookup"><span data-stu-id="76201-145">Default to Delete.</span></span>

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

### <span data-ttu-id="76201-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="76201-146">-ScaleSetPriority</span></span>
<span data-ttu-id="76201-147">ScaleSetPriority, который будет использоваться для задания приоритета для установки масштаба виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="76201-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="76201-148">По умолчанию используется обычный.</span><span class="sxs-lookup"><span data-stu-id="76201-148">Default to regular.</span></span>

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

### <span data-ttu-id="76201-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="76201-149">-VmSetType</span></span>
<span data-ttu-id="76201-150">Представляет типы пула узлов.</span><span class="sxs-lookup"><span data-stu-id="76201-150">Represents types of an node pool.</span></span>
<span data-ttu-id="76201-151">Возможные значения: "VirtualMachineScaleSets", "Группа доступности"</span><span class="sxs-lookup"><span data-stu-id="76201-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="76201-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="76201-152">-VmSize</span></span>
<span data-ttu-id="76201-153">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="76201-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="76201-154">Значение по умолчанию — Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="76201-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="76201-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="76201-155">-VnetSubnetID</span></span>
<span data-ttu-id="76201-156">VNet SubnetID указывает идентификатор подсети VNet.</span><span class="sxs-lookup"><span data-stu-id="76201-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="76201-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76201-157">-Confirm</span></span>
<span data-ttu-id="76201-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76201-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76201-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76201-159">-WhatIf</span></span>
<span data-ttu-id="76201-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76201-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76201-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76201-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76201-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76201-162">CommonParameters</span></span>
<span data-ttu-id="76201-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76201-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76201-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76201-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76201-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76201-165">INPUTS</span></span>

### <span data-ttu-id="76201-166">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="76201-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="76201-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76201-167">OUTPUTS</span></span>

### <span data-ttu-id="76201-168">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="76201-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="76201-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="76201-169">NOTES</span></span>

## <span data-ttu-id="76201-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76201-170">RELATED LINKS</span></span>
