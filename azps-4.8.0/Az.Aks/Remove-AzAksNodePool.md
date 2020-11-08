---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235153"
---
# <span data-ttu-id="ec406-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="ec406-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="ec406-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec406-102">SYNOPSIS</span></span>
<span data-ttu-id="ec406-103">Удаление пула узлов из управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="ec406-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="ec406-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec406-104">SYNTAX</span></span>

### <span data-ttu-id="ec406-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec406-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec406-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec406-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec406-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec406-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec406-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec406-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec406-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec406-109">DESCRIPTION</span></span>
<span data-ttu-id="ec406-110">Удаление пула узлов из управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="ec406-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="ec406-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec406-111">EXAMPLES</span></span>

### <span data-ttu-id="ec406-112">Удаление указанного пула узлов</span><span class="sxs-lookup"><span data-stu-id="ec406-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="ec406-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec406-113">PARAMETERS</span></span>

### <span data-ttu-id="ec406-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec406-114">-AsJob</span></span>
<span data-ttu-id="ec406-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ec406-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec406-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ec406-116">-ClusterName</span></span>
<span data-ttu-id="ec406-117">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ec406-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ec406-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="ec406-118">-ClusterObject</span></span>
<span data-ttu-id="ec406-119">Объект кластера.</span><span class="sxs-lookup"><span data-stu-id="ec406-119">The cluster object.</span></span>

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

### <span data-ttu-id="ec406-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec406-120">-DefaultProfile</span></span>
<span data-ttu-id="ec406-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec406-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec406-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ec406-122">-Force</span></span>
<span data-ttu-id="ec406-123">Удаление пула узлов без запроса</span><span class="sxs-lookup"><span data-stu-id="ec406-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="ec406-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ec406-124">-Id</span></span>
<span data-ttu-id="ec406-125">Идентификатор пула узлов в управляемом кластере Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ec406-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ec406-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec406-126">-InputObject</span></span>
<span data-ttu-id="ec406-127">Объект PSAgentPool, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ec406-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ec406-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec406-128">-Name</span></span>
<span data-ttu-id="ec406-129">Имя пула узлов</span><span class="sxs-lookup"><span data-stu-id="ec406-129">Name of your node pool</span></span>

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

### <span data-ttu-id="ec406-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec406-130">-PassThru</span></span>
<span data-ttu-id="ec406-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ec406-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ec406-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec406-132">-ResourceGroupName</span></span>
<span data-ttu-id="ec406-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ec406-133">Resource group name</span></span>

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

### <span data-ttu-id="ec406-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec406-134">-Confirm</span></span>
<span data-ttu-id="ec406-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ec406-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec406-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec406-136">-WhatIf</span></span>
<span data-ttu-id="ec406-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ec406-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec406-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ec406-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec406-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec406-139">CommonParameters</span></span>
<span data-ttu-id="ec406-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec406-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec406-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec406-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec406-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec406-142">INPUTS</span></span>

### <span data-ttu-id="ec406-143">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="ec406-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="ec406-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ec406-144">System.String</span></span>

## <span data-ttu-id="ec406-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec406-145">OUTPUTS</span></span>

### <span data-ttu-id="ec406-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec406-146">System.Boolean</span></span>

## <span data-ttu-id="ec406-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec406-147">NOTES</span></span>

## <span data-ttu-id="ec406-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec406-148">RELATED LINKS</span></span>
