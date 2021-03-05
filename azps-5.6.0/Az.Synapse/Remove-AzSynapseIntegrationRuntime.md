---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: bf15d0f533f54de589ef354d92c4cf2f600b12cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961080"
---
# <span data-ttu-id="3e9b0-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e9b0-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="3e9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9b0-103">Удаляет время интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="3e9b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e9b0-104">SYNTAX</span></span>

### <span data-ttu-id="3e9b0-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e9b0-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e9b0-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9b0-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e9b0-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9b0-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e9b0-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9b0-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e9b0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e9b0-109">DESCRIPTION</span></span>
<span data-ttu-id="3e9b0-110">Для удаления интегрированного времени запуска удаляется **cmdlet Remove-AzSynapseIntegrationRuntime.**</span><span class="sxs-lookup"><span data-stu-id="3e9b0-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="3e9b0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e9b0-111">EXAMPLES</span></span>

### <span data-ttu-id="3e9b0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e9b0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="3e9b0-113">Эта команда удаляет время интеграции с именем test-reserved-ir из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3e9b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e9b0-114">PARAMETERS</span></span>

### <span data-ttu-id="3e9b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9b0-115">-DefaultProfile</span></span>
<span data-ttu-id="3e9b0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e9b0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3e9b0-117">-Force</span></span>
<span data-ttu-id="3e9b0-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3e9b0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e9b0-119">-InputObject</span></span>
<span data-ttu-id="3e9b0-120">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="3e9b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3e9b0-121">-Name</span></span>
<span data-ttu-id="3e9b0-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e9b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e9b0-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-124">Resource group name.</span></span>

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

### <span data-ttu-id="3e9b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e9b0-125">-ResourceId</span></span>
<span data-ttu-id="3e9b0-126">Идентификатор ресурса для времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="3e9b0-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e9b0-127">-WorkspaceName</span></span>
<span data-ttu-id="3e9b0-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e9b0-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e9b0-129">-WorkspaceObject</span></span>
<span data-ttu-id="3e9b0-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e9b0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e9b0-131">-Confirm</span></span>
<span data-ttu-id="3e9b0-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e9b0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e9b0-133">-WhatIf</span></span>
<span data-ttu-id="3e9b0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e9b0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e9b0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9b0-136">CommonParameters</span></span>
<span data-ttu-id="3e9b0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9b0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9b0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e9b0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9b0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e9b0-139">INPUTS</span></span>

### <span data-ttu-id="3e9b0-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e9b0-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3e9b0-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3e9b0-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3e9b0-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e9b0-142">OUTPUTS</span></span>

### <span data-ttu-id="3e9b0-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="3e9b0-143">System.Void</span></span>

## <span data-ttu-id="3e9b0-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e9b0-144">NOTES</span></span>

## <span data-ttu-id="3e9b0-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e9b0-145">RELATED LINKS</span></span>
