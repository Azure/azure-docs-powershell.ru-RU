---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/new-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/New-AzKubernetesConfiguration.md
ms.openlocfilehash: 70ff3c636f6c88ac89e53a5c2b1acb209aad274a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236328"
---
# <span data-ttu-id="ce268-101">New-AzKubernetesConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce268-101">New-AzKubernetesConfiguration</span></span>

## <span data-ttu-id="ce268-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce268-102">SYNOPSIS</span></span>
<span data-ttu-id="ce268-103">Создайте новую конфигурацию системы управления версиями Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ce268-103">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="ce268-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce268-104">SYNTAX</span></span>

```
New-AzKubernetesConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 -RepositoryUrl <String> [-ClusterType <String>] [-SubscriptionId <String>] [-ClusterScoped]
 [-EnableHelmOperator] [-HelmOperatorChartValues <String>] [-HelmOperatorChartVersion <String>]
 [-OperatorInstanceName <String>] [-OperatorNamespace <String>] [-OperatorParameters <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce268-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce268-105">DESCRIPTION</span></span>
<span data-ttu-id="ce268-106">Создайте новую конфигурацию системы управления версиями Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ce268-106">Create a new Kubernetes Source Control Configuration.</span></span>

## <span data-ttu-id="ce268-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce268-107">EXAMPLES</span></span>

### <span data-ttu-id="ce268-108">Пример 1: создание configuation для кластера kubernetes</span><span class="sxs-lookup"><span data-stu-id="ce268-108">Example 1: Create a configuation for kubernetes cluster</span></span>
```powershell
PS C:\> New-AzKubernetesConfiguration -Name conf-test01 -ClusterName connaks-d983yc -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

<span data-ttu-id="ce268-109">Эта команда создает configuation для кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ce268-109">This command creates a configuation for kubernetes cluster.</span></span>

## <span data-ttu-id="ce268-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce268-110">PARAMETERS</span></span>

### <span data-ttu-id="ce268-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ce268-111">-ClusterName</span></span>
<span data-ttu-id="ce268-112">Имя кластера kubernetes.</span><span class="sxs-lookup"><span data-stu-id="ce268-112">The name of the kubernetes cluster.</span></span>

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

### <span data-ttu-id="ce268-113">-ClusterScoped</span><span class="sxs-lookup"><span data-stu-id="ce268-113">-ClusterScoped</span></span>
<span data-ttu-id="ce268-114">При переданном параметре задает область конфигурации для кластера (значение по умолчанию — nameSpace).</span><span class="sxs-lookup"><span data-stu-id="ce268-114">If passed set the scope of the Configuration to Cluster (default is nameSpace).</span></span>

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

### <span data-ttu-id="ce268-115">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ce268-115">-ClusterType</span></span>
<span data-ttu-id="ce268-116">Имя ресурса кластера Kubernetes — либо managedClusters (для AKS кластеров), либо connectedClusters (для локальных кластеров K8S).</span><span class="sxs-lookup"><span data-stu-id="ce268-116">The Kubernetes cluster resource name - either managedClusters (for AKS clusters) or connectedClusters (for OnPrem K8S clusters).</span></span>

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

### <span data-ttu-id="ce268-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce268-117">-DefaultProfile</span></span>
<span data-ttu-id="ce268-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce268-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce268-119">-EnableHelmOperator</span><span class="sxs-lookup"><span data-stu-id="ce268-119">-EnableHelmOperator</span></span>
<span data-ttu-id="ce268-120">Параметр для включения Helm оператора для этой конфигурации Git.</span><span class="sxs-lookup"><span data-stu-id="ce268-120">Option to enable Helm Operator for this git configuration.</span></span>

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

### <span data-ttu-id="ce268-121">-HelmOperatorChartValues</span><span class="sxs-lookup"><span data-stu-id="ce268-121">-HelmOperatorChartValues</span></span>
<span data-ttu-id="ce268-122">Переопределение значений в диаграмме Helm оператора.</span><span class="sxs-lookup"><span data-stu-id="ce268-122">Values override for the operator Helm chart.</span></span>

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

### <span data-ttu-id="ce268-123">-HelmOperatorChartVersion</span><span class="sxs-lookup"><span data-stu-id="ce268-123">-HelmOperatorChartVersion</span></span>
<span data-ttu-id="ce268-124">Версия Helm оператора на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="ce268-124">Version of the operator Helm chart.</span></span>

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

### <span data-ttu-id="ce268-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce268-125">-Name</span></span>
<span data-ttu-id="ce268-126">Имя конфигурации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ce268-126">Name of the Source Control Configuration.</span></span>

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

### <span data-ttu-id="ce268-127">-OperatorInstanceName</span><span class="sxs-lookup"><span data-stu-id="ce268-127">-OperatorInstanceName</span></span>
<span data-ttu-id="ce268-128">Имя экземпляра оператора, определяющего определенную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ce268-128">Instance name of the operator - identifying the specific configuration.</span></span>

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

### <span data-ttu-id="ce268-129">-OperatorNamespace</span><span class="sxs-lookup"><span data-stu-id="ce268-129">-OperatorNamespace</span></span>
<span data-ttu-id="ce268-130">Пространство имен, в которое установлен этот оператор.</span><span class="sxs-lookup"><span data-stu-id="ce268-130">The namespace to which this operator is installed to.</span></span>
<span data-ttu-id="ce268-131">Не более 253 строчных букв, дефисов и периодических знаков.</span><span class="sxs-lookup"><span data-stu-id="ce268-131">Maximum of 253 lower case alphanumeric characters, hyphen and period only.</span></span>

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

### <span data-ttu-id="ce268-132">-OperatorParameters</span><span class="sxs-lookup"><span data-stu-id="ce268-132">-OperatorParameters</span></span>
<span data-ttu-id="ce268-133">Любые параметры для экземпляра оператора в строковом формате.</span><span class="sxs-lookup"><span data-stu-id="ce268-133">Any Parameters for the Operator instance in string format.</span></span>

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

### <span data-ttu-id="ce268-134">-RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="ce268-134">-RepositoryUrl</span></span>
<span data-ttu-id="ce268-135">URL-адрес репозитория SourceControl.</span><span class="sxs-lookup"><span data-stu-id="ce268-135">Url of the SourceControl Repository.</span></span>

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

### <span data-ttu-id="ce268-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce268-136">-ResourceGroupName</span></span>
<span data-ttu-id="ce268-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce268-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce268-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce268-138">-SubscriptionId</span></span>
<span data-ttu-id="ce268-139">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ce268-139">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="ce268-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce268-140">-Confirm</span></span>
<span data-ttu-id="ce268-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce268-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce268-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce268-142">-WhatIf</span></span>
<span data-ttu-id="ce268-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce268-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce268-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce268-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce268-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce268-145">CommonParameters</span></span>
<span data-ttu-id="ce268-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce268-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce268-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce268-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce268-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce268-148">INPUTS</span></span>

## <span data-ttu-id="ce268-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce268-149">OUTPUTS</span></span>

### <span data-ttu-id="ce268-150">Microsoft. Azure. PowerShell. командлеты. KubernetesConfiguration. Models. Api20191101Preview. ISourceControlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce268-150">Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.Api20191101Preview.ISourceControlConfiguration</span></span>

## <span data-ttu-id="ce268-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce268-151">NOTES</span></span>

<span data-ttu-id="ce268-152">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ce268-152">ALIASES</span></span>

## <span data-ttu-id="ce268-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce268-153">RELATED LINKS</span></span>

