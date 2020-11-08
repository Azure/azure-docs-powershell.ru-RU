---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: f7a3479fb7fd70c47d5d4d3b80004cb25d9baa0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235165"
---
# <span data-ttu-id="7e67b-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="7e67b-101">New-AzAksCluster</span></span>

## <span data-ttu-id="7e67b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e67b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e67b-103">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7e67b-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7e67b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e67b-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeOsType <String>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
 [-NodeScaleSetEvictionPolicy <String>] [-AddOnNameToBeEnabled <String[]>] [-WorkspaceResourceId <String>]
 [-SubnetName <String>] [-AcrNameToAttach <String>] [-EnableRbac] [-WindowsProfileAdminUserName <String>]
 [-WindowsProfileAdminUserPassword <SecureString>] [-NetworkPlugin <String>] [-LoadBalancerSku <String>]
 [-ResourceGroupName] <String> [-Name] <String> [[-ServicePrincipalIdAndSecret] <PSCredential>]
 [-Location <String>] [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>]
 [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e67b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e67b-105">DESCRIPTION</span></span>

<span data-ttu-id="7e67b-106">Создайте новый кластер служб Azure Kubernetes (AKS).</span><span class="sxs-lookup"><span data-stu-id="7e67b-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="7e67b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e67b-107">EXAMPLES</span></span>

### <span data-ttu-id="7e67b-108">Новые параметры AKS с параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e67b-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="7e67b-109">Создайте контейнер Windows Server на AKS.</span><span class="sxs-lookup"><span data-stu-id="7e67b-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="7e67b-110">Чтобы создать контейнер Windows Server на AKS, при создании AKS необходимо указать по крайней мере четыре следующих параметра, а для параметра `NetworkPlugin` и `NodeVmSetType` должны быть `azure` и `VirtualMachineScaleSets` соответственно.</span><span class="sxs-lookup"><span data-stu-id="7e67b-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="7e67b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e67b-111">PARAMETERS</span></span>

### <span data-ttu-id="7e67b-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="7e67b-112">-AcrNameToAttach</span></span>
<span data-ttu-id="7e67b-113">Предоставьте роль "acrpull" указанной записью контроля доступа AKS субъекта-службы, например myacr</span><span class="sxs-lookup"><span data-stu-id="7e67b-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="7e67b-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="7e67b-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="7e67b-115">Имена надстроек, которые будут включены при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="7e67b-115">Add-on names to be enabled when cluster is created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e67b-116">-AsJob</span></span>
<span data-ttu-id="7e67b-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7e67b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e67b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e67b-118">-DefaultProfile</span></span>
<span data-ttu-id="7e67b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e67b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e67b-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="7e67b-120">-DnsNamePrefix</span></span>
<span data-ttu-id="7e67b-121">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="7e67b-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="7e67b-122">Длина должна быть <= 9, если пользователи планирует добавить контейнер Windows.</span><span class="sxs-lookup"><span data-stu-id="7e67b-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="7e67b-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="7e67b-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="7e67b-124">Следует ли включить автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="7e67b-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="7e67b-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="7e67b-125">-EnableRbac</span></span>
<span data-ttu-id="7e67b-126">Следует ли включить доступ Kubernetes Role-Based</span><span class="sxs-lookup"><span data-stu-id="7e67b-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="7e67b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7e67b-127">-Force</span></span>
<span data-ttu-id="7e67b-128">Создать кластер, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="7e67b-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="7e67b-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="7e67b-129">-GenerateSshKey</span></span>
<span data-ttu-id="7e67b-130">Создание файла ключа SSH для {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="7e67b-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="7e67b-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="7e67b-131">-KubernetesVersion</span></span>
<span data-ttu-id="7e67b-132">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="7e67b-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="7e67b-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="7e67b-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="7e67b-134">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="7e67b-134">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="7e67b-135">-LoadBalancerSku</span></span>
<span data-ttu-id="7e67b-136">SKU подсистемы балансировки нагрузки для управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="7e67b-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="7e67b-137">-Location</span><span class="sxs-lookup"><span data-stu-id="7e67b-137">-Location</span></span>
<span data-ttu-id="7e67b-138">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="7e67b-138">Azure location for the cluster.</span></span>
<span data-ttu-id="7e67b-139">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="7e67b-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e67b-140">-Name</span></span>
<span data-ttu-id="7e67b-141">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7e67b-141">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="7e67b-142">-NetworkPlugin</span></span>
<span data-ttu-id="7e67b-143">Сетевой подключаемый модуль, используемый для создания сети Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="7e67b-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="7e67b-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="7e67b-144">-NodeCount</span></span>
<span data-ttu-id="7e67b-145">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="7e67b-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="7e67b-146">-NodeMaxCount</span></span>
<span data-ttu-id="7e67b-147">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="7e67b-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="7e67b-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="7e67b-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="7e67b-149">Максимальное количество обыкновенных модулей, которые могут работать на узле.</span><span class="sxs-lookup"><span data-stu-id="7e67b-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="7e67b-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="7e67b-150">-NodeMinCount</span></span>
<span data-ttu-id="7e67b-151">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7e67b-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="7e67b-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="7e67b-152">-NodeName</span></span>
<span data-ttu-id="7e67b-153">Уникальное имя профиля пула агентов в контексте подписок и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="7e67b-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="7e67b-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="7e67b-155">Размер диска операционной системы (ГБ) для каждого узла в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="7e67b-156">Минимум 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="7e67b-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="7e67b-157">-NodeOsType</span><span class="sxs-lookup"><span data-stu-id="7e67b-157">-NodeOsType</span></span>
<span data-ttu-id="7e67b-158">OsType, который будет использоваться для указания типа ОС.</span><span class="sxs-lookup"><span data-stu-id="7e67b-158">OsType to be used to specify os type.</span></span> <span data-ttu-id="7e67b-159">Выберите один из Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="7e67b-159">Choose from Linux and Windows.</span></span> <span data-ttu-id="7e67b-160">По умолчанию для Linux.</span><span class="sxs-lookup"><span data-stu-id="7e67b-160">Default to Linux.</span></span>

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

### <span data-ttu-id="7e67b-161">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="7e67b-161">-NodePoolMode</span></span>
<span data-ttu-id="7e67b-162">NodePoolMode представляет режим пула узлов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-162">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="7e67b-163">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e67b-163">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="7e67b-164">ScaleSetEvictionPolicy, который будет использоваться для указания политики вытесненности для установленного уровня с низким приоритетом виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7e67b-164">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="7e67b-165">По умолчанию удалить.</span><span class="sxs-lookup"><span data-stu-id="7e67b-165">Default to Delete.</span></span>

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

### <span data-ttu-id="7e67b-166">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="7e67b-166">-NodeSetPriority</span></span>
<span data-ttu-id="7e67b-167">ScaleSetPriority, который будет использоваться для задания приоритета для установки масштаба виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7e67b-167">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="7e67b-168">По умолчанию используется обычный.</span><span class="sxs-lookup"><span data-stu-id="7e67b-168">Default to regular.</span></span>

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

### <span data-ttu-id="7e67b-169">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="7e67b-169">-NodeVmSetType</span></span>
<span data-ttu-id="7e67b-170">AgentPoolType представляет типы пула агентов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-170">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="7e67b-171">Возможные значения: "VirtualMachineScaleSets", "Группа доступности"</span><span class="sxs-lookup"><span data-stu-id="7e67b-171">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="7e67b-172">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="7e67b-172">-NodeVmSize</span></span>
<span data-ttu-id="7e67b-173">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7e67b-173">The size of the Virtual Machine.</span></span> <span data-ttu-id="7e67b-174">Значение по умолчанию — Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="7e67b-174">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="7e67b-175">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="7e67b-175">-NodeVnetSubnetID</span></span>
<span data-ttu-id="7e67b-176">VNet SubnetID указывает идентификатор подсети VNet.</span><span class="sxs-lookup"><span data-stu-id="7e67b-176">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="7e67b-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e67b-177">-ResourceGroupName</span></span>
<span data-ttu-id="7e67b-178">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e67b-178">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-179">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="7e67b-179">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="7e67b-180">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="7e67b-180">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClientIdAndSecret

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-181">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="7e67b-181">-SshKeyValue</span></span>
<span data-ttu-id="7e67b-182">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="7e67b-182">SSH key file value or key file path.</span></span>
<span data-ttu-id="7e67b-183">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="7e67b-183">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-184">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7e67b-184">-SubnetName</span></span>
<span data-ttu-id="7e67b-185">Имя подсети надстройки VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="7e67b-185">Subnet name of VirtualNode addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-186">-Тег</span><span class="sxs-lookup"><span data-stu-id="7e67b-186">-Tag</span></span>
<span data-ttu-id="7e67b-187">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="7e67b-187">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="7e67b-188">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="7e67b-188">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="7e67b-189">Имя пользователя администратора, используемое для виртуальных машин Windows.</span><span class="sxs-lookup"><span data-stu-id="7e67b-189">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="7e67b-190">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="7e67b-190">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="7e67b-191">Пароль администратора для Windows VM, его длина должна быть не менее 12, в которой есть хотя бы один знак нижнего регистра, например `[a-z]` один `[A-Z]` и один специальный символ `[!@#$%^&*()]` .</span><span class="sxs-lookup"><span data-stu-id="7e67b-191">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-192">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="7e67b-192">-WorkspaceResourceId</span></span>
<span data-ttu-id="7e67b-193">Идентификатор ресурса рабочей области для мониторинга надстройки.</span><span class="sxs-lookup"><span data-stu-id="7e67b-193">Resource Id of the workspace of Monitoring addon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e67b-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e67b-194">-Confirm</span></span>
<span data-ttu-id="7e67b-195">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e67b-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e67b-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e67b-196">-WhatIf</span></span>
<span data-ttu-id="7e67b-197">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e67b-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e67b-198">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e67b-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e67b-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e67b-199">CommonParameters</span></span>
<span data-ttu-id="7e67b-200">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e67b-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e67b-201">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e67b-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e67b-202">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e67b-202">INPUTS</span></span>

### <span data-ttu-id="7e67b-203">Ничего</span><span class="sxs-lookup"><span data-stu-id="7e67b-203">None</span></span>

## <span data-ttu-id="7e67b-204">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e67b-204">OUTPUTS</span></span>

### <span data-ttu-id="7e67b-205">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7e67b-205">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7e67b-206">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e67b-206">NOTES</span></span>

## <span data-ttu-id="7e67b-207">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e67b-207">RELATED LINKS</span></span>
