---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 27de96fccf2c420bd15e4a7522fecc16fd3032fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993107"
---
# <span data-ttu-id="8de15-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="8de15-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="8de15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de15-102">SYNOPSIS</span></span>
<span data-ttu-id="8de15-103">Удаление пула узлов из управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="8de15-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="8de15-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8de15-104">SYNTAX</span></span>

### <span data-ttu-id="8de15-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8de15-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de15-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de15-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de15-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de15-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8de15-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8de15-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de15-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8de15-109">DESCRIPTION</span></span>
<span data-ttu-id="8de15-110">Удаление пула узлов из управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="8de15-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="8de15-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8de15-111">EXAMPLES</span></span>

### <span data-ttu-id="8de15-112">Удаление указанного пула узлов</span><span class="sxs-lookup"><span data-stu-id="8de15-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="8de15-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8de15-113">PARAMETERS</span></span>

### <span data-ttu-id="8de15-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8de15-114">-AsJob</span></span>
<span data-ttu-id="8de15-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8de15-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8de15-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8de15-116">-ClusterName</span></span>
<span data-ttu-id="8de15-117">Название кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="8de15-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de15-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="8de15-118">-ClusterObject</span></span>
<span data-ttu-id="8de15-119">Объект кластера.</span><span class="sxs-lookup"><span data-stu-id="8de15-119">The cluster object.</span></span>

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

### <span data-ttu-id="8de15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de15-120">-DefaultProfile</span></span>
<span data-ttu-id="8de15-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8de15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de15-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8de15-122">-Force</span></span>
<span data-ttu-id="8de15-123">Удаление пула узлов без запроса</span><span class="sxs-lookup"><span data-stu-id="8de15-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="8de15-124">-Id</span><span class="sxs-lookup"><span data-stu-id="8de15-124">-Id</span></span>
<span data-ttu-id="8de15-125">ИД пула узлов в кластере Managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="8de15-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de15-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8de15-126">-InputObject</span></span>
<span data-ttu-id="8de15-127">Объект PSAgentPool, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="8de15-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="8de15-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8de15-128">-Name</span></span>
<span data-ttu-id="8de15-129">Имя пула узлов</span><span class="sxs-lookup"><span data-stu-id="8de15-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de15-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de15-130">-PassThru</span></span>
<span data-ttu-id="8de15-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="8de15-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8de15-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de15-132">-ResourceGroupName</span></span>
<span data-ttu-id="8de15-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8de15-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de15-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8de15-134">-Confirm</span></span>
<span data-ttu-id="8de15-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8de15-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de15-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de15-136">-WhatIf</span></span>
<span data-ttu-id="8de15-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8de15-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de15-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8de15-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de15-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de15-139">CommonParameters</span></span>
<span data-ttu-id="8de15-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de15-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de15-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8de15-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de15-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8de15-142">INPUTS</span></span>

### <span data-ttu-id="8de15-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="8de15-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="8de15-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8de15-144">System.String</span></span>

## <span data-ttu-id="8de15-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8de15-145">OUTPUTS</span></span>

### <span data-ttu-id="8de15-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8de15-146">System.Boolean</span></span>

## <span data-ttu-id="8de15-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8de15-147">NOTES</span></span>

## <span data-ttu-id="8de15-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8de15-148">RELATED LINKS</span></span>
