---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247928"
---
# <span data-ttu-id="3a911-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="3a911-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="3a911-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a911-102">SYNOPSIS</span></span>
<span data-ttu-id="3a911-103">Удаление записной книжки из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3a911-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="3a911-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a911-104">SYNTAX</span></span>

### <span data-ttu-id="3a911-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a911-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a911-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="3a911-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a911-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a911-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a911-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a911-108">DESCRIPTION</span></span>
<span data-ttu-id="3a911-109">Командлет **Remove-AzSynapseNotebook** удаляет записную книжку из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3a911-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="3a911-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a911-110">EXAMPLES</span></span>

### <span data-ttu-id="3a911-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a911-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="3a911-112">Удаление записной книжки с именем ContosoNotebook из ContosoWorkspace рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3a911-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="3a911-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a911-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="3a911-114">Удаление записной книжки с именем ContosoNotebook из рабочей области ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3a911-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="3a911-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3a911-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="3a911-116">Удаление записной книжки с именем ContosoNotebook из рабочей области ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3a911-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3a911-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a911-117">PARAMETERS</span></span>

### <span data-ttu-id="3a911-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a911-118">-AsJob</span></span>
<span data-ttu-id="3a911-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a911-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a911-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a911-120">-DefaultProfile</span></span>
<span data-ttu-id="3a911-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a911-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a911-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a911-122">-InputObject</span></span>
<span data-ttu-id="3a911-123">Объект записной книжки.</span><span class="sxs-lookup"><span data-stu-id="3a911-123">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a911-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a911-124">-Name</span></span>
<span data-ttu-id="3a911-125">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="3a911-125">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a911-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a911-126">-PassThru</span></span>
<span data-ttu-id="3a911-127">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a911-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3a911-128">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="3a911-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3a911-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a911-129">-WorkspaceName</span></span>
<span data-ttu-id="3a911-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3a911-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a911-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a911-131">-WorkspaceObject</span></span>
<span data-ttu-id="3a911-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3a911-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a911-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a911-133">-Confirm</span></span>
<span data-ttu-id="3a911-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a911-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a911-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a911-135">-WhatIf</span></span>
<span data-ttu-id="3a911-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a911-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a911-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a911-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a911-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a911-138">CommonParameters</span></span>
<span data-ttu-id="3a911-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a911-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a911-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a911-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a911-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a911-141">INPUTS</span></span>

### <span data-ttu-id="3a911-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a911-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3a911-143">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="3a911-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="3a911-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a911-144">OUTPUTS</span></span>

### <span data-ttu-id="3a911-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a911-145">System.Boolean</span></span>

## <span data-ttu-id="3a911-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a911-146">NOTES</span></span>

## <span data-ttu-id="3a911-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a911-147">RELATED LINKS</span></span>
