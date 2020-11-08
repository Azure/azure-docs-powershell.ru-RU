---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236338"
---
# <span data-ttu-id="072df-101">Get-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="072df-101">Get-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="072df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="072df-102">SYNOPSIS</span></span>
<span data-ttu-id="072df-103">Получает сведения о настройке системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="072df-103">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="072df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="072df-104">SYNTAX</span></span>

### <span data-ttu-id="072df-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="072df-105">List (Default)</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="072df-106">Получить</span><span class="sxs-lookup"><span data-stu-id="072df-106">Get</span></span>
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="072df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="072df-107">GetViaIdentity</span></span>
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="072df-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="072df-108">DESCRIPTION</span></span>
<span data-ttu-id="072df-109">Получает сведения о настройке системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="072df-109">Gets details of the Source Control Configuration.</span></span>

## <span data-ttu-id="072df-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="072df-110">EXAMPLES</span></span>

### <span data-ttu-id="072df-111">Пример 1: получение всех конфигураций кластера kubernetes</span><span class="sxs-lookup"><span data-stu-id="072df-111">Example 1: Get all configurations of kubernetes cluster</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="072df-112">Эта команда получает все конфигурации кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="072df-112">This command gets all configurations of kubernetes cluster.</span></span>

### <span data-ttu-id="072df-113">Пример 2: получение конфигурации кластера kubernetes по имени</span><span class="sxs-lookup"><span data-stu-id="072df-113">Example 2: Get a configuration of kubernetes cluster by name</span></span>
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="072df-114">Эта команда возвращает конфигурацию кластера kubernetes по имени.</span><span class="sxs-lookup"><span data-stu-id="072df-114">This command gets a configuration of kubernetes cluster by name.</span></span>

### <span data-ttu-id="072df-115">Пример 3: получение конфигурации кластера kubernetes по объекту</span><span class="sxs-lookup"><span data-stu-id="072df-115">Example 3: Get a configuration of kubernetes cluster by object</span></span>
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="072df-116">Эта команда получает конфигурацию кластера kubernetes по объекту.</span><span class="sxs-lookup"><span data-stu-id="072df-116">This command gets a configuration of kubernetes cluster by object.</span></span>

### <span data-ttu-id="072df-117">Пример 4: получение конфигурации кластера kubernetes по каналам продаж</span><span class="sxs-lookup"><span data-stu-id="072df-117">Example 4: Get a configuration of kubernetes cluster by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="072df-118">Эта команда возвращает конфигурацию кластера kubernetes с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="072df-118">This command gets a configuration of kubernetes cluster by pipeline.</span></span>

## <span data-ttu-id="072df-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="072df-119">PARAMETERS</span></span>

### <span data-ttu-id="072df-120">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="072df-120">-ClusterName</span></span>
<span data-ttu-id="072df-121">Имя кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="072df-121">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="072df-122">-ClusterRp</span><span class="sxs-lookup"><span data-stu-id="072df-122">-ClusterRp</span></span>
<span data-ttu-id="072df-123">Kubernetes Cluster RP — либо Microsoft. ContainerService (для AKS кластеров), либо Microsoft. Kubernetes (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="072df-123">The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="072df-124">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="072df-124">-ClusterType</span></span>
<span data-ttu-id="072df-125">Имя ресурса кластера Kubernetes — либо managedClusters (для AKS кластеров), либо connectedClusters (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="072df-125">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="072df-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072df-126">-DefaultProfile</span></span>
<span data-ttu-id="072df-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="072df-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="072df-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="072df-128">-InputObject</span></span>
<span data-ttu-id="072df-129">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="072df-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="072df-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="072df-130">-Name</span></span>
<span data-ttu-id="072df-131">Имя конфигурации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="072df-131">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="072df-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072df-132">-ResourceGroupName</span></span>
<span data-ttu-id="072df-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="072df-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="072df-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="072df-134">-SubscriptionId</span></span>
<span data-ttu-id="072df-135">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="072df-135">The Azure subscription ID.</span></span>
<span data-ttu-id="072df-136">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="072df-136">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="072df-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072df-137">CommonParameters</span></span>
<span data-ttu-id="072df-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="072df-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072df-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="072df-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072df-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="072df-140">INPUTS</span></span>

### <span data-ttu-id="072df-141">Microsoft. Azure. PowerShell. командлеты. KubernetesConfiguration. Models. IKubernetesConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="072df-141">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity</span></span>

## <span data-ttu-id="072df-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="072df-142">OUTPUTS</span></span>

### <span data-ttu-id="072df-143">Microsoft. Azure. PowerShell. командлеты. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="072df-143">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="072df-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="072df-144">NOTES</span></span>

<span data-ttu-id="072df-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="072df-145">ALIASES</span></span>

<span data-ttu-id="072df-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="072df-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="072df-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="072df-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="072df-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="072df-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="072df-149">INPUTOBJECT <IKubernetesConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="072df-149">INPUTOBJECT <IKubernetesConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="072df-150">`[ClusterName <String>]`: Имя кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="072df-150">`[ClusterName <String>]`: The name of the kubernetes cluster.</span></span>
  - <span data-ttu-id="072df-151">`[ClusterResourceName <String>]`: Имя ресурса кластера Kubernetes — либо managedClusters (для AKS кластеров), либо connectedClusters (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="072df-151">`[ClusterResourceName <String>]`: The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="072df-152">`[ClusterRp <String>]`: Кластер Kubernetes RP — либо Microsoft. ContainerService (для AKS кластеров), либо Microsoft. Kubernetes (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="072df-152">`[ClusterRp <String>]`: The Kubernetes cluster RP - either Microsoft.ContainerService (for AKS clusters) or Microsoft.Kubernetes (for OnPrem K8S clusters).</span></span>
  - <span data-ttu-id="072df-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="072df-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="072df-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="072df-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="072df-155">`[SourceControlConfigurationName <String>]`: Имя конфигурации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="072df-155">`[SourceControlConfigurationName <String>]`: Name of the Source Control Configuration.</span></span>
  - <span data-ttu-id="072df-156">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="072df-156">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="072df-157">Это строка в формате GUID (например, 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="072df-157">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="072df-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="072df-158">RELATED LINKS</span></span>

