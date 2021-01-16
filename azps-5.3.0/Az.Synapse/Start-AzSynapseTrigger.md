---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507926"
---
# <span data-ttu-id="d609b-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="d609b-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="d609b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d609b-102">SYNOPSIS</span></span>
<span data-ttu-id="d609b-103">Запуск триггера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d609b-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="d609b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d609b-104">SYNTAX</span></span>

### <span data-ttu-id="d609b-105">StartByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d609b-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d609b-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="d609b-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d609b-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="d609b-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d609b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d609b-108">DESCRIPTION</span></span>
<span data-ttu-id="d609b-109">Для **запуска триггера Start-AzSynapseTrigger** в рабочей области запускается триггер.</span><span class="sxs-lookup"><span data-stu-id="d609b-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="d609b-110">Если триггер находится в состоянии "Остановлено", запускается триггер и в конечном итоге запускается конвейеры на основе его определения.</span><span class="sxs-lookup"><span data-stu-id="d609b-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="d609b-111">Если триггер уже находится в состоянии "Запущено", этот cmdlet не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="d609b-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="d609b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d609b-112">EXAMPLES</span></span>

### <span data-ttu-id="d609b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d609b-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="d609b-114">Запуск триггера ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d609b-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d609b-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d609b-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="d609b-116">Запуск триггера ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="d609b-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d609b-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d609b-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="d609b-118">Запуск триггера ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="d609b-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d609b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d609b-119">PARAMETERS</span></span>

### <span data-ttu-id="d609b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d609b-120">-AsJob</span></span>
<span data-ttu-id="d609b-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d609b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d609b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d609b-122">-DefaultProfile</span></span>
<span data-ttu-id="d609b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d609b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d609b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d609b-124">-InputObject</span></span>
<span data-ttu-id="d609b-125">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="d609b-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d609b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d609b-126">-Name</span></span>
<span data-ttu-id="d609b-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="d609b-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d609b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d609b-128">-PassThru</span></span>
<span data-ttu-id="d609b-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d609b-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d609b-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="d609b-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d609b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d609b-131">-WorkspaceName</span></span>
<span data-ttu-id="d609b-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d609b-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d609b-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d609b-133">-WorkspaceObject</span></span>
<span data-ttu-id="d609b-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d609b-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d609b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d609b-135">-Confirm</span></span>
<span data-ttu-id="d609b-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d609b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d609b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d609b-137">-WhatIf</span></span>
<span data-ttu-id="d609b-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d609b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d609b-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d609b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d609b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d609b-140">CommonParameters</span></span>
<span data-ttu-id="d609b-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d609b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d609b-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d609b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d609b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d609b-143">INPUTS</span></span>

### <span data-ttu-id="d609b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d609b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d609b-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="d609b-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="d609b-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d609b-146">OUTPUTS</span></span>

### <span data-ttu-id="d609b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d609b-147">System.Boolean</span></span>

## <span data-ttu-id="d609b-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d609b-148">NOTES</span></span>

## <span data-ttu-id="d609b-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d609b-149">RELATED LINKS</span></span>
