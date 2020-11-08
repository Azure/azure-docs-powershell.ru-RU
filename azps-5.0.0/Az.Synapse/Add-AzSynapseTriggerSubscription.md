---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247965"
---
# <span data-ttu-id="90483-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="90483-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="90483-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90483-102">SYNOPSIS</span></span>
<span data-ttu-id="90483-103">Подписка триггера события на внешние события службы.</span><span class="sxs-lookup"><span data-stu-id="90483-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="90483-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90483-104">SYNTAX</span></span>

### <span data-ttu-id="90483-105">AddByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90483-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90483-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="90483-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90483-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="90483-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90483-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90483-108">DESCRIPTION</span></span>
<span data-ttu-id="90483-109">Командлет **Add-AzSynapseTriggerSubscription** подписывает триггер событий на указанные внешние события службы из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="90483-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="90483-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90483-110">EXAMPLES</span></span>

### <span data-ttu-id="90483-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90483-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="90483-112">Эта команда подписала триггер с именем ContosoTrigger к указанным событиям из определения триггера.</span><span class="sxs-lookup"><span data-stu-id="90483-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="90483-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="90483-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="90483-114">Эта команда подписала триггер, именуемый ContosoTrigger, с указанными событиями из определения триггера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="90483-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="90483-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="90483-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="90483-116">Эта команда подписала триггер, именуемый ContosoTrigger, с указанными событиями из определения триггера с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="90483-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="90483-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90483-117">PARAMETERS</span></span>

### <span data-ttu-id="90483-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90483-118">-AsJob</span></span>
<span data-ttu-id="90483-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="90483-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90483-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90483-120">-DefaultProfile</span></span>
<span data-ttu-id="90483-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90483-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90483-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90483-122">-InputObject</span></span>
<span data-ttu-id="90483-123">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="90483-123">The trigger object.</span></span>

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

### <span data-ttu-id="90483-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90483-124">-Name</span></span>
<span data-ttu-id="90483-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="90483-125">The trigger name.</span></span>

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

### <span data-ttu-id="90483-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="90483-126">-WorkspaceName</span></span>
<span data-ttu-id="90483-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="90483-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="90483-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="90483-128">-WorkspaceObject</span></span>
<span data-ttu-id="90483-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="90483-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="90483-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90483-130">-Confirm</span></span>
<span data-ttu-id="90483-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90483-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90483-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90483-132">-WhatIf</span></span>
<span data-ttu-id="90483-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90483-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90483-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90483-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90483-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90483-135">CommonParameters</span></span>
<span data-ttu-id="90483-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90483-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90483-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90483-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90483-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90483-138">INPUTS</span></span>

### <span data-ttu-id="90483-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="90483-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="90483-140">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="90483-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="90483-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90483-141">OUTPUTS</span></span>

### <span data-ttu-id="90483-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="90483-142">System.Object</span></span>
## <span data-ttu-id="90483-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="90483-143">NOTES</span></span>

## <span data-ttu-id="90483-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90483-144">RELATED LINKS</span></span>
