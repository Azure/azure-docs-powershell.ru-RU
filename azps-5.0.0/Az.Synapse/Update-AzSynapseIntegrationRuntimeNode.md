---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245147"
---
# <span data-ttu-id="b0800-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b0800-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b0800-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0800-102">SYNOPSIS</span></span>
<span data-ttu-id="b0800-103">Обновляет узел среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="b0800-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="b0800-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0800-104">SYNTAX</span></span>

### <span data-ttu-id="b0800-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0800-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0800-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0800-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0800-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0800-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0800-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0800-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0800-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0800-109">DESCRIPTION</span></span>
<span data-ttu-id="b0800-110">Командлет **Update-AzSynapseIntegrationRuntimeNode** обновляет свойства узла среды выполнения интеграции с самостоятельным размещением в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b0800-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="b0800-111">В настоящее время поддерживается только обновление "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="b0800-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="b0800-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0800-112">EXAMPLES</span></span>

### <span data-ttu-id="b0800-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0800-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="b0800-114">Командлет обновляет "ConcurrentJobsLimit" до 3 для узла "Node_1" в саморазмещенной среде выполнения Integration теста-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="b0800-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b0800-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0800-115">PARAMETERS</span></span>

### <span data-ttu-id="b0800-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="b0800-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="b0800-117">Количество одновременных заданий, разрешенных для выполнения на узле среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="b0800-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="b0800-118">Значения в диапазоне от 1 до maxConcurrentJobs разрешены.</span><span class="sxs-lookup"><span data-stu-id="b0800-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0800-119">-DefaultProfile</span></span>
<span data-ttu-id="b0800-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0800-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0800-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0800-121">-InputObject</span></span>
<span data-ttu-id="b0800-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="b0800-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b0800-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b0800-124">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="b0800-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0800-125">-Name</span></span>
<span data-ttu-id="b0800-126">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="b0800-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b0800-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0800-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0800-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0800-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0800-129">-ResourceId</span></span>
<span data-ttu-id="b0800-130">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0800-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0800-131">-WorkspaceName</span></span>
<span data-ttu-id="b0800-132">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b0800-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b0800-133">-WorkspaceObject</span></span>
<span data-ttu-id="b0800-134">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b0800-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0800-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0800-135">-Confirm</span></span>
<span data-ttu-id="b0800-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b0800-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0800-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0800-137">-WhatIf</span></span>
<span data-ttu-id="b0800-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b0800-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0800-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b0800-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0800-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0800-140">CommonParameters</span></span>
<span data-ttu-id="b0800-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0800-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0800-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0800-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0800-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0800-143">INPUTS</span></span>

### <span data-ttu-id="b0800-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0800-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b0800-145">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b0800-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b0800-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0800-146">OUTPUTS</span></span>

### <span data-ttu-id="b0800-147">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="b0800-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="b0800-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0800-148">NOTES</span></span>

## <span data-ttu-id="b0800-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0800-149">RELATED LINKS</span></span>
