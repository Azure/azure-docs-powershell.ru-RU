---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksCluster.md
ms.openlocfilehash: c0eeaedfc98f8225b097345908638d52bb4ed297
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233916"
---
# <span data-ttu-id="67ebf-101">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="67ebf-101">New-AzAksCluster</span></span>

## <span data-ttu-id="67ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="67ebf-103">Создайте новый управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="67ebf-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="67ebf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67ebf-104">SYNTAX</span></span>

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

## <span data-ttu-id="67ebf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ebf-105">DESCRIPTION</span></span>

<span data-ttu-id="67ebf-106">Создайте кластер Службы Azure Kubernetes(AKS).</span><span class="sxs-lookup"><span data-stu-id="67ebf-106">Create a new Azure Kubernetes Service(AKS) cluster.</span></span>

## <span data-ttu-id="67ebf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="67ebf-108">Новый параметр AKS с параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="67ebf-108">New an AKS with default params.</span></span>

```powershell
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster
```

### <span data-ttu-id="67ebf-109">Создайте контейнер Windows Server на akS.</span><span class="sxs-lookup"><span data-stu-id="67ebf-109">Create Windows Server container on an AKS.</span></span>
<span data-ttu-id="67ebf-110">Чтобы создать контейнер Windows Server на основе AKS, при его создании необходимо указать как минимум четыре следующих параметра: значение и значение (и должно `NetworkPlugin` `NodeVmSetType` `azure` быть) `VirtualMachineScaleSets` и соответственно.</span><span class="sxs-lookup"><span data-stu-id="67ebf-110">To create Windows Server container on an AKS, you must specify at least four following parameters when creating the AKS, and the value for `NetworkPlugin` and `NodeVmSetType` must be `azure` and `VirtualMachineScaleSets` respectively.</span></span>
`-WindowsProfileAdminUserName *** -WindowsProfileAdminUserPassword *** -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets`

