---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409895"
---
# <span data-ttu-id="e16c4-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="e16c4-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="e16c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e16c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e16c4-103">Создает триггер в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e16c4-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="e16c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e16c4-104">SYNTAX</span></span>

### <span data-ttu-id="e16c4-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e16c4-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e16c4-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="e16c4-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e16c4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e16c4-107">DESCRIPTION</span></span>
<span data-ttu-id="e16c4-108">Для создания триггера в рабочей области запускается **cmdlet Set-AzSynapseTrigger.**</span><span class="sxs-lookup"><span data-stu-id="e16c4-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="e16c4-109">Триггеры создаются в состоянии "Остановлено", то есть они не начинают прямо сейчас вызывать конвейеры, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="e16c4-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="e16c4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e16c4-110">EXAMPLES</span></span>

### <span data-ttu-id="e16c4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e16c4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="e16c4-112">Создайте новый триггер ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e16c4-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="e16c4-113">Триггер создается в состоянии "Остановлено", то есть он не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="e16c4-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="e16c4-114">С помощью этого триггера можно запускать `Start-AzDataFactoryV2Trigger` триггеры.</span><span class="sxs-lookup"><span data-stu-id="e16c4-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="e16c4-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e16c4-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="e16c4-116">Создайте новый триггер ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="e16c4-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="e16c4-117">Триггер создается в состоянии "Остановлено", то есть он не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="e16c4-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="e16c4-118">С помощью этого триггера можно запускать `Start-AzDataFactoryV2Trigger` триггеры.</span><span class="sxs-lookup"><span data-stu-id="e16c4-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="e16c4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e16c4-119">PARAMETERS</span></span>

### <span data-ttu-id="e16c4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e16c4-120">-AsJob</span></span>
<span data-ttu-id="e16c4-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e16c4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e16c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16c4-122">-DefaultProfile</span></span>
<span data-ttu-id="e16c4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e16c4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e16c4-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e16c4-124">-DefinitionFile</span></span>
<span data-ttu-id="e16c4-125">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="e16c4-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16c4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e16c4-126">-Name</span></span>
<span data-ttu-id="e16c4-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="e16c4-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16c4-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e16c4-128">-WorkspaceName</span></span>
<span data-ttu-id="e16c4-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="e16c4-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16c4-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e16c4-130">-WorkspaceObject</span></span>
<span data-ttu-id="e16c4-131">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="e16c4-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e16c4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e16c4-132">-Confirm</span></span>
<span data-ttu-id="e16c4-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e16c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e16c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e16c4-134">-WhatIf</span></span>
<span data-ttu-id="e16c4-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e16c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e16c4-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e16c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e16c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16c4-137">CommonParameters</span></span>
<span data-ttu-id="e16c4-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e16c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16c4-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e16c4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16c4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e16c4-140">INPUTS</span></span>

### <span data-ttu-id="e16c4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e16c4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e16c4-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e16c4-142">OUTPUTS</span></span>

### <span data-ttu-id="e16c4-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="e16c4-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="e16c4-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e16c4-144">NOTES</span></span>

## <span data-ttu-id="e16c4-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e16c4-145">RELATED LINKS</span></span>
