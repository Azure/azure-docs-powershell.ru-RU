---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5c2d7c8aa81cb45b6b49898c95b27256aa504b73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963432"
---
# <span data-ttu-id="57b11-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="57b11-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="57b11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57b11-102">SYNOPSIS</span></span>
<span data-ttu-id="57b11-103">Обновления узла runtime для самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="57b11-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="57b11-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57b11-104">SYNTAX</span></span>

### <span data-ttu-id="57b11-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57b11-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57b11-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57b11-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57b11-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57b11-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57b11-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57b11-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57b11-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57b11-109">DESCRIPTION</span></span>
<span data-ttu-id="57b11-110">Для свойства узла времени самостоятельной интеграции в рабочей области обновляется **cmdlet Update-AzSynapseIntegrationRuntimeNode.**</span><span class="sxs-lookup"><span data-stu-id="57b11-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="57b11-111">В настоящее время поддерживается только обновление "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="57b11-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="57b11-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57b11-112">EXAMPLES</span></span>

### <span data-ttu-id="57b11-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57b11-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="57b11-114">Для узла "Node_1" в режиме самостоятельной интеграции "test-selfhost-ir" для 3-го узла обновляется "ConcurrentJobsLimit".</span><span class="sxs-lookup"><span data-stu-id="57b11-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="57b11-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57b11-115">PARAMETERS</span></span>

### <span data-ttu-id="57b11-116">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="57b11-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="57b11-117">Количество заданий одновременного запуска, разрешенных для узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="57b11-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="57b11-118">Допустимы значения от 1 до maxConcurrentJobs.</span><span class="sxs-lookup"><span data-stu-id="57b11-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="57b11-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b11-119">-DefaultProfile</span></span>
<span data-ttu-id="57b11-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57b11-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b11-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57b11-121">-InputObject</span></span>
<span data-ttu-id="57b11-122">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="57b11-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="57b11-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="57b11-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="57b11-124">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="57b11-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="57b11-125">-Name</span><span class="sxs-lookup"><span data-stu-id="57b11-125">-Name</span></span>
<span data-ttu-id="57b11-126">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="57b11-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="57b11-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b11-127">-ResourceGroupName</span></span>
<span data-ttu-id="57b11-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57b11-128">Resource group name.</span></span>

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

### <span data-ttu-id="57b11-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57b11-129">-ResourceId</span></span>
<span data-ttu-id="57b11-130">Идентификатор ресурса для времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="57b11-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="57b11-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="57b11-131">-WorkspaceName</span></span>
<span data-ttu-id="57b11-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="57b11-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="57b11-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="57b11-133">-WorkspaceObject</span></span>
<span data-ttu-id="57b11-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="57b11-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="57b11-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57b11-135">-Confirm</span></span>
<span data-ttu-id="57b11-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b11-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b11-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b11-137">-WhatIf</span></span>
<span data-ttu-id="57b11-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57b11-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b11-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57b11-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b11-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b11-140">CommonParameters</span></span>
<span data-ttu-id="57b11-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57b11-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b11-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57b11-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b11-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57b11-143">INPUTS</span></span>

### <span data-ttu-id="57b11-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="57b11-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="57b11-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="57b11-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="57b11-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57b11-146">OUTPUTS</span></span>

### <span data-ttu-id="57b11-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="57b11-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="57b11-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57b11-148">NOTES</span></span>

## <span data-ttu-id="57b11-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57b11-149">RELATED LINKS</span></span>
