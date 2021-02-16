---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: 16b1e6f56cd5d324815dcf9453bc7f94e0de2480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219393"
---
# <span data-ttu-id="8c1c9-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c1c9-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="8c1c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1c9-103">При этом будет удален файл YAML, используемый для настройки конфигурации управления источником, что останавливает его последующие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="8c1c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c1c9-104">SYNTAX</span></span>

### <span data-ttu-id="8c1c9-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c1c9-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c1c9-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c1c9-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c1c9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c1c9-107">DESCRIPTION</span></span>
<span data-ttu-id="8c1c9-108">При этом будет удален файл YAML, используемый для настройки конфигурации управления источником, поэтому в будущем синхронизация будет удалена из повторной настройки источника.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="8c1c9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c1c9-109">EXAMPLES</span></span>

### <span data-ttu-id="8c1c9-110">Пример 1. Удаление кластера куберсетей по имени</span><span class="sxs-lookup"><span data-stu-id="8c1c9-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="8c1c9-111">Эта команда удаляет по имени кластер кюберсетей.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="8c1c9-112">Пример 2. Удаление кластера куберсетей по объектам</span><span class="sxs-lookup"><span data-stu-id="8c1c9-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="8c1c9-113">Эта команда удаляет кластер куберсетей по объектам.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="8c1c9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c1c9-114">PARAMETERS</span></span>

### <span data-ttu-id="8c1c9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c1c9-115">-AsJob</span></span>
<span data-ttu-id="8c1c9-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8c1c9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8c1c9-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8c1c9-117">-ClusterName</span></span>
<span data-ttu-id="8c1c9-118">Название кластера "Кубберсети".</span><span class="sxs-lookup"><span data-stu-id="8c1c9-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="8c1c9-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="8c1c9-119">-ClusterType</span></span>
<span data-ttu-id="8c1c9-120">Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="8c1c9-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="8c1c9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1c9-121">-DefaultProfile</span></span>
<span data-ttu-id="8c1c9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c1c9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c1c9-123">-InputObject</span></span>
<span data-ttu-id="8c1c9-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8c1c9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8c1c9-125">-Name</span></span>
<span data-ttu-id="8c1c9-126">Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="8c1c9-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8c1c9-127">-NoWait</span></span>
<span data-ttu-id="8c1c9-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="8c1c9-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c1c9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c1c9-129">-PassThru</span></span>
<span data-ttu-id="8c1c9-130">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8c1c9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c1c9-131">-ResourceGroupName</span></span>
<span data-ttu-id="8c1c9-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c1c9-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c1c9-133">-SubscriptionId</span></span>
<span data-ttu-id="8c1c9-134">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="8c1c9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c1c9-135">-Confirm</span></span>
<span data-ttu-id="8c1c9-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c1c9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c1c9-137">-WhatIf</span></span>
<span data-ttu-id="8c1c9-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c1c9-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c1c9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1c9-140">CommonParameters</span></span>
<span data-ttu-id="8c1c9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1c9-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c1c9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1c9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c1c9-143">INPUTS</span></span>

### <span data-ttu-id="8c1c9-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="8c1c9-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="8c1c9-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c1c9-145">OUTPUTS</span></span>

### <span data-ttu-id="8c1c9-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c1c9-146">System.Boolean</span></span>

## <span data-ttu-id="8c1c9-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c1c9-147">NOTES</span></span>

<span data-ttu-id="8c1c9-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8c1c9-148">ALIASES</span></span>

<span data-ttu-id="8c1c9-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8c1c9-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c1c9-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c1c9-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c1c9-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8c1c9-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c1c9-153">`[ClusterName <String>]`Название кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="8c1c9-154">`[ClusterResourceName <String>]`Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="8c1c9-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="8c1c9-155">`[ClusterRp <String>]`: RP кластера "Кубберсети" — Microsoft.ContainerService (для кластеров AKS) или Microsoft.Kubernetes (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="8c1c9-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="8c1c9-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8c1c9-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c1c9-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8c1c9-158">`[SourceControlConfigurationName <String>]`: Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="8c1c9-159">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="8c1c9-160">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="8c1c9-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="8c1c9-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c1c9-161">RELATED LINKS</span></span>

