---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247893"
---
# <span data-ttu-id="7d8f6-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="7d8f6-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="7d8f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8f6-103">Обновление пула узлов в управляемом кластере.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="7d8f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d8f6-104">SYNTAX</span></span>

### <span data-ttu-id="7d8f6-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d8f6-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8f6-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8f6-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8f6-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8f6-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8f6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8f6-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d8f6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8f6-109">DESCRIPTION</span></span>
<span data-ttu-id="7d8f6-110">Обновление пула узлов в управляемом кластере.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="7d8f6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d8f6-111">EXAMPLES</span></span>

### <span data-ttu-id="7d8f6-112">Изменить число minimun на 5 для указанного пула узлов</span><span class="sxs-lookup"><span data-stu-id="7d8f6-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="7d8f6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d8f6-113">PARAMETERS</span></span>

### <span data-ttu-id="7d8f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d8f6-114">-AsJob</span></span>
<span data-ttu-id="7d8f6-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7d8f6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d8f6-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="7d8f6-116">-ClusterName</span></span>
<span data-ttu-id="7d8f6-117">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f6-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="7d8f6-118">-ClusterObject</span></span>
<span data-ttu-id="7d8f6-119">Объект Cluster</span><span class="sxs-lookup"><span data-stu-id="7d8f6-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8f6-120">-DefaultProfile</span></span>
<span data-ttu-id="7d8f6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8f6-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="7d8f6-122">-EnableAutoScaling</span></span>
<span data-ttu-id="7d8f6-123">Следует ли включить автоматическое масштабирование</span><span class="sxs-lookup"><span data-stu-id="7d8f6-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="7d8f6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7d8f6-124">-Force</span></span>
<span data-ttu-id="7d8f6-125">Обновление пула узлов без запроса</span><span class="sxs-lookup"><span data-stu-id="7d8f6-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="7d8f6-126">-ID</span><span class="sxs-lookup"><span data-stu-id="7d8f6-126">-Id</span></span>
<span data-ttu-id="7d8f6-127">Идентификатор пула узлов в управляемом кластере Kubernetes</span><span class="sxs-lookup"><span data-stu-id="7d8f6-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d8f6-128">-InputObject</span></span>
<span data-ttu-id="7d8f6-129">Объект PSAgentPool, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f6-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="7d8f6-130">-KubernetesVersion</span></span>
<span data-ttu-id="7d8f6-131">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="7d8f6-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7d8f6-132">-MaxCount</span></span>
<span data-ttu-id="7d8f6-133">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="7d8f6-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="7d8f6-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="7d8f6-134">-MinCount</span></span>
<span data-ttu-id="7d8f6-135">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="7d8f6-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d8f6-136">-Name</span></span>
<span data-ttu-id="7d8f6-137">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8f6-138">-ResourceGroupName</span></span>
<span data-ttu-id="7d8f6-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8f6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d8f6-140">-Confirm</span></span>
<span data-ttu-id="7d8f6-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8f6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8f6-142">-WhatIf</span></span>
<span data-ttu-id="7d8f6-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8f6-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8f6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8f6-145">CommonParameters</span></span>
<span data-ttu-id="7d8f6-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d8f6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8f6-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d8f6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8f6-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d8f6-148">INPUTS</span></span>

### <span data-ttu-id="7d8f6-149">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="7d8f6-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="7d8f6-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7d8f6-150">System.String</span></span>

## <span data-ttu-id="7d8f6-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8f6-151">OUTPUTS</span></span>

### <span data-ttu-id="7d8f6-152">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="7d8f6-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="7d8f6-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d8f6-153">NOTES</span></span>

## <span data-ttu-id="7d8f6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d8f6-154">RELATED LINKS</span></span>
