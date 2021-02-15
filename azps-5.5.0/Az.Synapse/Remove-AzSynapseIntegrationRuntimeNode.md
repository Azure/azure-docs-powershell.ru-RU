---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232420"
---
# <span data-ttu-id="dded3-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="dded3-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="dded3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dded3-102">SYNOPSIS</span></span>
<span data-ttu-id="dded3-103">Удалите узел с заданным именем в интегрированном времени запуска.</span><span class="sxs-lookup"><span data-stu-id="dded3-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="dded3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dded3-104">SYNTAX</span></span>

### <span data-ttu-id="dded3-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dded3-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dded3-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dded3-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dded3-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dded3-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dded3-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dded3-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dded3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dded3-109">DESCRIPTION</span></span>
<span data-ttu-id="dded3-110">Для удаления узла в интегрированной runtime удаляется **cmdlet Remove-AzSynapseIntegrationRuntimeNode.**</span><span class="sxs-lookup"><span data-stu-id="dded3-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="dded3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dded3-111">EXAMPLES</span></span>

### <span data-ttu-id="dded3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dded3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="dded3-113">Удалите узел с заданным именем в интегрированном времени запуска.</span><span class="sxs-lookup"><span data-stu-id="dded3-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="dded3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dded3-114">PARAMETERS</span></span>

### <span data-ttu-id="dded3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dded3-115">-DefaultProfile</span></span>
<span data-ttu-id="dded3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dded3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dded3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dded3-117">-Force</span></span>
<span data-ttu-id="dded3-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dded3-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dded3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dded3-119">-InputObject</span></span>
<span data-ttu-id="dded3-120">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="dded3-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dded3-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="dded3-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="dded3-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="dded3-123">-NodeName</span></span>
<span data-ttu-id="dded3-124">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="dded3-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dded3-125">-ResourceGroupName</span></span>
<span data-ttu-id="dded3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dded3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dded3-127">-ResourceId</span></span>
<span data-ttu-id="dded3-128">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="dded3-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dded3-129">-WorkspaceName</span></span>
<span data-ttu-id="dded3-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="dded3-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dded3-131">-WorkspaceObject</span></span>
<span data-ttu-id="dded3-132">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="dded3-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dded3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dded3-133">-Confirm</span></span>
<span data-ttu-id="dded3-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dded3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dded3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dded3-135">-WhatIf</span></span>
<span data-ttu-id="dded3-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dded3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dded3-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dded3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dded3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dded3-138">CommonParameters</span></span>
<span data-ttu-id="dded3-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dded3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dded3-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dded3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dded3-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dded3-141">INPUTS</span></span>

### <span data-ttu-id="dded3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dded3-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dded3-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dded3-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="dded3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="dded3-144">System.String</span></span>

## <span data-ttu-id="dded3-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dded3-145">OUTPUTS</span></span>

### <span data-ttu-id="dded3-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="dded3-146">System.Void</span></span>

## <span data-ttu-id="dded3-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dded3-147">NOTES</span></span>

## <span data-ttu-id="dded3-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dded3-148">RELATED LINKS</span></span>
