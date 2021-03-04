---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 07b1b36222f0d1a31d4a4a7374957336246f0073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011304"
---
# <span data-ttu-id="2d632-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="2d632-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="2d632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d632-102">SYNOPSIS</span></span>
<span data-ttu-id="2d632-103">Удаление узла с заданным именем в интегрированном времени запуска.</span><span class="sxs-lookup"><span data-stu-id="2d632-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="2d632-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d632-104">SYNTAX</span></span>

### <span data-ttu-id="2d632-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d632-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d632-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d632-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d632-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d632-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d632-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d632-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d632-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d632-109">DESCRIPTION</span></span>
<span data-ttu-id="2d632-110">Для удаления узла в интегрированной runtime удаляется **cmdlet Remove-AzSynapseIntegrationRuntimeNode.**</span><span class="sxs-lookup"><span data-stu-id="2d632-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="2d632-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d632-111">EXAMPLES</span></span>

### <span data-ttu-id="2d632-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d632-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="2d632-113">Удаление узла с заданным именем в интегрированном времени запуска.</span><span class="sxs-lookup"><span data-stu-id="2d632-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="2d632-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d632-114">PARAMETERS</span></span>

### <span data-ttu-id="2d632-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d632-115">-DefaultProfile</span></span>
<span data-ttu-id="2d632-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d632-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d632-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d632-117">-Force</span></span>
<span data-ttu-id="2d632-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2d632-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2d632-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d632-119">-InputObject</span></span>
<span data-ttu-id="2d632-120">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d632-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="2d632-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="2d632-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2d632-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d632-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="2d632-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="2d632-123">-NodeName</span></span>
<span data-ttu-id="2d632-124">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="2d632-124">The integration runtime node name.</span></span>

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

### <span data-ttu-id="2d632-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d632-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d632-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d632-126">Resource group name.</span></span>

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

### <span data-ttu-id="2d632-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d632-127">-ResourceId</span></span>
<span data-ttu-id="2d632-128">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="2d632-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="2d632-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d632-129">-WorkspaceName</span></span>
<span data-ttu-id="2d632-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="2d632-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2d632-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d632-131">-WorkspaceObject</span></span>
<span data-ttu-id="2d632-132">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="2d632-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2d632-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d632-133">-Confirm</span></span>
<span data-ttu-id="2d632-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d632-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d632-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d632-135">-WhatIf</span></span>
<span data-ttu-id="2d632-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d632-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d632-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d632-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d632-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d632-138">CommonParameters</span></span>
<span data-ttu-id="2d632-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d632-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d632-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d632-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d632-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d632-141">INPUTS</span></span>

### <span data-ttu-id="2d632-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d632-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2d632-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2d632-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="2d632-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2d632-144">System.String</span></span>

## <span data-ttu-id="2d632-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d632-145">OUTPUTS</span></span>

### <span data-ttu-id="2d632-146">System.Void</span><span class="sxs-lookup"><span data-stu-id="2d632-146">System.Void</span></span>

## <span data-ttu-id="2d632-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d632-147">NOTES</span></span>

## <span data-ttu-id="2d632-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d632-148">RELATED LINKS</span></span>