```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="67ebf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ebf-111">PARAMETERS</span></span>

### <span data-ttu-id="67ebf-112">-AcrNameToAttach</span><span class="sxs-lookup"><span data-stu-id="67ebf-112">-AcrNameToAttach</span></span>
<span data-ttu-id="67ebf-113">Придание роли "acrpull" указанного ACR основному службе AKS, например myacr</span><span class="sxs-lookup"><span data-stu-id="67ebf-113">Grant the 'acrpull' role of the specified ACR to AKS Service Principal, e.g. myacr</span></span>

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

### <span data-ttu-id="67ebf-114">-AddOnNameToBeEnabled</span><span class="sxs-lookup"><span data-stu-id="67ebf-114">-AddOnNameToBeEnabled</span></span>
<span data-ttu-id="67ebf-115">Имена надстройок, которые должны быть включены при создания кластера.</span><span class="sxs-lookup"><span data-stu-id="67ebf-115">Add-on names to be enabled when cluster is created.</span></span>

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

### <span data-ttu-id="67ebf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67ebf-116">-AsJob</span></span>
<span data-ttu-id="67ebf-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67ebf-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67ebf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ebf-118">-DefaultProfile</span></span>
<span data-ttu-id="67ebf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67ebf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ebf-120">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="67ebf-120">-DnsNamePrefix</span></span>
<span data-ttu-id="67ebf-121">Префикс имени DNS для кластера.</span><span class="sxs-lookup"><span data-stu-id="67ebf-121">The DNS name prefix for the cluster.</span></span> <span data-ttu-id="67ebf-122">Длина должна быть <= 9, если пользователи планируют добавить контейнер Windows.</span><span class="sxs-lookup"><span data-stu-id="67ebf-122">The length must be <= 9 if users plan to add windows container.</span></span>

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

### <span data-ttu-id="67ebf-123">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="67ebf-123">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="67ebf-124">Следует ли включить авторе шкалу</span><span class="sxs-lookup"><span data-stu-id="67ebf-124">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="67ebf-125">-EnableRbac</span><span class="sxs-lookup"><span data-stu-id="67ebf-125">-EnableRbac</span></span>
<span data-ttu-id="67ebf-126">Следует ли включить веб-Role-Based Access</span><span class="sxs-lookup"><span data-stu-id="67ebf-126">Whether to enable Kubernetes Role-Based Access</span></span>

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

### <span data-ttu-id="67ebf-127">-Force</span><span class="sxs-lookup"><span data-stu-id="67ebf-127">-Force</span></span>
<span data-ttu-id="67ebf-128">Создание кластера, даже если он уже существует</span><span class="sxs-lookup"><span data-stu-id="67ebf-128">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="67ebf-129">-GenerateSshKey</span><span class="sxs-lookup"><span data-stu-id="67ebf-129">-GenerateSshKey</span></span>
<span data-ttu-id="67ebf-130">Создание SSH-файла в {HOME}/.ssh/id_rsa.</span><span class="sxs-lookup"><span data-stu-id="67ebf-130">Generate ssh key file to {HOME}/.ssh/id_rsa.</span></span>

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

### <span data-ttu-id="67ebf-131">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="67ebf-131">-KubernetesVersion</span></span>
<span data-ttu-id="67ebf-132">Версия Кубберсетей, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="67ebf-132">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="67ebf-133">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="67ebf-133">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="67ebf-134">Имя пользователя виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="67ebf-134">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="67ebf-135">-LoadBalancerSku</span><span class="sxs-lookup"><span data-stu-id="67ebf-135">-LoadBalancerSku</span></span>
<span data-ttu-id="67ebf-136">SKU балансиров нагрузки для управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="67ebf-136">The load balancer sku for the managed cluster.</span></span>

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

### <span data-ttu-id="67ebf-137">-Location</span><span class="sxs-lookup"><span data-stu-id="67ebf-137">-Location</span></span>
<span data-ttu-id="67ebf-138">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="67ebf-138">Azure location for the cluster.</span></span>
<span data-ttu-id="67ebf-139">По умолчанию для расположения группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-139">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="67ebf-140">-Name</span><span class="sxs-lookup"><span data-stu-id="67ebf-140">-Name</span></span>
<span data-ttu-id="67ebf-141">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="67ebf-141">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="67ebf-142">-NetworkPlugin</span><span class="sxs-lookup"><span data-stu-id="67ebf-142">-NetworkPlugin</span></span>
<span data-ttu-id="67ebf-143">Сетевой подключаемый модуль, используемый для построения сети Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="67ebf-143">Network plugin used for building Kubernetes network.</span></span>

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

### <span data-ttu-id="67ebf-144">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="67ebf-144">-NodeCount</span></span>
<span data-ttu-id="67ebf-145">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-145">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="67ebf-146">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="67ebf-146">-NodeMaxCount</span></span>
<span data-ttu-id="67ebf-147">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="67ebf-147">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="67ebf-148">-NodeMaxPodCount</span><span class="sxs-lookup"><span data-stu-id="67ebf-148">-NodeMaxPodCount</span></span>
<span data-ttu-id="67ebf-149">Максимальное количество pods, которые могут запускаться в узле.</span><span class="sxs-lookup"><span data-stu-id="67ebf-149">Maximum number of pods that can run on node.</span></span>

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

### <span data-ttu-id="67ebf-150">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="67ebf-150">-NodeMinCount</span></span>
<span data-ttu-id="67ebf-151">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="67ebf-151">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="67ebf-152">-NodeName</span><span class="sxs-lookup"><span data-stu-id="67ebf-152">-NodeName</span></span>
<span data-ttu-id="67ebf-153">Уникальное имя профиля пула агентов в контексте подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-153">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="67ebf-154">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="67ebf-154">-NodeOsDiskSize</span></span>
<span data-ttu-id="67ebf-155">Размер в ГБ диска ОС для каждого узла в пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-155">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="67ebf-156">Минимум 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="67ebf-156">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="67ebf-157">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="67ebf-157">-NodePoolMode</span></span>
<span data-ttu-id="67ebf-158">NodePoolMode представляет режим пула узлов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-158">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="67ebf-159">-NodeScaleSetevictionPolicy</span><span class="sxs-lookup"><span data-stu-id="67ebf-159">-NodeScaleSetEvictionPolicy</span></span>
<span data-ttu-id="67ebf-160">ScaleSetEvictionPolicy, которая используется для указания политики разборки для набора виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="67ebf-160">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span> <span data-ttu-id="67ebf-161">Значение по умолчанию для удаления.</span><span class="sxs-lookup"><span data-stu-id="67ebf-161">Default to Delete.</span></span>

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

### <span data-ttu-id="67ebf-162">-NodeSetPriority</span><span class="sxs-lookup"><span data-stu-id="67ebf-162">-NodeSetPriority</span></span>
<span data-ttu-id="67ebf-163">ScaleSetPriority, используемое для указания приоритета набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67ebf-163">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span> <span data-ttu-id="67ebf-164">Значение по умолчанию ( обычный).</span><span class="sxs-lookup"><span data-stu-id="67ebf-164">Default to regular.</span></span>

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

### <span data-ttu-id="67ebf-165">-NodeVmSetType</span><span class="sxs-lookup"><span data-stu-id="67ebf-165">-NodeVmSetType</span></span>
<span data-ttu-id="67ebf-166">AgentPoolType представляет типы пула агентов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-166">AgentPoolType represents types of an agent pool.</span></span> <span data-ttu-id="67ebf-167">Возможные значения: 'VirtualMascaleeScaleSets', 'AvailabilitySet'</span><span class="sxs-lookup"><span data-stu-id="67ebf-167">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="67ebf-168">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="67ebf-168">-NodeVmSize</span></span>
<span data-ttu-id="67ebf-169">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67ebf-169">The size of the Virtual Machine.</span></span> <span data-ttu-id="67ebf-170">Значение по умолчанию — Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="67ebf-170">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="67ebf-171">-NodeVnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="67ebf-171">-NodeVnetSubnetID</span></span>
<span data-ttu-id="67ebf-172">Код подсети VNet указывает идентификатор подсети VNet.</span><span class="sxs-lookup"><span data-stu-id="67ebf-172">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="67ebf-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ebf-173">-ResourceGroupName</span></span>
<span data-ttu-id="67ebf-174">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67ebf-174">Resource Group Name.</span></span>

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

### <span data-ttu-id="67ebf-175">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="67ebf-175">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="67ebf-176">ИД клиента и секрет клиента, связанные с приложением AAD или главой службы.</span><span class="sxs-lookup"><span data-stu-id="67ebf-176">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="67ebf-177">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="67ebf-177">-SshKeyValue</span></span>
<span data-ttu-id="67ebf-178">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="67ebf-178">SSH key file value or key file path.</span></span>
<span data-ttu-id="67ebf-179">По умолчанию для {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="67ebf-179">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="67ebf-180">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="67ebf-180">-SubnetName</span></span>
<span data-ttu-id="67ebf-181">Имя подсети надстройки VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="67ebf-181">Subnet name of VirtualNode addon.</span></span>

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

### <span data-ttu-id="67ebf-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="67ebf-182">-Tag</span></span>
<span data-ttu-id="67ebf-183">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="67ebf-183">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="67ebf-184">-WindowsProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="67ebf-184">-WindowsProfileAdminUserName</span></span>
<span data-ttu-id="67ebf-185">Имя пользователя администратора, который будет использовать для VMs Windows.</span><span class="sxs-lookup"><span data-stu-id="67ebf-185">The administrator username to use for Windows VMs.</span></span>

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

### <span data-ttu-id="67ebf-186">-WindowsProfileAdminUserPassword</span><span class="sxs-lookup"><span data-stu-id="67ebf-186">-WindowsProfileAdminUserPassword</span></span>
<span data-ttu-id="67ebf-187">Пароль администратора для VMs Windows должен иметь длину не менее 12 символов, содержащих по крайней мере один символ нижнего уровня, то есть один и один `[a-z]` `[A-Z]` специальный `[!@#$%^&*()]` знак.</span><span class="sxs-lookup"><span data-stu-id="67ebf-187">The administrator password to use for Windows VMs, its length must be at least 12, containing at least one lower case character, i.e. `[a-z]`, one `[A-Z]` and one special character `[!@#$%^&*()]`.</span></span>

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

### <span data-ttu-id="67ebf-188">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="67ebf-188">-WorkspaceResourceId</span></span>
<span data-ttu-id="67ebf-189">ИД ресурса в рабочей области надстройки "Мониторинг".</span><span class="sxs-lookup"><span data-stu-id="67ebf-189">Resource Id of the workspace of Monitoring addon.</span></span>

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

### <span data-ttu-id="67ebf-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67ebf-190">-Confirm</span></span>
<span data-ttu-id="67ebf-191">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="67ebf-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ebf-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ebf-192">-WhatIf</span></span>
<span data-ttu-id="67ebf-193">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ebf-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ebf-194">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67ebf-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ebf-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ebf-195">CommonParameters</span></span>
<span data-ttu-id="67ebf-196">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ebf-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ebf-197">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67ebf-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ebf-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67ebf-198">INPUTS</span></span>

### <span data-ttu-id="67ebf-199">Нет</span><span class="sxs-lookup"><span data-stu-id="67ebf-199">None</span></span>

## <span data-ttu-id="67ebf-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67ebf-200">OUTPUTS</span></span>

### <span data-ttu-id="67ebf-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="67ebf-201">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="67ebf-202">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67ebf-202">NOTES</span></span>

## <span data-ttu-id="67ebf-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67ebf-203">RELATED LINKS</span></span>
