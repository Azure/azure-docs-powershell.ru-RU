---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: aaab86d7943072ae861acb71ec5021bb098a48ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247111"
---
# <span data-ttu-id="b8cee-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="b8cee-101">New-AzAksCluster</span></span>

## <span data-ttu-id="b8cee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8cee-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cee-103">Создание нового управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b8cee-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="b8cee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8cee-104">SYNTAX</span></span>

```
New-AzAksCluster [-Force] [-GenerateSshKey] [-NodeVmSetType <String>] [-NodeVnetSubnetID <String>]
 [-NodeMaxPodCount <Int32>] [-NodeSetPriority <String>] [-NodePoolMode <String>]
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

## <span data-ttu-id="b8cee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8cee-105">DESCRIPTION</span></span>

<span data-ttu-id="b8cee-106">Создайте новый кластер служб Azure Kubernetes (AKS).</span><span class="sxs-lookup"><span data-stu-id="b8cee-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="b8cee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8cee-107">EXAMPLES</span></span>

### <span data-ttu-id="b8cee-108">Новые параметры AKS с параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8cee-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="b8cee-109">Создайте контейнер Windows Server на AKS.</span><span class="sxs-lookup"><span data-stu-id="b8cee-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="b8cee-110">Чтобы создать контейнер Windows Server на AKS, при создании AKS необходимо указать по крайней мере четыре следующих параметра, а для параметра `NetworkPlugin` и `NodeVmSetType` должны быть `azure` и `VirtualMachineScaleSets` соответственно.</span><span class="sxs-lookup"><span data-stu-id="b8cee-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword **_ -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="b8cee-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8cee-111">PARAMETERS</span></span>

### <span data-ttu-id="b8cee-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="b8cee-112">-AcrNameToAttach</span></span>
<span data-ttu-id="b8cee-113">Предоставьте роль "acrpull" указанной записью контроля доступа AKS субъекта-службы, например myacr</span><span class="sxs-lookup"><span data-stu-id="b8cee-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="b8cee-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="b8cee-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="b8cee-115">Имена надстроек, которые будут включены при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="b8cee-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="b8cee-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8cee-116">-AsJob</span></span>
<span data-ttu-id="b8cee-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b8cee-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8cee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8cee-118">-DefaultProfile</span></span>
<span data-ttu-id="b8cee-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8cee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8cee-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="b8cee-120">-DnsNamePrefix</span></span>
<span data-ttu-id="b8cee-121">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="b8cee-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="b8cee-122">Длина должна быть <= 9, если пользователи планирует добавить контейнер Windows.</span><span class="sxs-lookup"><span data-stu-id="b8cee-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="b8cee-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="b8cee-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="b8cee-124">Следует ли включить автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="b8cee-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="b8cee-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="b8cee-125">-EnableRbac</span></span>
<span data-ttu-id="b8cee-126">Следует ли включить доступ Kubernetes Role-Based</span><span class="sxs-lookup"><span data-stu-id="b8cee-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="b8cee-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b8cee-127">-Force</span></span>
<span data-ttu-id="b8cee-128">Создать кластер, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="b8cee-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="b8cee-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="b8cee-129">-GenerateSshKey</span></span>
<span data-ttu-id="b8cee-130">Создание файла ключа SSH для {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="b8cee-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="b8cee-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="b8cee-131">-KubernetesVersion</span></span>
<span data-ttu-id="b8cee-132">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="b8cee-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="b8cee-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="b8cee-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="b8cee-134">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="b8cee-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="b8cee-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="b8cee-135">-LoadBalancerSku</span></span>
<span data-ttu-id="b8cee-136">SKU подсистемы балансировки нагрузки для управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="b8cee-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="b8cee-137">-Location</span><span class="sxs-lookup"><span data-stu-id="b8cee-137">-Location</span></span>
<span data-ttu-id="b8cee-138">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="b8cee-138">Azure location for the cluster.</span></span>
<span data-ttu-id="b8cee-139">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="b8cee-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8cee-140">-Name</span></span>
<span data-ttu-id="b8cee-141">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b8cee-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="b8cee-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="b8cee-142">-NetworkPlugin</span></span>
<span data-ttu-id="b8cee-143">Сетевой подключаемый модуль, используемый для создания сети Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="b8cee-143">Network plugin used for building Kubernetes network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: azure
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8cee-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b8cee-144">-NodeCount</span></span>
<span data-ttu-id="b8cee-145">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="b8cee-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="b8cee-146">-NodeMaxCount</span></span>
<span data-ttu-id="b8cee-147">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="b8cee-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="b8cee-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="b8cee-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="b8cee-149">Максимальное количество обыкновенных модулей, которые могут работать на узле.</span><span class="sxs-lookup"><span data-stu-id="b8cee-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="b8cee-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="b8cee-150">-NodeMinCount</span></span>
<span data-ttu-id="b8cee-151">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b8cee-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="b8cee-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="b8cee-152">-NodeName</span></span>
<span data-ttu-id="b8cee-153">Уникальное имя профиля пула агентов в контексте подписок и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="b8cee-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="b8cee-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="b8cee-155">Размер диска операционной системы (ГБ) для каждого узла в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="b8cee-156">Минимум 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="b8cee-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="b8cee-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="b8cee-157">-NodePoolMode</span></span>
<span data-ttu-id="b8cee-158">NodePoolMode представляет режим пула узлов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="b8cee-159">-NodeScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="b8cee-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="b8cee-160">ScaleSetEvictionPolicy, который будет использоваться для указания политики вытесненности для установленного уровня с низким приоритетом виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b8cee-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="b8cee-161">По умолчанию удалить.</span><span class="sxs-lookup"><span data-stu-id="b8cee-161">Default to Delete.</span></span>

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

### <span data-ttu-id="b8cee-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="b8cee-162">-NodeSetPriority</span></span>
<span data-ttu-id="b8cee-163">ScaleSetPriority, который будет использоваться для задания приоритета для установки масштаба виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="b8cee-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="b8cee-164">По умолчанию используется обычный.</span><span class="sxs-lookup"><span data-stu-id="b8cee-164">Default to regular.</span></span>

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

### <span data-ttu-id="b8cee-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="b8cee-165">-NodeVmSetType</span></span>
<span data-ttu-id="b8cee-166">AgentPoolType представляет типы пула агентов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="b8cee-167">Возможные значения: "VirtualMachineScaleSets", "Группа доступности"</span><span class="sxs-lookup"><span data-stu-id="b8cee-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: VirtualMachineScaleSets
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8cee-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="b8cee-168">-NodeVmSize</span></span>
<span data-ttu-id="b8cee-169">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b8cee-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="b8cee-170">Значение по умолчанию — Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="b8cee-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="b8cee-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="b8cee-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="b8cee-172">VNet SubnetID указывает идентификатор подсети VNet.</span><span class="sxs-lookup"><span data-stu-id="b8cee-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="b8cee-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8cee-173">-ResourceGroupName</span></span>
<span data-ttu-id="b8cee-174">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8cee-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="b8cee-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="b8cee-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="b8cee-176">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="b8cee-176">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8cee-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="b8cee-177">-SshKeyValue</span></span>
<span data-ttu-id="b8cee-178">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="b8cee-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="b8cee-179">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="b8cee-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="b8cee-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b8cee-180">-SubnetName</span></span>
<span data-ttu-id="b8cee-181">Имя подсети надстройки VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="b8cee-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="b8cee-182">-Тег</span><span class="sxs-lookup"><span data-stu-id="b8cee-182">-Tag</span></span>
<span data-ttu-id="b8cee-183">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="b8cee-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="b8cee-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="b8cee-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="b8cee-185">Имя пользователя администратора, используемое для виртуальных машин Windows.</span><span class="sxs-lookup"><span data-stu-id="b8cee-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="b8cee-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="b8cee-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="b8cee-187">Пароль администратора для Windows VM, его длина должна быть не менее 12, в которой есть хотя бы один знак нижнего регистра, например `[a-z]` один `[A-Z]` и один специальный символ `[!@#$%^&_()]` .</span><span class="sxs-lookup"><span data-stu-id="b8cee-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&_()]`.</span></span>

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

### <span data-ttu-id="b8cee-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b8cee-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="b8cee-189">Идентификатор ресурса рабочей области для мониторинга надстройки.</span><span class="sxs-lookup"><span data-stu-id="b8cee-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="b8cee-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8cee-190">-Confirm</span></span>
<span data-ttu-id="b8cee-191">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8cee-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8cee-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8cee-192">-WhatIf</span></span>
<span data-ttu-id="b8cee-193">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8cee-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8cee-194">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8cee-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8cee-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cee-195">CommonParameters</span></span>
<span data-ttu-id="b8cee-196">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8cee-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cee-197">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8cee-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cee-198">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8cee-198">INPUTS</span></span>

### <span data-ttu-id="b8cee-199">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8cee-199">None</span></span>

## <span data-ttu-id="b8cee-200">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8cee-200">OUTPUTS</span></span>

### <span data-ttu-id="b8cee-201">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b8cee-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b8cee-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8cee-202">NOTES</span></span>

## <span data-ttu-id="b8cee-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8cee-203">RELATED LINKS</span></span>
