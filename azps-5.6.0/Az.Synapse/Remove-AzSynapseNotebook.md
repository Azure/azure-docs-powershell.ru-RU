---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 6203143eb2d386b627d0208730987709b1dd68c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983944"
---
# <span data-ttu-id="afb99-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="afb99-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="afb99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb99-102">SYNOPSIS</span></span>
<span data-ttu-id="afb99-103">Удаляет записную книжку из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="afb99-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="afb99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afb99-104">SYNTAX</span></span>

### <span data-ttu-id="afb99-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="afb99-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb99-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="afb99-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb99-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="afb99-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afb99-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb99-108">DESCRIPTION</span></span>
<span data-ttu-id="afb99-109">При этом из **рабочей** области удаляется записная книжка.</span><span class="sxs-lookup"><span data-stu-id="afb99-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="afb99-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afb99-110">EXAMPLES</span></span>

### <span data-ttu-id="afb99-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afb99-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="afb99-112">Удалите записную книжку ContosoNotebook из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="afb99-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="afb99-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="afb99-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="afb99-114">Удалите записную книжку ContosoNotebook из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="afb99-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="afb99-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="afb99-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="afb99-116">Удалите записную книжку ContosoNotebook из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="afb99-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="afb99-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb99-117">PARAMETERS</span></span>

### <span data-ttu-id="afb99-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afb99-118">-AsJob</span></span>
<span data-ttu-id="afb99-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="afb99-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afb99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb99-120">-DefaultProfile</span></span>
<span data-ttu-id="afb99-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afb99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb99-122">-Force</span><span class="sxs-lookup"><span data-stu-id="afb99-122">-Force</span></span>
<span data-ttu-id="afb99-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="afb99-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="afb99-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afb99-124">-InputObject</span></span>
<span data-ttu-id="afb99-125">Объект записной книжки.</span><span class="sxs-lookup"><span data-stu-id="afb99-125">The notebook object.</span></span>

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

### <span data-ttu-id="afb99-126">-Name</span><span class="sxs-lookup"><span data-stu-id="afb99-126">-Name</span></span>
<span data-ttu-id="afb99-127">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="afb99-127">The notebook name.</span></span>

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

### <span data-ttu-id="afb99-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afb99-128">-PassThru</span></span>
<span data-ttu-id="afb99-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="afb99-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="afb99-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="afb99-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="afb99-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="afb99-131">-WorkspaceName</span></span>
<span data-ttu-id="afb99-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="afb99-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="afb99-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="afb99-133">-WorkspaceObject</span></span>
<span data-ttu-id="afb99-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="afb99-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="afb99-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afb99-135">-Confirm</span></span>
<span data-ttu-id="afb99-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="afb99-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb99-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb99-137">-WhatIf</span></span>
<span data-ttu-id="afb99-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb99-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afb99-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="afb99-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb99-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb99-140">CommonParameters</span></span>
<span data-ttu-id="afb99-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb99-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb99-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afb99-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb99-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afb99-143">INPUTS</span></span>

### <span data-ttu-id="afb99-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="afb99-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="afb99-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="afb99-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="afb99-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afb99-146">OUTPUTS</span></span>

### <span data-ttu-id="afb99-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="afb99-147">System.Boolean</span></span>

## <span data-ttu-id="afb99-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afb99-148">NOTES</span></span>

## <span data-ttu-id="afb99-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afb99-149">RELATED LINKS</span></span>
