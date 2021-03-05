---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 171cb897d1e385056d391468cf31f3b361c39202
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959960"
---
# <span data-ttu-id="b59f0-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="b59f0-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="b59f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b59f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b59f0-103">Удаляет триггер из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b59f0-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="b59f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b59f0-104">SYNTAX</span></span>

### <span data-ttu-id="b59f0-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b59f0-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59f0-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="b59f0-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b59f0-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b59f0-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b59f0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b59f0-108">DESCRIPTION</span></span>
<span data-ttu-id="b59f0-109">Для удаления триггера из рабочей области запускается **cmdlet Remove-AzSynapseTrigger.**</span><span class="sxs-lookup"><span data-stu-id="b59f0-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="b59f0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b59f0-110">EXAMPLES</span></span>

### <span data-ttu-id="b59f0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b59f0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b59f0-112">Удалите триггер ContosoTrigger из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b59f0-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b59f0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b59f0-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="b59f0-114">Удалите триггер ContosoTrigger из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="b59f0-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="b59f0-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b59f0-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="b59f0-116">Удалите триггер ContosoTrigger из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="b59f0-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b59f0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b59f0-117">PARAMETERS</span></span>

### <span data-ttu-id="b59f0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b59f0-118">-AsJob</span></span>
<span data-ttu-id="b59f0-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b59f0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b59f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59f0-120">-DefaultProfile</span></span>
<span data-ttu-id="b59f0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b59f0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b59f0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b59f0-122">-Force</span></span>
<span data-ttu-id="b59f0-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b59f0-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b59f0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b59f0-124">-InputObject</span></span>
<span data-ttu-id="b59f0-125">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="b59f0-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b59f0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b59f0-126">-Name</span></span>
<span data-ttu-id="b59f0-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="b59f0-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59f0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b59f0-128">-PassThru</span></span>
<span data-ttu-id="b59f0-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b59f0-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b59f0-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="b59f0-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b59f0-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b59f0-131">-WorkspaceName</span></span>
<span data-ttu-id="b59f0-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="b59f0-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b59f0-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b59f0-133">-WorkspaceObject</span></span>
<span data-ttu-id="b59f0-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b59f0-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b59f0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b59f0-135">-Confirm</span></span>
<span data-ttu-id="b59f0-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b59f0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b59f0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b59f0-137">-WhatIf</span></span>
<span data-ttu-id="b59f0-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b59f0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b59f0-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b59f0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b59f0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59f0-140">CommonParameters</span></span>
<span data-ttu-id="b59f0-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59f0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59f0-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b59f0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59f0-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b59f0-143">INPUTS</span></span>

### <span data-ttu-id="b59f0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b59f0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b59f0-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b59f0-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b59f0-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b59f0-146">OUTPUTS</span></span>

### <span data-ttu-id="b59f0-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b59f0-147">System.Boolean</span></span>

## <span data-ttu-id="b59f0-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b59f0-148">NOTES</span></span>

## <span data-ttu-id="b59f0-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b59f0-149">RELATED LINKS</span></span>
