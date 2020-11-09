---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243465"
---
# <span data-ttu-id="cb323-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="cb323-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="cb323-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb323-102">SYNOPSIS</span></span>
<span data-ttu-id="cb323-103">Удаление триггера из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb323-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="cb323-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb323-104">SYNTAX</span></span>

### <span data-ttu-id="cb323-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb323-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb323-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="cb323-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb323-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="cb323-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb323-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb323-108">DESCRIPTION</span></span>
<span data-ttu-id="cb323-109">Командлет **Remove-AzSynapseTrigger** удаляет триггер из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb323-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="cb323-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb323-110">EXAMPLES</span></span>

### <span data-ttu-id="cb323-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb323-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="cb323-112">Удалите триггер с именем ContosoTrigger из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb323-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cb323-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb323-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="cb323-114">Удалите триггер с именем ContosoTrigger из рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb323-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="cb323-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cb323-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="cb323-116">Удалите триггер с именем ContosoTrigger из рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb323-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cb323-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb323-117">PARAMETERS</span></span>

### <span data-ttu-id="cb323-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb323-118">-AsJob</span></span>
<span data-ttu-id="cb323-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cb323-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb323-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb323-120">-DefaultProfile</span></span>
<span data-ttu-id="cb323-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb323-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb323-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb323-122">-InputObject</span></span>
<span data-ttu-id="cb323-123">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="cb323-123">The trigger object.</span></span>

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

### <span data-ttu-id="cb323-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb323-124">-Name</span></span>
<span data-ttu-id="cb323-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="cb323-125">The trigger name.</span></span>

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

### <span data-ttu-id="cb323-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb323-126">-PassThru</span></span>
<span data-ttu-id="cb323-127">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb323-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cb323-128">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="cb323-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cb323-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb323-129">-WorkspaceName</span></span>
<span data-ttu-id="cb323-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb323-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cb323-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cb323-131">-WorkspaceObject</span></span>
<span data-ttu-id="cb323-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cb323-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cb323-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb323-133">-Confirm</span></span>
<span data-ttu-id="cb323-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb323-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb323-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb323-135">-WhatIf</span></span>
<span data-ttu-id="cb323-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb323-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb323-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb323-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb323-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb323-138">CommonParameters</span></span>
<span data-ttu-id="cb323-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb323-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb323-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb323-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb323-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb323-141">INPUTS</span></span>

### <span data-ttu-id="cb323-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cb323-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="cb323-143">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="cb323-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="cb323-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb323-144">OUTPUTS</span></span>

### <span data-ttu-id="cb323-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb323-145">System.Boolean</span></span>

## <span data-ttu-id="cb323-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb323-146">NOTES</span></span>

## <span data-ttu-id="cb323-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb323-147">RELATED LINKS</span></span>