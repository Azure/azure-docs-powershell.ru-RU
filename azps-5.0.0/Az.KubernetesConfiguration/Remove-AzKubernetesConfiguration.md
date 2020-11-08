---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 2a9547b88129a199f97bbcff9281348f9d2c4659
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249034"
---
# <span data-ttu-id="a8fa9-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8fa9-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="a8fa9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fa9-103">Это приведет к удалению файла YAML, используемого для настройки конфигурации системы управления версиями, тем самым прекращая дальнейшую синхронизацию из исходного репозитория.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="a8fa9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8fa9-104">SYNTAX</span></span>

### <span data-ttu-id="a8fa9-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8fa9-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a8fa9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a8fa9-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8fa9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-107">DESCRIPTION</span></span>
<span data-ttu-id="a8fa9-108">Это приведет к удалению файла YAML, используемого для настройки конфигурации системы управления версиями, тем самым прекращая дальнейшую синхронизацию из исходного репозитория.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="a8fa9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-109">EXAMPLES</span></span>

### <span data-ttu-id="a8fa9-110">Пример 1: удаление configuation из kubernetes кластера по имени</span><span class="sxs-lookup"><span data-stu-id="a8fa9-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ClusterName connaks-d983yc -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test01

```

<span data-ttu-id="a8fa9-111">Эта команда удаляет configuation из kubernetes кластера по имени.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="a8fa9-112">Пример 2: удаление configuation из kubernetes кластера по объекту</span><span class="sxs-lookup"><span data-stu-id="a8fa9-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="a8fa9-113">Эта команда удаляет configuation из kubernetes кластера по объекту.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="a8fa9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-114">PARAMETERS</span></span>

### <span data-ttu-id="a8fa9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8fa9-115">-AsJob</span></span>
<span data-ttu-id="a8fa9-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a8fa9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a8fa9-117">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="a8fa9-117">-ClusterName</span></span>
<span data-ttu-id="a8fa9-118">Имя кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-118">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a8fa9-119">-ClusterType</span></span>
<span data-ttu-id="a8fa9-120">Имя ресурса кластера Kubernetes — либо managedClusters (для AKS кластеров), либо connectedClusters (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="a8fa9-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fa9-121">-DefaultProfile</span></span>
<span data-ttu-id="a8fa9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8fa9-123">-InputObject</span></span>
<span data-ttu-id="a8fa9-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8fa9-125">-Name</span></span>
<span data-ttu-id="a8fa9-126">Имя конфигурации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-126">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="a8fa9-127">-NoWait</span></span>
<span data-ttu-id="a8fa9-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a8fa9-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a8fa9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8fa9-129">-PassThru</span></span>
<span data-ttu-id="a8fa9-130">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a8fa9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fa9-131">-ResourceGroupName</span></span>
<span data-ttu-id="a8fa9-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8fa9-133">-SubscriptionId</span></span>
<span data-ttu-id="a8fa9-134">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-134">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fa9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8fa9-135">-Confirm</span></span>
<span data-ttu-id="a8fa9-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8fa9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8fa9-137">-WhatIf</span></span>
<span data-ttu-id="a8fa9-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8fa9-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8fa9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8fa9-140">CommonParameters</span></span>
<span data-ttu-id="a8fa9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8fa9-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8fa9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8fa9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8fa9-143">INPUTS</span></span>

### <span data-ttu-id="a8fa9-144">Microsoft. Azure. PowerShell. командлеты. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="a8fa9-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="a8fa9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-145">OUTPUTS</span></span>

### <span data-ttu-id="a8fa9-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8fa9-146">System.Boolean</span></span>

## <span data-ttu-id="a8fa9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8fa9-147">NOTES</span></span>

<span data-ttu-id="a8fa9-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-148">ALIASES</span></span>

<span data-ttu-id="a8fa9-149">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8fa9-150">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8fa9-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8fa9-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a8fa9-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8fa9-153">`[ClusterName <String>]`: Имя кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="a8fa9-154">`[ClusterResourceName <String>]`: Имя ресурса кластера Kubernetes — либо managedClusters (для AKS кластеров), либо connectedClusters (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="a8fa9-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="a8fa9-155">`[ClusterRp <String>]`: Кластер Kubernetes RP — либо Microsoft. ContainerService (для AKS кластеров), либо Microsoft. Kubernetes (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="a8fa9-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="a8fa9-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a8fa9-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8fa9-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a8fa9-158">`[SourceControlConfigurationName <String>]`: Имя конфигурации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="a8fa9-159">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a8fa9-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a8fa9-160">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="a8fa9-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a8fa9-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8fa9-161">RELATED LINKS</span></span>

