---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247103"
---
# <span data-ttu-id="e194f-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="e194f-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="e194f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e194f-102">SYNOPSIS</span></span>
<span data-ttu-id="e194f-103">Обновите или создайте управляемый кластер Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e194f-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e194f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e194f-104">SYNTAX</span></span>

### <span data-ttu-id="e194f-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e194f-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e194f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e194f-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e194f-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e194f-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e194f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e194f-108">DESCRIPTION</span></span>
<span data-ttu-id="e194f-109">Обновите или создайте управляемый кластер Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e194f-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e194f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e194f-110">EXAMPLES</span></span>

### <span data-ttu-id="e194f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e194f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="e194f-112">Установите количество узлов в кластере Kubernetes равным 5.</span><span class="sxs-lookup"><span data-stu-id="e194f-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="e194f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e194f-113">PARAMETERS</span></span>

### <span data-ttu-id="e194f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e194f-114">-AsJob</span></span>
<span data-ttu-id="e194f-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e194f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e194f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e194f-116">-DefaultProfile</span></span>
<span data-ttu-id="e194f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e194f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e194f-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e194f-118">-DnsNamePrefix</span></span>
<span data-ttu-id="e194f-119">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="e194f-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="e194f-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="e194f-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="e194f-121">Следует ли включить автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="e194f-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="e194f-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e194f-122">-Id</span></span>
<span data-ttu-id="e194f-123">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e194f-123">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e194f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e194f-124">-InputObject</span></span>
<span data-ttu-id="e194f-125">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e194f-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e194f-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e194f-126">-KubernetesVersion</span></span>
<span data-ttu-id="e194f-127">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="e194f-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="e194f-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="e194f-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="e194f-129">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="e194f-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="e194f-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e194f-130">-Location</span></span>
<span data-ttu-id="e194f-131">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="e194f-131">Azure location for the cluster.</span></span>
<span data-ttu-id="e194f-132">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e194f-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="e194f-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e194f-133">-Name</span></span>
<span data-ttu-id="e194f-134">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e194f-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e194f-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e194f-135">-NodeCount</span></span>
<span data-ttu-id="e194f-136">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="e194f-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="e194f-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="e194f-137">-NodeMaxCount</span></span>
<span data-ttu-id="e194f-138">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="e194f-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="e194f-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="e194f-139">-NodeMinCount</span></span>
<span data-ttu-id="e194f-140">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e194f-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="e194f-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="e194f-141">-NodeName</span></span>
<span data-ttu-id="e194f-142">Уникальное имя профиля пула агентов в контексте подписок и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e194f-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="e194f-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e194f-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="e194f-144">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="e194f-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="e194f-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="e194f-145">-NodePoolMode</span></span>
<span data-ttu-id="e194f-146">NodePoolMode представляет режим пула узлов.</span><span class="sxs-lookup"><span data-stu-id="e194f-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="e194f-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="e194f-147">-NodeVmSize</span></span>
<span data-ttu-id="e194f-148">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e194f-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="e194f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e194f-149">-ResourceGroupName</span></span>
<span data-ttu-id="e194f-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e194f-150">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e194f-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="e194f-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="e194f-152">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="e194f-152">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e194f-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e194f-153">-SshKeyValue</span></span>
<span data-ttu-id="e194f-154">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="e194f-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="e194f-155">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="e194f-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="e194f-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="e194f-156">-Tag</span></span>
<span data-ttu-id="e194f-157">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="e194f-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="e194f-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e194f-158">-Confirm</span></span>
<span data-ttu-id="e194f-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e194f-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e194f-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e194f-160">-WhatIf</span></span>
<span data-ttu-id="e194f-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e194f-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e194f-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e194f-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e194f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e194f-163">CommonParameters</span></span>
<span data-ttu-id="e194f-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e194f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e194f-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e194f-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e194f-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e194f-166">INPUTS</span></span>

### <span data-ttu-id="e194f-167">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e194f-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="e194f-168">System. String</span><span class="sxs-lookup"><span data-stu-id="e194f-168">System.String</span></span>

## <span data-ttu-id="e194f-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e194f-169">OUTPUTS</span></span>

### <span data-ttu-id="e194f-170">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e194f-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e194f-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="e194f-171">NOTES</span></span>

## <span data-ttu-id="e194f-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e194f-172">RELATED LINKS</span></span>
