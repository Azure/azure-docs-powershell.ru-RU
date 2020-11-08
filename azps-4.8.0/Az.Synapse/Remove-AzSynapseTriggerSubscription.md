---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236959"
---
# <span data-ttu-id="859ff-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="859ff-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="859ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="859ff-102">SYNOPSIS</span></span>
<span data-ttu-id="859ff-103">Отменяйте подписку триггера события на внешние события службы.</span><span class="sxs-lookup"><span data-stu-id="859ff-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="859ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="859ff-104">SYNTAX</span></span>

### <span data-ttu-id="859ff-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="859ff-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859ff-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="859ff-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859ff-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="859ff-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859ff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="859ff-108">DESCRIPTION</span></span>
<span data-ttu-id="859ff-109">Командлет **Remove-AzSynapseTriggerSubscription** отменяет подписку триггера событий на указанные внешние события службы из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="859ff-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="859ff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="859ff-110">EXAMPLES</span></span>

### <span data-ttu-id="859ff-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="859ff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="859ff-112">Эта команда отменяет подписку триггера с именем ContosoTrigger на указанные события из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="859ff-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="859ff-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="859ff-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="859ff-114">Эта команда отменяет подписку триггера с именем ContosoTrigger на указанные события из определения триггера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="859ff-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="859ff-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="859ff-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="859ff-116">Эта команда отменяет подписку триггера с именем ContosoTrigger на указанные события из определения триггера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="859ff-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="859ff-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="859ff-117">PARAMETERS</span></span>

### <span data-ttu-id="859ff-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="859ff-118">-AsJob</span></span>
<span data-ttu-id="859ff-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="859ff-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="859ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859ff-120">-DefaultProfile</span></span>
<span data-ttu-id="859ff-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="859ff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="859ff-122">-InputObject</span></span>
<span data-ttu-id="859ff-123">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="859ff-123">The trigger object.</span></span>

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

### <span data-ttu-id="859ff-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="859ff-124">-Name</span></span>
<span data-ttu-id="859ff-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="859ff-125">The trigger name.</span></span>

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

### <span data-ttu-id="859ff-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="859ff-126">-PassThru</span></span>
<span data-ttu-id="859ff-127">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="859ff-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="859ff-128">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="859ff-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="859ff-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="859ff-129">-WorkspaceName</span></span>
<span data-ttu-id="859ff-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="859ff-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="859ff-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="859ff-131">-WorkspaceObject</span></span>
<span data-ttu-id="859ff-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="859ff-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="859ff-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="859ff-133">-Confirm</span></span>
<span data-ttu-id="859ff-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="859ff-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859ff-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859ff-135">-WhatIf</span></span>
<span data-ttu-id="859ff-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="859ff-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="859ff-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="859ff-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859ff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859ff-138">CommonParameters</span></span>
<span data-ttu-id="859ff-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="859ff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859ff-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="859ff-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859ff-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="859ff-141">INPUTS</span></span>

### <span data-ttu-id="859ff-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="859ff-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="859ff-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="859ff-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="859ff-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="859ff-144">OUTPUTS</span></span>

### <span data-ttu-id="859ff-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="859ff-145">System.Boolean</span></span>

## <span data-ttu-id="859ff-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="859ff-146">NOTES</span></span>

## <span data-ttu-id="859ff-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="859ff-147">RELATED LINKS</span></span>
