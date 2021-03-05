---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: f331cad857fba20d72ffdd34f84f70a5d6392bff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002131"
---
# <span data-ttu-id="ea52b-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="ea52b-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="ea52b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea52b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea52b-103">Отписать триггер события к событиям внешней службы.</span><span class="sxs-lookup"><span data-stu-id="ea52b-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="ea52b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea52b-104">SYNTAX</span></span>

### <span data-ttu-id="ea52b-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea52b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea52b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ea52b-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea52b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea52b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea52b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea52b-108">DESCRIPTION</span></span>
<span data-ttu-id="ea52b-109">Для **этого с** его триггера будут отписаны указанные события внешней службы.</span><span class="sxs-lookup"><span data-stu-id="ea52b-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="ea52b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea52b-110">EXAMPLES</span></span>

### <span data-ttu-id="ea52b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea52b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="ea52b-112">Эта команда отпишет триггер ContosoTrigger на указанные события из триггера в именах.</span><span class="sxs-lookup"><span data-stu-id="ea52b-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="ea52b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea52b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="ea52b-114">Эта команда отпишет триггер ContosoTrigger на указанные события из триггера в канале связи.</span><span class="sxs-lookup"><span data-stu-id="ea52b-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="ea52b-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ea52b-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="ea52b-116">Эта команда отпишет триггер ContosoTrigger на указанные события из триггера в канале связи.</span><span class="sxs-lookup"><span data-stu-id="ea52b-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="ea52b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea52b-117">PARAMETERS</span></span>

### <span data-ttu-id="ea52b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea52b-118">-AsJob</span></span>
<span data-ttu-id="ea52b-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ea52b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea52b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea52b-120">-DefaultProfile</span></span>
<span data-ttu-id="ea52b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea52b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea52b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ea52b-122">-Force</span></span>
<span data-ttu-id="ea52b-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ea52b-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ea52b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea52b-124">-InputObject</span></span>
<span data-ttu-id="ea52b-125">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="ea52b-125">The trigger object.</span></span>

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

### <span data-ttu-id="ea52b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ea52b-126">-Name</span></span>
<span data-ttu-id="ea52b-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="ea52b-127">The trigger name.</span></span>

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

### <span data-ttu-id="ea52b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea52b-128">-PassThru</span></span>
<span data-ttu-id="ea52b-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea52b-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ea52b-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="ea52b-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ea52b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea52b-131">-WorkspaceName</span></span>
<span data-ttu-id="ea52b-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="ea52b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ea52b-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ea52b-133">-WorkspaceObject</span></span>
<span data-ttu-id="ea52b-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ea52b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea52b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea52b-135">-Confirm</span></span>
<span data-ttu-id="ea52b-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ea52b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea52b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea52b-137">-WhatIf</span></span>
<span data-ttu-id="ea52b-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea52b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea52b-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea52b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea52b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea52b-140">CommonParameters</span></span>
<span data-ttu-id="ea52b-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea52b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea52b-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea52b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea52b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea52b-143">INPUTS</span></span>

### <span data-ttu-id="ea52b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea52b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ea52b-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="ea52b-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ea52b-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea52b-146">OUTPUTS</span></span>

### <span data-ttu-id="ea52b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea52b-147">System.Boolean</span></span>

## <span data-ttu-id="ea52b-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea52b-148">NOTES</span></span>

## <span data-ttu-id="ea52b-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea52b-149">RELATED LINKS</span></span>
