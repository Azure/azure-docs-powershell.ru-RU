---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: 747658224703a09f98f232deb865adf4bb084682
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413636"
---
# <span data-ttu-id="776ca-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="776ca-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="776ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="776ca-102">SYNOPSIS</span></span>
<span data-ttu-id="776ca-103">Удаляет канал из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="776ca-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="776ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="776ca-104">SYNTAX</span></span>

### <span data-ttu-id="776ca-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="776ca-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776ca-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="776ca-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776ca-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="776ca-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="776ca-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="776ca-108">DESCRIPTION</span></span>
<span data-ttu-id="776ca-109">Для удаления конвейера из рабочей области будет удален из нее **cmdlet Remove-AzSynapsePipeline.**</span><span class="sxs-lookup"><span data-stu-id="776ca-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="776ca-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="776ca-110">EXAMPLES</span></span>

### <span data-ttu-id="776ca-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="776ca-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="776ca-112">Этот командлет удаляет канал ContosoPipeline из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="776ca-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="776ca-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="776ca-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="776ca-114">Этот командлет удаляет канал ContosoPipeline из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="776ca-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="776ca-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="776ca-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="776ca-116">Этот командлет удаляет канал ContosoPipeline из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="776ca-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="776ca-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="776ca-117">PARAMETERS</span></span>

### <span data-ttu-id="776ca-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="776ca-118">-AsJob</span></span>
<span data-ttu-id="776ca-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="776ca-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="776ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776ca-120">-DefaultProfile</span></span>
<span data-ttu-id="776ca-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="776ca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="776ca-122">-Force</span><span class="sxs-lookup"><span data-stu-id="776ca-122">-Force</span></span>
<span data-ttu-id="776ca-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="776ca-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="776ca-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="776ca-124">-InputObject</span></span>
<span data-ttu-id="776ca-125">Объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="776ca-125">The pipeline object.</span></span>

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

### <span data-ttu-id="776ca-126">-Name</span><span class="sxs-lookup"><span data-stu-id="776ca-126">-Name</span></span>
<span data-ttu-id="776ca-127">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="776ca-127">The pipeline name.</span></span>

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

### <span data-ttu-id="776ca-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="776ca-128">-PassThru</span></span>
<span data-ttu-id="776ca-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="776ca-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="776ca-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="776ca-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="776ca-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="776ca-131">-WorkspaceName</span></span>
<span data-ttu-id="776ca-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="776ca-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="776ca-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="776ca-133">-WorkspaceObject</span></span>
<span data-ttu-id="776ca-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="776ca-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="776ca-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="776ca-135">-Confirm</span></span>
<span data-ttu-id="776ca-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="776ca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="776ca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="776ca-137">-WhatIf</span></span>
<span data-ttu-id="776ca-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="776ca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="776ca-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="776ca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="776ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776ca-140">CommonParameters</span></span>
<span data-ttu-id="776ca-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="776ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776ca-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="776ca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776ca-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="776ca-143">INPUTS</span></span>

### <span data-ttu-id="776ca-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="776ca-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="776ca-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="776ca-145">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="776ca-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="776ca-146">OUTPUTS</span></span>

### <span data-ttu-id="776ca-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="776ca-147">System.Boolean</span></span>

## <span data-ttu-id="776ca-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="776ca-148">NOTES</span></span>

## <span data-ttu-id="776ca-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="776ca-149">RELATED LINKS</span></span>
