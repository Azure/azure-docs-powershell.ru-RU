---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415191"
---
# <span data-ttu-id="d91f6-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="d91f6-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="d91f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d91f6-103">Создайте новую конфигурацию управления исходными данными в Кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="d91f6-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="d91f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d91f6-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d91f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d91f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d91f6-106">Создайте новую конфигурацию управления исходными данными в Кубберсетях.</span><span class="sxs-lookup"><span data-stu-id="d91f6-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="d91f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d91f6-107">EXAMPLES</span></span>

### <span data-ttu-id="d91f6-108">Пример 1. Создание configuation для кластера kubernetes</span><span class="sxs-lookup"><span data-stu-id="d91f6-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="d91f6-109">Эта команда создает слияние для кластера куберсетей.</span><span class="sxs-lookup"><span data-stu-id="d91f6-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="d91f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d91f6-110">PARAMETERS</span></span>

### <span data-ttu-id="d91f6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d91f6-111">-ClusterName</span></span>
<span data-ttu-id="d91f6-112">Название кластера "Кубберсети".</span><span class="sxs-lookup"><span data-stu-id="d91f6-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="d91f6-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="d91f6-113">-ClusterScoped</span></span>
<span data-ttu-id="d91f6-114">Если он прошел, задате область настройки кластера (по умолчанию — nameSpace).</span><span class="sxs-lookup"><span data-stu-id="d91f6-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="d91f6-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d91f6-115">-ClusterType</span></span>
<span data-ttu-id="d91f6-116">Название ресурсов кластера "Кубберсети" — управляемые кластеры (для кластеров AKS) или подключенные (для кластеров OnPrem K8S).</span><span class="sxs-lookup"><span data-stu-id="d91f6-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="d91f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91f6-117">-DefaultProfile</span></span>
<span data-ttu-id="d91f6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d91f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d91f6-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="d91f6-119">-EnableHelmOperator</span></span>
<span data-ttu-id="d91f6-120">Параметр для настройки helm Operator (Оператор helm).</span><span class="sxs-lookup"><span data-stu-id="d91f6-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="d91f6-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="d91f6-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="d91f6-122">Переопределять значения для оператора Helm Chart.</span><span class="sxs-lookup"><span data-stu-id="d91f6-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="d91f6-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="d91f6-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="d91f6-124">Версия оператора Helm Chart.</span><span class="sxs-lookup"><span data-stu-id="d91f6-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="d91f6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d91f6-125">-Name</span></span>
<span data-ttu-id="d91f6-126">Имя конфигурации управления источником.</span><span class="sxs-lookup"><span data-stu-id="d91f6-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="d91f6-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="d91f6-127">-OperatorInstanceName</span></span>
<span data-ttu-id="d91f6-128">Имя экземпляра оператора, определяющий конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d91f6-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="d91f6-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="d91f6-129">-OperatorNamespace</span></span>
<span data-ttu-id="d91f6-130">Пространство имен, к которому установлен этот оператор.</span><span class="sxs-lookup"><span data-stu-id="d91f6-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="d91f6-131">Не более 253 нижних букв и цифр, дефис и точка.</span><span class="sxs-lookup"><span data-stu-id="d91f6-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="d91f6-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="d91f6-132">-OperatorParameters</span></span>
<span data-ttu-id="d91f6-133">Любые параметры экземпляра "Оператор" в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="d91f6-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="d91f6-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="d91f6-134">-RepositoryUrl</span></span>
<span data-ttu-id="d91f6-135">URL-адрес репозитория SourceControl.</span><span class="sxs-lookup"><span data-stu-id="d91f6-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="d91f6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91f6-136">-ResourceGroupName</span></span>
<span data-ttu-id="d91f6-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d91f6-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="d91f6-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d91f6-138">-SubscriptionId</span></span>
<span data-ttu-id="d91f6-139">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d91f6-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d91f6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d91f6-140">-Confirm</span></span>
<span data-ttu-id="d91f6-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d91f6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d91f6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d91f6-142">-WhatIf</span></span>
<span data-ttu-id="d91f6-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d91f6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d91f6-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d91f6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d91f6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91f6-145">CommonParameters</span></span>
<span data-ttu-id="d91f6-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91f6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91f6-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d91f6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91f6-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d91f6-148">INPUTS</span></span>

## <span data-ttu-id="d91f6-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d91f6-149">OUTPUTS</span></span>

### <span data-ttu-id="d91f6-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d91f6-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="d91f6-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d91f6-151">NOTES</span></span>

<span data-ttu-id="d91f6-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d91f6-152">ALIASES</span></span>

## <span data-ttu-id="d91f6-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d91f6-153">RELATED LINKS</span></span>

