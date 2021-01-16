---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507910"
---
# <span data-ttu-id="dbdce-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="dbdce-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="dbdce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbdce-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdce-103">Синхронизирует учетные данные между узлами времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbdce-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="dbdce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbdce-104">SYNTAX</span></span>

### <span data-ttu-id="dbdce-105">StopByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dbdce-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdce-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdce-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdce-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdce-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbdce-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbdce-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbdce-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbdce-109">DESCRIPTION</span></span>
<span data-ttu-id="dbdce-110">Cmdlet **Sync-AzSynapseIntegrationRuntimeCredential** синхронизирует учетные данные на локальном устройстве с узлами времени интеграции, что не только является одинаковым для всех узлов.</span><span class="sxs-lookup"><span data-stu-id="dbdce-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="dbdce-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbdce-111">EXAMPLES</span></span>

### <span data-ttu-id="dbdce-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbdce-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="dbdce-113">Синхронизирует учетные данные между узлами времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbdce-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="dbdce-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbdce-114">PARAMETERS</span></span>

### <span data-ttu-id="dbdce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdce-115">-DefaultProfile</span></span>
<span data-ttu-id="dbdce-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbdce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdce-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dbdce-117">-Force</span></span>
<span data-ttu-id="dbdce-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dbdce-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dbdce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbdce-119">-InputObject</span></span>
<span data-ttu-id="dbdce-120">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbdce-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdce-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dbdce-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="dbdce-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="dbdce-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdce-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbdce-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbdce-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdce-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbdce-125">-ResourceId</span></span>
<span data-ttu-id="dbdce-126">Идентификатор ресурса для времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="dbdce-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdce-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dbdce-127">-WorkspaceName</span></span>
<span data-ttu-id="dbdce-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="dbdce-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdce-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dbdce-129">-WorkspaceObject</span></span>
<span data-ttu-id="dbdce-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="dbdce-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdce-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbdce-131">-Confirm</span></span>
<span data-ttu-id="dbdce-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dbdce-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdce-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdce-133">-WhatIf</span></span>
<span data-ttu-id="dbdce-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbdce-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdce-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dbdce-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdce-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdce-136">CommonParameters</span></span>
<span data-ttu-id="dbdce-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdce-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdce-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbdce-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdce-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbdce-139">INPUTS</span></span>

### <span data-ttu-id="dbdce-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dbdce-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dbdce-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dbdce-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dbdce-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbdce-142">OUTPUTS</span></span>

### <span data-ttu-id="dbdce-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="dbdce-143">System.Void</span></span>

## <span data-ttu-id="dbdce-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbdce-144">NOTES</span></span>

## <span data-ttu-id="dbdce-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbdce-145">RELATED LINKS</span></span>
