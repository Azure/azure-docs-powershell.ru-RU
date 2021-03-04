---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/powershell/module/az.kubernetesconfiguration/remove-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Remove-AzKubernetesConfiguration.md
ms.openlocfilehash: a63a28d301b5b565a01bf1e3c22acba413ee779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964600"
---
# <span data-ttu-id="19b2b-101">Remove-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="19b2b-101">Remove-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="19b2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="19b2b-103">При этом будет удален файл YAML, используемый для настройки конфигурации управления источником, что останавливает его последующие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="19b2b-103">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="19b2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19b2b-104">SYNTAX</span></span>

### <span data-ttu-id="19b2b-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19b2b-105">Delete (Default)</span></span>
```
Remove-AzKubernetesConfiguration -ClusterName <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="19b2b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19b2b-106">DeleteViaIdentity</span></span>
```
Remove-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="19b2b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19b2b-107">DESCRIPTION</span></span>
<span data-ttu-id="19b2b-108">При этом будет удален файл YAML, используемый для настройки конфигурации управления источником, что останавливает его последующие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="19b2b-108">This will delete the YAML file used to set up the Source control configuration, thus stopping future sync from the source repo.</span></span>

## <span data-ttu-id="19b2b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19b2b-109">EXAMPLES</span></span>

### <span data-ttu-id="19b2b-110">Пример 1. Удаление кластера куберсетей по имени</span><span class="sxs-lookup"><span data-stu-id="19b2b-110">Example 1: Remove a configuation of kubernetes cluster by name</span></span>
```powershell
PS C:\> Remove-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name  k8sconfig-t02 -ClusterType ConnectedClusters

```

<span data-ttu-id="19b2b-111">Эта команда удаляет кластер куберсетей по имени.</span><span class="sxs-lookup"><span data-stu-id="19b2b-111">This command removes a configuation of kubernetes cluster by name.</span></span>

### <span data-ttu-id="19b2b-112">Пример 2. Удаление кластера куберсетей по объектам</span><span class="sxs-lookup"><span data-stu-id="19b2b-112">Example 2: Remove a configuation of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = Get-AzKubernetesConfiguration -ClusterName connaks-dkc29c -ClusterType ConnectedClusters -ResourceGroupName connaks-rg-w9vlnp -Name conf-test02 -ClusterRp Microsoft.Kubernetes
PS C:\> Remove-AzKubernetesConfiguration -InputObject $kubConf

```

<span data-ttu-id="19b2b-113">Эта команда удаляет кластер куберсетей по объектам.</span><span class="sxs-lookup"><span data-stu-id="19b2b-113">This command removes a configuation of kubernetes cluster by object.</span></span>

## <span data-ttu-id="19b2b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19b2b-114">PARAMETERS</span></span>

### <span data-ttu-id="19b2b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19b2b-115">-AsJob</span></span>
<span data-ttu-id="19b2b-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="19b2b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="19b2b-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="19b2b-117">-ClusterName</span></span>
<span data-ttu-id="19b2b-118">Название кластера "Кубберсети".</span><span class="sxs-lookup"><span data-stu-id="19b2b-118">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="19b2b-119">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="19b2b-119">-ClusterType</span></span>
<span data-ttu-id="19b2b-120">Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="19b2b-120">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="19b2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b2b-121">-DefaultProfile</span></span>
<span data-ttu-id="19b2b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19b2b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b2b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19b2b-123">-InputObject</span></span>
<span data-ttu-id="19b2b-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="19b2b-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19b2b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="19b2b-125">-Name</span></span>
<span data-ttu-id="19b2b-126">Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="19b2b-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="19b2b-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="19b2b-127">-NoWait</span></span>
<span data-ttu-id="19b2b-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="19b2b-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="19b2b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19b2b-129">-PassThru</span></span>
<span data-ttu-id="19b2b-130">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="19b2b-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19b2b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b2b-131">-ResourceGroupName</span></span>
<span data-ttu-id="19b2b-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19b2b-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="19b2b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19b2b-133">-SubscriptionId</span></span>
<span data-ttu-id="19b2b-134">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="19b2b-134">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="19b2b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19b2b-135">-Confirm</span></span>
<span data-ttu-id="19b2b-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="19b2b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b2b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b2b-137">-WhatIf</span></span>
<span data-ttu-id="19b2b-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19b2b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19b2b-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19b2b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b2b-140">CommonParameters</span></span>
<span data-ttu-id="19b2b-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b2b-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19b2b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b2b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19b2b-143">INPUTS</span></span>

### <span data-ttu-id="19b2b-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="19b2b-144">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="19b2b-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19b2b-145">OUTPUTS</span></span>

### <span data-ttu-id="19b2b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19b2b-146">System.Boolean</span></span>

## <span data-ttu-id="19b2b-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19b2b-147">NOTES</span></span>

<span data-ttu-id="19b2b-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="19b2b-148">ALIASES</span></span>

<span data-ttu-id="19b2b-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="19b2b-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19b2b-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="19b2b-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19b2b-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19b2b-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19b2b-152">INPUTOBJECT <IKubernetesConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="19b2b-152">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19b2b-153">`[ClusterName <String>]`Название кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="19b2b-153">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="19b2b-154">`[ClusterResourceName <String>]`Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="19b2b-154">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="19b2b-155">`[ClusterRp <String>]`: Кластер "Кубберсети" — Microsoft.ContainerService (для кластеров AKS) или Microsoft.Kubernetes (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="19b2b-155">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="19b2b-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="19b2b-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19b2b-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19b2b-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="19b2b-158">`[SourceControlConfigurationName <String>]`: Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="19b2b-158">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="19b2b-159">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="19b2b-159">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="19b2b-160">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="19b2b-160">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="19b2b-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19b2b-161">RELATED LINKS</span></span>

