---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415212"
---
# <span data-ttu-id="35dab-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="35dab-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="35dab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35dab-102">SYNOPSIS</span></span>
<span data-ttu-id="35dab-103">Сведения о конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="35dab-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="35dab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35dab-104">SYNTAX</span></span>

### <span data-ttu-id="35dab-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35dab-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35dab-106">Получить</span><span class="sxs-lookup"><span data-stu-id="35dab-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35dab-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35dab-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="35dab-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35dab-108">DESCRIPTION</span></span>
<span data-ttu-id="35dab-109">Сведения о конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="35dab-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="35dab-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35dab-110">EXAMPLES</span></span>

### <span data-ttu-id="35dab-111">Пример 1. Получить все конфигурации кластера куберсетей</span><span class="sxs-lookup"><span data-stu-id="35dab-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="35dab-112">Эта команда получает все конфигурации кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="35dab-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="35dab-113">Пример 2. Настройка кластера куберсетей по имени</span><span class="sxs-lookup"><span data-stu-id="35dab-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="35dab-114">Эта команда получает конфигурацию кластера куберсетей по имени.</span><span class="sxs-lookup"><span data-stu-id="35dab-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="35dab-115">Пример 3. Настройка кластера куберсетей по объектам</span><span class="sxs-lookup"><span data-stu-id="35dab-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="35dab-116">Эта команда получает конфигурацию кластера куберсетей по объектам.</span><span class="sxs-lookup"><span data-stu-id="35dab-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="35dab-117">Пример 4. Настройка кластера куберсетей по конвейеру</span><span class="sxs-lookup"><span data-stu-id="35dab-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="35dab-118">Эта команда получает конфигурацию кластера куберсетей по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="35dab-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="35dab-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35dab-119">PARAMETERS</span></span>

### <span data-ttu-id="35dab-120">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="35dab-120">-ClusterName</span></span>
<span data-ttu-id="35dab-121">Название кластера "Кубберсети".</span><span class="sxs-lookup"><span data-stu-id="35dab-121">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="35dab-122">-ClusterRp</span></span>
<span data-ttu-id="35dab-123">Кластер "Кубберсети" — Microsoft.ContainerService (для кластеров AKS) или Microsoft.Kubernetes (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="35dab-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="35dab-124">-ClusterType</span></span>
<span data-ttu-id="35dab-125">Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="35dab-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35dab-126">-DefaultProfile</span></span>
<span data-ttu-id="35dab-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35dab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35dab-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35dab-128">-InputObject</span></span>
<span data-ttu-id="35dab-129">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="35dab-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-130">-Name</span><span class="sxs-lookup"><span data-stu-id="35dab-130">-Name</span></span>
<span data-ttu-id="35dab-131">Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="35dab-131">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35dab-132">-ResourceGroupName</span></span>
<span data-ttu-id="35dab-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35dab-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35dab-134">-SubscriptionId</span></span>
<span data-ttu-id="35dab-135">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="35dab-135">The Azure subscription ID.</span></span>
<span data-ttu-id="35dab-136">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="35dab-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dab-137">CommonParameters</span></span>
<span data-ttu-id="35dab-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dab-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35dab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dab-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35dab-140">INPUTS</span></span>

### <span data-ttu-id="35dab-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="35dab-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="35dab-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35dab-142">OUTPUTS</span></span>

### <span data-ttu-id="35dab-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="35dab-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="35dab-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35dab-144">NOTES</span></span>

<span data-ttu-id="35dab-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35dab-145">ALIASES</span></span>

<span data-ttu-id="35dab-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="35dab-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35dab-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="35dab-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35dab-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35dab-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35dab-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="35dab-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35dab-150">`[ClusterName <String>]`Название кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="35dab-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="35dab-151">`[ClusterResourceName <String>]`Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="35dab-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="35dab-152">`[ClusterRp <String>]`: Кластер "Кубберсети" — Microsoft.ContainerService (для кластеров AKS) или Microsoft.Kubernetes (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="35dab-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="35dab-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="35dab-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35dab-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35dab-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="35dab-155">`[SourceControlConfigurationName <String>]`: Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="35dab-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="35dab-156">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="35dab-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="35dab-157">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="35dab-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="35dab-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35dab-158">RELATED LINKS</span></span>

