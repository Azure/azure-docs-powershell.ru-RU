---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: b7bd7866ec6c6ff41a6ef7474b71cfc880e28f49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981800"
---
# <span data-ttu-id="35327-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="35327-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="35327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35327-102">SYNOPSIS</span></span>
<span data-ttu-id="35327-103">Удаляет канал из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="35327-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="35327-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35327-104">SYNTAX</span></span>

### <span data-ttu-id="35327-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35327-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35327-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="35327-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35327-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="35327-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35327-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35327-108">DESCRIPTION</span></span>
<span data-ttu-id="35327-109">Для удаления из рабочей области конвейер удаляется из нее степенный **cmdlet Remove-AzSynapsePipeline.**</span><span class="sxs-lookup"><span data-stu-id="35327-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="35327-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35327-110">EXAMPLES</span></span>

### <span data-ttu-id="35327-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35327-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="35327-112">Этот командлет удаляет канал ContosoPipeline из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="35327-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="35327-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35327-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="35327-114">Этот командлет удаляет канал ContosoPipeline из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="35327-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="35327-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="35327-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="35327-116">Этот командлет удаляет канал ContosoPipeline из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="35327-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="35327-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35327-117">PARAMETERS</span></span>

### <span data-ttu-id="35327-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35327-118">-AsJob</span></span>
<span data-ttu-id="35327-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35327-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35327-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35327-120">-DefaultProfile</span></span>
<span data-ttu-id="35327-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35327-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35327-122">-Force</span><span class="sxs-lookup"><span data-stu-id="35327-122">-Force</span></span>
<span data-ttu-id="35327-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="35327-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="35327-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35327-124">-InputObject</span></span>
<span data-ttu-id="35327-125">Объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="35327-125">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35327-126">-Name</span><span class="sxs-lookup"><span data-stu-id="35327-126">-Name</span></span>
<span data-ttu-id="35327-127">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="35327-127">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35327-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35327-128">-PassThru</span></span>
<span data-ttu-id="35327-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="35327-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="35327-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="35327-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="35327-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35327-131">-WorkspaceName</span></span>
<span data-ttu-id="35327-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="35327-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35327-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="35327-133">-WorkspaceObject</span></span>
<span data-ttu-id="35327-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="35327-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35327-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35327-135">-Confirm</span></span>
<span data-ttu-id="35327-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="35327-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35327-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35327-137">-WhatIf</span></span>
<span data-ttu-id="35327-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35327-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35327-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35327-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35327-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35327-140">CommonParameters</span></span>
<span data-ttu-id="35327-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35327-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35327-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35327-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35327-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35327-143">INPUTS</span></span>

### <span data-ttu-id="35327-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35327-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="35327-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="35327-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="35327-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35327-146">OUTPUTS</span></span>

### <span data-ttu-id="35327-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35327-147">System.Boolean</span></span>

## <span data-ttu-id="35327-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35327-148">NOTES</span></span>

## <span data-ttu-id="35327-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35327-149">RELATED LINKS</span></span>
