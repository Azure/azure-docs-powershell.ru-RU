---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403692"
---
# <span data-ttu-id="e1ce7-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="e1ce7-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="e1ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ce7-103">Обновление пула узлов в управляемом кластере.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="e1ce7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1ce7-104">SYNTAX</span></span>

### <span data-ttu-id="e1ce7-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1ce7-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ce7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ce7-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ce7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ce7-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ce7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1ce7-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ce7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1ce7-109">DESCRIPTION</span></span>
<span data-ttu-id="e1ce7-110">Обновление пула узлов в управляемом кластере.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="e1ce7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1ce7-111">EXAMPLES</span></span>

### <span data-ttu-id="e1ce7-112">Изменение minimun count на 5 для указанного пула узлов</span><span class="sxs-lookup"><span data-stu-id="e1ce7-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="e1ce7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1ce7-113">PARAMETERS</span></span>

### <span data-ttu-id="e1ce7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1ce7-114">-AsJob</span></span>
<span data-ttu-id="e1ce7-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e1ce7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1ce7-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e1ce7-116">-ClusterName</span></span>
<span data-ttu-id="e1ce7-117">Имя ресурса управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="e1ce7-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="e1ce7-118">-ClusterObject</span></span>
<span data-ttu-id="e1ce7-119">Объект кластера</span><span class="sxs-lookup"><span data-stu-id="e1ce7-119">The cluster object</span></span>

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

### <span data-ttu-id="e1ce7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ce7-120">-DefaultProfile</span></span>
<span data-ttu-id="e1ce7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ce7-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="e1ce7-122">-EnableAutoScaling</span></span>
<span data-ttu-id="e1ce7-123">Следует ли включить авто scaler</span><span class="sxs-lookup"><span data-stu-id="e1ce7-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="e1ce7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e1ce7-124">-Force</span></span>
<span data-ttu-id="e1ce7-125">Обновление пула узлов без запроса</span><span class="sxs-lookup"><span data-stu-id="e1ce7-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="e1ce7-126">-Id</span><span class="sxs-lookup"><span data-stu-id="e1ce7-126">-Id</span></span>
<span data-ttu-id="e1ce7-127">Id of an node pool in Managed Kubernetes cluster</span><span class="sxs-lookup"><span data-stu-id="e1ce7-127">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e1ce7-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1ce7-128">-InputObject</span></span>
<span data-ttu-id="e1ce7-129">Объект PSAgentPool, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="e1ce7-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e1ce7-130">-KubernetesVersion</span></span>
<span data-ttu-id="e1ce7-131">Версия Кубберсетей, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="e1ce7-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e1ce7-132">-MaxCount</span></span>
<span data-ttu-id="e1ce7-133">Максимальное количество узлов для автоматического масштабирования</span><span class="sxs-lookup"><span data-stu-id="e1ce7-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="e1ce7-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="e1ce7-134">-MinCount</span></span>
<span data-ttu-id="e1ce7-135">Минимальное количество узлов для автоматического масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="e1ce7-136">-Name</span><span class="sxs-lookup"><span data-stu-id="e1ce7-136">-Name</span></span>
<span data-ttu-id="e1ce7-137">Имя пула узлов.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-137">The name of the node pool.</span></span>

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

### <span data-ttu-id="e1ce7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ce7-138">-ResourceGroupName</span></span>
<span data-ttu-id="e1ce7-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="e1ce7-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1ce7-140">-Confirm</span></span>
<span data-ttu-id="e1ce7-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ce7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ce7-142">-WhatIf</span></span>
<span data-ttu-id="e1ce7-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ce7-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ce7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ce7-145">CommonParameters</span></span>
<span data-ttu-id="e1ce7-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ce7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ce7-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1ce7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ce7-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1ce7-148">INPUTS</span></span>

### <span data-ttu-id="e1ce7-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="e1ce7-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="e1ce7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e1ce7-150">System.String</span></span>

## <span data-ttu-id="e1ce7-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1ce7-151">OUTPUTS</span></span>

### <span data-ttu-id="e1ce7-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="e1ce7-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="e1ce7-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1ce7-153">NOTES</span></span>

## <span data-ttu-id="e1ce7-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1ce7-154">RELATED LINKS</span></span>
