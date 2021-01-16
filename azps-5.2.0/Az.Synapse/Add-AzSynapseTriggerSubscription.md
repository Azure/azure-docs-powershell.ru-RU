---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398799"
---
# <span data-ttu-id="23bae-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="23bae-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="23bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23bae-102">SYNOPSIS</span></span>
<span data-ttu-id="23bae-103">Подпишитесь на триггер события внешней службы.</span><span class="sxs-lookup"><span data-stu-id="23bae-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="23bae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23bae-104">SYNTAX</span></span>

### <span data-ttu-id="23bae-105">AddByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23bae-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23bae-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="23bae-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23bae-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="23bae-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23bae-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23bae-108">DESCRIPTION</span></span>
<span data-ttu-id="23bae-109">Cmdlet **Add-AzSynapseTriggerSubscription** подписывает триггер события на указанные события внешней службы из триггера.</span><span class="sxs-lookup"><span data-stu-id="23bae-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="23bae-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23bae-110">EXAMPLES</span></span>

### <span data-ttu-id="23bae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23bae-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="23bae-112">Эта команда подписывает триггер ContosoTrigger на указанные события из ветвях триггера.</span><span class="sxs-lookup"><span data-stu-id="23bae-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="23bae-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="23bae-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="23bae-114">Эта команда подписывает триггер ContosoTrigger на указанные события из триггера в канале в канале.</span><span class="sxs-lookup"><span data-stu-id="23bae-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="23bae-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="23bae-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="23bae-116">Эта команда подписывает триггер ContosoTrigger на указанные события из триггера в канале ветвь.</span><span class="sxs-lookup"><span data-stu-id="23bae-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="23bae-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23bae-117">PARAMETERS</span></span>

### <span data-ttu-id="23bae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23bae-118">-AsJob</span></span>
<span data-ttu-id="23bae-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="23bae-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23bae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23bae-120">-DefaultProfile</span></span>
<span data-ttu-id="23bae-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23bae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23bae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23bae-122">-InputObject</span></span>
<span data-ttu-id="23bae-123">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="23bae-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23bae-124">-Name</span><span class="sxs-lookup"><span data-stu-id="23bae-124">-Name</span></span>
<span data-ttu-id="23bae-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="23bae-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23bae-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23bae-126">-WorkspaceName</span></span>
<span data-ttu-id="23bae-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="23bae-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23bae-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="23bae-128">-WorkspaceObject</span></span>
<span data-ttu-id="23bae-129">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="23bae-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23bae-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23bae-130">-Confirm</span></span>
<span data-ttu-id="23bae-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="23bae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23bae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23bae-132">-WhatIf</span></span>
<span data-ttu-id="23bae-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23bae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23bae-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23bae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23bae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23bae-135">CommonParameters</span></span>
<span data-ttu-id="23bae-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23bae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23bae-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23bae-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23bae-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23bae-138">INPUTS</span></span>

### <span data-ttu-id="23bae-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="23bae-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="23bae-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="23bae-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="23bae-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23bae-141">OUTPUTS</span></span>

### <span data-ttu-id="23bae-142">System.Object</span><span class="sxs-lookup"><span data-stu-id="23bae-142">System.Object</span></span>
## <span data-ttu-id="23bae-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23bae-143">NOTES</span></span>

## <span data-ttu-id="23bae-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23bae-144">RELATED LINKS</span></span>
