---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 23bd6186f31199ab9387df5ee78ce3fdbe89032e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413647"
---
# <span data-ttu-id="f2c22-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="f2c22-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="f2c22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2c22-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c22-103">Удаляет записную книжку из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f2c22-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="f2c22-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2c22-104">SYNTAX</span></span>

### <span data-ttu-id="f2c22-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2c22-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2c22-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="f2c22-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2c22-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2c22-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2c22-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2c22-108">DESCRIPTION</span></span>
<span data-ttu-id="f2c22-109">При этом из **рабочей** области удаляется записная книжка.</span><span class="sxs-lookup"><span data-stu-id="f2c22-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="f2c22-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2c22-110">EXAMPLES</span></span>

### <span data-ttu-id="f2c22-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2c22-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="f2c22-112">Удалите записную книжку ContosoNotebook из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f2c22-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f2c22-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f2c22-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="f2c22-114">Удалите записную книжку ContosoNotebook из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="f2c22-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="f2c22-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f2c22-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="f2c22-116">Удалите записную книжку ContosoNotebook из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="f2c22-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f2c22-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2c22-117">PARAMETERS</span></span>

### <span data-ttu-id="f2c22-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2c22-118">-AsJob</span></span>
<span data-ttu-id="f2c22-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f2c22-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2c22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c22-120">-DefaultProfile</span></span>
<span data-ttu-id="f2c22-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2c22-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2c22-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f2c22-122">-Force</span></span>
<span data-ttu-id="f2c22-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f2c22-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2c22-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2c22-124">-InputObject</span></span>
<span data-ttu-id="f2c22-125">Объект записной книжки.</span><span class="sxs-lookup"><span data-stu-id="f2c22-125">The notebook object.</span></span>

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

### <span data-ttu-id="f2c22-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f2c22-126">-Name</span></span>
<span data-ttu-id="f2c22-127">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="f2c22-127">The notebook name.</span></span>

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

### <span data-ttu-id="f2c22-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2c22-128">-PassThru</span></span>
<span data-ttu-id="f2c22-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2c22-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f2c22-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="f2c22-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f2c22-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f2c22-131">-WorkspaceName</span></span>
<span data-ttu-id="f2c22-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="f2c22-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f2c22-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f2c22-133">-WorkspaceObject</span></span>
<span data-ttu-id="f2c22-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f2c22-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f2c22-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2c22-135">-Confirm</span></span>
<span data-ttu-id="f2c22-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f2c22-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2c22-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2c22-137">-WhatIf</span></span>
<span data-ttu-id="f2c22-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2c22-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2c22-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f2c22-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2c22-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c22-140">CommonParameters</span></span>
<span data-ttu-id="f2c22-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2c22-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c22-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2c22-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c22-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2c22-143">INPUTS</span></span>

### <span data-ttu-id="f2c22-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f2c22-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f2c22-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="f2c22-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="f2c22-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2c22-146">OUTPUTS</span></span>

### <span data-ttu-id="f2c22-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2c22-147">System.Boolean</span></span>

## <span data-ttu-id="f2c22-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2c22-148">NOTES</span></span>

## <span data-ttu-id="f2c22-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2c22-149">RELATED LINKS</span></span>
