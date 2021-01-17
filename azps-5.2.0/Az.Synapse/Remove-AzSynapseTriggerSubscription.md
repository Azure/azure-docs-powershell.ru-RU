---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ac0606b73145a0d72a5776ede00a24bb802642e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401839"
---
# <span data-ttu-id="3e672-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="3e672-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="3e672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e672-102">SYNOPSIS</span></span>
<span data-ttu-id="3e672-103">Отписать триггер событий для событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="3e672-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="3e672-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e672-104">SYNTAX</span></span>

### <span data-ttu-id="3e672-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e672-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e672-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3e672-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e672-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e672-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e672-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e672-108">DESCRIPTION</span></span>
<span data-ttu-id="3e672-109">Для **этого с** его триггера будут отписаны указанные события внешней службы.</span><span class="sxs-lookup"><span data-stu-id="3e672-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="3e672-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e672-110">EXAMPLES</span></span>

### <span data-ttu-id="3e672-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e672-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="3e672-112">Эта команда отпишет триггер ContosoTrigger на указанные события из ветвях триггера.</span><span class="sxs-lookup"><span data-stu-id="3e672-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="3e672-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3e672-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="3e672-114">Эта команда отпишет триггер ContosoTrigger на указанные события из триггера в канале связи.</span><span class="sxs-lookup"><span data-stu-id="3e672-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="3e672-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3e672-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="3e672-116">Эта команда отпишет триггер ContosoTrigger на указанные события из триггера в канале связи.</span><span class="sxs-lookup"><span data-stu-id="3e672-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="3e672-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e672-117">PARAMETERS</span></span>

### <span data-ttu-id="3e672-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e672-118">-AsJob</span></span>
<span data-ttu-id="3e672-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3e672-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e672-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e672-120">-DefaultProfile</span></span>
<span data-ttu-id="3e672-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e672-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e672-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3e672-122">-Force</span></span>
<span data-ttu-id="3e672-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3e672-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e672-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e672-124">-InputObject</span></span>
<span data-ttu-id="3e672-125">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="3e672-125">The trigger object.</span></span>

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

### <span data-ttu-id="3e672-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3e672-126">-Name</span></span>
<span data-ttu-id="3e672-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="3e672-127">The trigger name.</span></span>

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

### <span data-ttu-id="3e672-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e672-128">-PassThru</span></span>
<span data-ttu-id="3e672-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e672-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3e672-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="3e672-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3e672-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e672-131">-WorkspaceName</span></span>
<span data-ttu-id="3e672-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="3e672-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3e672-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e672-133">-WorkspaceObject</span></span>
<span data-ttu-id="3e672-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="3e672-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3e672-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e672-135">-Confirm</span></span>
<span data-ttu-id="3e672-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e672-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e672-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e672-137">-WhatIf</span></span>
<span data-ttu-id="3e672-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e672-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e672-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3e672-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e672-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e672-140">CommonParameters</span></span>
<span data-ttu-id="3e672-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e672-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e672-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e672-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e672-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e672-143">INPUTS</span></span>

### <span data-ttu-id="3e672-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e672-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3e672-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="3e672-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="3e672-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e672-146">OUTPUTS</span></span>

### <span data-ttu-id="3e672-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e672-147">System.Boolean</span></span>

## <span data-ttu-id="3e672-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e672-148">NOTES</span></span>

## <span data-ttu-id="3e672-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e672-149">RELATED LINKS</span></span>
