---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236955"
---
# <span data-ttu-id="2899e-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="2899e-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="2899e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2899e-102">SYNOPSIS</span></span>
<span data-ttu-id="2899e-103">Запускает триггер в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2899e-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="2899e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2899e-104">SYNTAX</span></span>

### <span data-ttu-id="2899e-105">StartByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2899e-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2899e-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="2899e-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2899e-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="2899e-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2899e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2899e-108">DESCRIPTION</span></span>
<span data-ttu-id="2899e-109">Командлет **Start-AzSynapseTrigger** запускает триггер в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2899e-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="2899e-110">Если триггер находится в состоянии "остановлено", командлет запускает триггер и в конечном итоге вызывает конвейеры на основе его определения.</span><span class="sxs-lookup"><span data-stu-id="2899e-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="2899e-111">Если триггер уже находится в состоянии "начато", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="2899e-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="2899e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2899e-112">EXAMPLES</span></span>

### <span data-ttu-id="2899e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2899e-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="2899e-114">Запускает триггер с именем ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2899e-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2899e-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2899e-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="2899e-116">Запускает триггер с именем ContosoTrigger в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="2899e-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="2899e-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2899e-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="2899e-118">Запускает триггер с именем ContosoTrigger в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="2899e-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2899e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2899e-119">PARAMETERS</span></span>

### <span data-ttu-id="2899e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2899e-120">-AsJob</span></span>
<span data-ttu-id="2899e-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2899e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2899e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2899e-122">-DefaultProfile</span></span>
<span data-ttu-id="2899e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2899e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2899e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2899e-124">-InputObject</span></span>
<span data-ttu-id="2899e-125">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="2899e-125">The trigger object.</span></span>

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

### <span data-ttu-id="2899e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2899e-126">-Name</span></span>
<span data-ttu-id="2899e-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="2899e-127">The trigger name.</span></span>

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

### <span data-ttu-id="2899e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2899e-128">-PassThru</span></span>
<span data-ttu-id="2899e-129">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2899e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2899e-130">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="2899e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2899e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2899e-131">-WorkspaceName</span></span>
<span data-ttu-id="2899e-132">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2899e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2899e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2899e-133">-WorkspaceObject</span></span>
<span data-ttu-id="2899e-134">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="2899e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2899e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2899e-135">-Confirm</span></span>
<span data-ttu-id="2899e-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2899e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2899e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2899e-137">-WhatIf</span></span>
<span data-ttu-id="2899e-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2899e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2899e-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2899e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2899e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2899e-140">CommonParameters</span></span>
<span data-ttu-id="2899e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2899e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2899e-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2899e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2899e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2899e-143">INPUTS</span></span>

### <span data-ttu-id="2899e-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2899e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2899e-145">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="2899e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="2899e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2899e-146">OUTPUTS</span></span>

### <span data-ttu-id="2899e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2899e-147">System.Boolean</span></span>

## <span data-ttu-id="2899e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2899e-148">NOTES</span></span>

## <span data-ttu-id="2899e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2899e-149">RELATED LINKS</span></span>
