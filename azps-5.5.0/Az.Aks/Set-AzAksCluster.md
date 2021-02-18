---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239981"
---
# <span data-ttu-id="90242-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="90242-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="90242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90242-102">SYNOPSIS</span></span>
<span data-ttu-id="90242-103">Обновим или создайте управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="90242-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="90242-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90242-104">SYNTAX</span></span>

### <span data-ttu-id="90242-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90242-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90242-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90242-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90242-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90242-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90242-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90242-108">DESCRIPTION</span></span>
<span data-ttu-id="90242-109">Обновим или создайте управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="90242-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="90242-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90242-110">EXAMPLES</span></span>

### <span data-ttu-id="90242-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90242-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="90242-112">Установите число узлов в кластере "Кубберсети" на 5.</span><span class="sxs-lookup"><span data-stu-id="90242-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="90242-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90242-113">PARAMETERS</span></span>

### <span data-ttu-id="90242-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90242-114">-AsJob</span></span>
<span data-ttu-id="90242-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="90242-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90242-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90242-116">-DefaultProfile</span></span>
<span data-ttu-id="90242-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90242-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90242-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="90242-118">-DnsNamePrefix</span></span>
<span data-ttu-id="90242-119">Префикс имени DNS для кластера.</span><span class="sxs-lookup"><span data-stu-id="90242-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="90242-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="90242-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="90242-121">Следует ли включить авто scaler</span><span class="sxs-lookup"><span data-stu-id="90242-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="90242-122">-Id</span><span class="sxs-lookup"><span data-stu-id="90242-122">-Id</span></span>
<span data-ttu-id="90242-123">ИД кластера управляемых кубарныхсетей</span><span class="sxs-lookup"><span data-stu-id="90242-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="90242-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90242-124">-InputObject</span></span>
<span data-ttu-id="90242-125">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="90242-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="90242-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="90242-126">-KubernetesVersion</span></span>
<span data-ttu-id="90242-127">Версия Кубберсетей, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="90242-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="90242-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="90242-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="90242-129">Имя пользователя виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="90242-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="90242-130">-Location</span><span class="sxs-lookup"><span data-stu-id="90242-130">-Location</span></span>
<span data-ttu-id="90242-131">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="90242-131">Azure location for the cluster.</span></span>
<span data-ttu-id="90242-132">По умолчанию для расположения группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90242-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="90242-133">-Name</span><span class="sxs-lookup"><span data-stu-id="90242-133">-Name</span></span>
<span data-ttu-id="90242-134">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="90242-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="90242-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="90242-135">-NodeCount</span></span>
<span data-ttu-id="90242-136">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="90242-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="90242-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="90242-137">-NodeMaxCount</span></span>
<span data-ttu-id="90242-138">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="90242-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="90242-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="90242-139">-NodeMinCount</span></span>
<span data-ttu-id="90242-140">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="90242-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="90242-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="90242-141">-NodeName</span></span>
<span data-ttu-id="90242-142">Уникальное имя профиля пула агентов в контексте подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90242-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="90242-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="90242-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="90242-144">Число узлов по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="90242-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="90242-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="90242-145">-NodePoolMode</span></span>
<span data-ttu-id="90242-146">NodePoolMode представляет режим пула узлов.</span><span class="sxs-lookup"><span data-stu-id="90242-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="90242-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="90242-147">-NodeVmSize</span></span>
<span data-ttu-id="90242-148">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="90242-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="90242-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90242-149">-ResourceGroupName</span></span>
<span data-ttu-id="90242-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90242-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="90242-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="90242-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="90242-152">ИД клиента и секрет клиента, связанные с приложением AAD или главой службы.</span><span class="sxs-lookup"><span data-stu-id="90242-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="90242-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="90242-153">-SshKeyValue</span></span>
<span data-ttu-id="90242-154">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="90242-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="90242-155">По умолчанию для {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="90242-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="90242-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="90242-156">-Tag</span></span>
<span data-ttu-id="90242-157">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="90242-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="90242-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90242-158">-Confirm</span></span>
<span data-ttu-id="90242-159">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90242-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90242-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90242-160">-WhatIf</span></span>
<span data-ttu-id="90242-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90242-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90242-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90242-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90242-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90242-163">CommonParameters</span></span>
<span data-ttu-id="90242-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90242-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90242-165">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90242-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90242-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90242-166">INPUTS</span></span>

### <span data-ttu-id="90242-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="90242-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="90242-168">System.String</span><span class="sxs-lookup"><span data-stu-id="90242-168">System.String</span></span>

## <span data-ttu-id="90242-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90242-169">OUTPUTS</span></span>

### <span data-ttu-id="90242-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="90242-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="90242-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90242-171">NOTES</span></span>

## <span data-ttu-id="90242-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90242-172">RELATED LINKS</span></span>
