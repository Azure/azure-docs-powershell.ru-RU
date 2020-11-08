---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236501"
---
# <span data-ttu-id="261cf-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="261cf-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="261cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="261cf-102">SYNOPSIS</span></span>
<span data-ttu-id="261cf-103">Подписка триггера события на внешние события службы.</span><span class="sxs-lookup"><span data-stu-id="261cf-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="261cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="261cf-104">SYNTAX</span></span>

### <span data-ttu-id="261cf-105">AddByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="261cf-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261cf-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="261cf-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="261cf-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="261cf-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="261cf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="261cf-108">DESCRIPTION</span></span>
<span data-ttu-id="261cf-109">Командлет **Add-AzSynapseTriggerSubscription** подписывает триггер событий на указанные внешние события службы из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="261cf-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="261cf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="261cf-110">EXAMPLES</span></span>

### <span data-ttu-id="261cf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="261cf-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="261cf-112">Эта команда подписала триггер с именем ContosoTrigger к указанным событиям из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="261cf-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="261cf-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="261cf-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="261cf-114">Эта команда подписала триггер, именуемый ContosoTrigger, с указанными событиями из определения триггера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="261cf-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="261cf-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="261cf-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="261cf-116">Эта команда подписала триггер, именуемый ContosoTrigger, с указанными событиями из определения триггера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="261cf-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="261cf-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="261cf-117">PARAMETERS</span></span>

### <span data-ttu-id="261cf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="261cf-118">-AsJob</span></span>
<span data-ttu-id="261cf-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="261cf-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="261cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261cf-120">-DefaultProfile</span></span>
<span data-ttu-id="261cf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="261cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="261cf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="261cf-122">-InputObject</span></span>
<span data-ttu-id="261cf-123">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="261cf-123">The trigger object.</span></span>

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

### <span data-ttu-id="261cf-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="261cf-124">-Name</span></span>
<span data-ttu-id="261cf-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="261cf-125">The trigger name.</span></span>

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

### <span data-ttu-id="261cf-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="261cf-126">-WorkspaceName</span></span>
<span data-ttu-id="261cf-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="261cf-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="261cf-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="261cf-128">-WorkspaceObject</span></span>
<span data-ttu-id="261cf-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="261cf-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="261cf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="261cf-130">-Confirm</span></span>
<span data-ttu-id="261cf-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="261cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="261cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="261cf-132">-WhatIf</span></span>
<span data-ttu-id="261cf-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="261cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="261cf-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="261cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="261cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261cf-135">CommonParameters</span></span>
<span data-ttu-id="261cf-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="261cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261cf-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="261cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261cf-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="261cf-138">INPUTS</span></span>

### <span data-ttu-id="261cf-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="261cf-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="261cf-140">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="261cf-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="261cf-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="261cf-141">OUTPUTS</span></span>

### <span data-ttu-id="261cf-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="261cf-142">System.Object</span></span>
## <span data-ttu-id="261cf-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="261cf-143">NOTES</span></span>

## <span data-ttu-id="261cf-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="261cf-144">RELATED LINKS</span></span>
