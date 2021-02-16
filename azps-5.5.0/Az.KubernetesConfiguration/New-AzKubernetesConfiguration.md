---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 425a2f2fcc145b360ea981a4d78113d6053c90e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219409"
---
# <span data-ttu-id="1f312-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f312-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="1f312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f312-102">SYNOPSIS</span></span>
<span data-ttu-id="1f312-103">Создайте новую конфигурацию управления исходными данными в Кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="1f312-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="1f312-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f312-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f312-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f312-105">DESCRIPTION</span></span>
<span data-ttu-id="1f312-106">Создайте новую конфигурацию управления исходным источником в Кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="1f312-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="1f312-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f312-107">EXAMPLES</span></span>

### <span data-ttu-id="1f312-108">Пример 1. Создание конфигурации для кластера куберсетей</span><span class="sxs-lookup"><span data-stu-id="1f312-108">Example 1: Create a configuration for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t01 -RepositoryUrl http://github.com/xxxx

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t01 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="1f312-109">Эта команда создает конфигурацию кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="1f312-109">This command creates a configuration for kubernetes cluster.</span></span>

### <span data-ttu-id="1f312-110">Пример 1. Создание конфигурации кластера куберсетей с указанием параметра OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="1f312-110">Example 1: Create a configuration for kubernetes cluster with specify paramter OperatorNamespace</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -ResourceGroupName azure-rg-test -ClusterName k8scluster-t01 -Name k8sconfig-t02 -RepositoryUrl http://github.com/xxxx -OperatorNamespace namespace-t01

Name          SystemDataCreatedAt   SystemDataCreatedBy SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
----          -------------------   ------------------- ----------------------- ------------------------ ------------------------ ---------------------------- ----
k8sconfig-t02 12/21/2020 5:26:17 AM                                             12/21/2020 5:26:17 AM                                                          Microsoft.KubernetesConfiguration/so…
```

<span data-ttu-id="1f312-111">Эта команда создает конфигурацию в новом пространстве имен оператора для кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="1f312-111">This command creates a configuration in the new operator namespace for kubernetes cluster.</span></span>
<span data-ttu-id="1f312-112">Обратите внимание: не удается создать конфигурацию в существующем пространстве имен оператора.</span><span class="sxs-lookup"><span data-stu-id="1f312-112">Note, Unable to create a configuration in an existing operator namespace.</span></span>

## <span data-ttu-id="1f312-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f312-113">PARAMETERS</span></span>

### <span data-ttu-id="1f312-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1f312-114">-ClusterName</span></span>
<span data-ttu-id="1f312-115">Название кластера "Кубберсети".</span><span class="sxs-lookup"><span data-stu-id="1f312-115">The name of the kubernetes cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f312-116">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="1f312-116">-ClusterScoped</span></span>
<span data-ttu-id="1f312-117">Если он прошел, задате область настройки кластера (по умолчанию — nameSpace).</span><span class="sxs-lookup"><span data-stu-id="1f312-117">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="1f312-118">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="1f312-118">-ClusterType</span></span>
<span data-ttu-id="1f312-119">Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="1f312-119">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="1f312-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f312-120">-DefaultProfile</span></span>
<span data-ttu-id="1f312-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f312-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f312-122">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="1f312-122">-EnableHelmOperator</span></span>
<span data-ttu-id="1f312-123">Параметр для настройки helm Operator (Оператор helm).</span><span class="sxs-lookup"><span data-stu-id="1f312-123">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="1f312-124">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="1f312-124">-HelmOperatorChartValues</span></span>
<span data-ttu-id="1f312-125">Переопределять значения для оператора Helm Chart.</span><span class="sxs-lookup"><span data-stu-id="1f312-125">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="1f312-126">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="1f312-126">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="1f312-127">Версия оператора Helm chart.</span><span class="sxs-lookup"><span data-stu-id="1f312-127">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="1f312-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1f312-128">-Name</span></span>
<span data-ttu-id="1f312-129">Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="1f312-129">Name of the Source Control Configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f312-130">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="1f312-130">-OperatorInstanceName</span></span>
<span data-ttu-id="1f312-131">Имя экземпляра оператора, определяющий конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1f312-131">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="1f312-132">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="1f312-132">-OperatorNamespace</span></span>
<span data-ttu-id="1f312-133">Пространство имен, к которому установлен этот оператор.</span><span class="sxs-lookup"><span data-stu-id="1f312-133">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="1f312-134">Не более 253 нижних букв и цифр, дефис и точка.</span><span class="sxs-lookup"><span data-stu-id="1f312-134">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="1f312-135">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="1f312-135">-OperatorParameters</span></span>
<span data-ttu-id="1f312-136">Любые параметры экземпляра "Оператор" в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="1f312-136">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="1f312-137">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="1f312-137">-RepositoryUrl</span></span>
<span data-ttu-id="1f312-138">URL-адрес репозитория SourceControl.</span><span class="sxs-lookup"><span data-stu-id="1f312-138">Url of the SourceControl Repository.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f312-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f312-139">-ResourceGroupName</span></span>
<span data-ttu-id="1f312-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f312-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f312-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f312-141">-SubscriptionId</span></span>
<span data-ttu-id="1f312-142">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="1f312-142">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f312-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f312-143">-Confirm</span></span>
<span data-ttu-id="1f312-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f312-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f312-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f312-145">-WhatIf</span></span>
<span data-ttu-id="1f312-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f312-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f312-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f312-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f312-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f312-148">CommonParameters</span></span>
<span data-ttu-id="1f312-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f312-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f312-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f312-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f312-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f312-151">INPUTS</span></span>

## <span data-ttu-id="1f312-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f312-152">OUTPUTS</span></span>

### <span data-ttu-id="1f312-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f312-153">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20201001Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="1f312-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f312-154">NOTES</span></span>

<span data-ttu-id="1f312-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1f312-155">ALIASES</span></span>

## <span data-ttu-id="1f312-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f312-156">RELATED LINKS</span></span>

