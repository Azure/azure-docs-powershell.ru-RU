---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318191"
---
# <span data-ttu-id="bd3f1-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="bd3f1-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="bd3f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bd3f1-103">Создание триггера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="bd3f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd3f1-104">SYNTAX</span></span>

### <span data-ttu-id="bd3f1-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd3f1-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd3f1-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="bd3f1-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd3f1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd3f1-107">DESCRIPTION</span></span>
<span data-ttu-id="bd3f1-108">Командлет **Set-AzSynapseTrigger** создает триггер в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="bd3f1-109">Триггеры создаются в состоянии "остановлено", что означает, что они сразу же не начинают вызывать конвейеры, на которые они ссылаются.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="bd3f1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd3f1-110">EXAMPLES</span></span>

### <span data-ttu-id="bd3f1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd3f1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="bd3f1-112">Создайте новый триггер с именем ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="bd3f1-113">Триггер создается в состоянии "остановлено", что означает, что оно не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="bd3f1-114">Триггер может быть запущен с помощью `Start-AzDataFactoryV2Trigger` командлета.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="bd3f1-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd3f1-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="bd3f1-116">Создайте новый триггер с именем ContosoTrigger в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="bd3f1-117">Триггер создается в состоянии "остановлено", что означает, что оно не запускается сразу.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="bd3f1-118">Триггер может быть запущен с помощью `Start-AzDataFactoryV2Trigger` командлета.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="bd3f1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd3f1-119">PARAMETERS</span></span>

### <span data-ttu-id="bd3f1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd3f1-120">-AsJob</span></span>
<span data-ttu-id="bd3f1-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd3f1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd3f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd3f1-122">-DefaultProfile</span></span>
<span data-ttu-id="bd3f1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd3f1-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="bd3f1-124">-DefinitionFile</span></span>
<span data-ttu-id="bd3f1-125">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-125">The JSON file path.</span></span>

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

### <span data-ttu-id="bd3f1-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd3f1-126">-Name</span></span>
<span data-ttu-id="bd3f1-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-127">The trigger name.</span></span>

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

### <span data-ttu-id="bd3f1-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd3f1-128">-WorkspaceName</span></span>
<span data-ttu-id="bd3f1-129">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bd3f1-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bd3f1-130">-WorkspaceObject</span></span>
<span data-ttu-id="bd3f1-131">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bd3f1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd3f1-132">-Confirm</span></span>
<span data-ttu-id="bd3f1-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd3f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd3f1-134">-WhatIf</span></span>
<span data-ttu-id="bd3f1-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd3f1-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd3f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd3f1-137">CommonParameters</span></span>
<span data-ttu-id="bd3f1-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd3f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd3f1-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd3f1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd3f1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd3f1-140">INPUTS</span></span>

### <span data-ttu-id="bd3f1-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd3f1-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bd3f1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd3f1-142">OUTPUTS</span></span>

### <span data-ttu-id="bd3f1-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="bd3f1-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="bd3f1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd3f1-144">NOTES</span></span>

## <span data-ttu-id="bd3f1-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd3f1-145">RELATED LINKS</span></span>
