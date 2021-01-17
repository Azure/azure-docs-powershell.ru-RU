---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413644"
---
# <span data-ttu-id="a8ca2-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="a8ca2-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="a8ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ca2-103">Удаляет связанную службу из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="a8ca2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8ca2-104">SYNTAX</span></span>

### <span data-ttu-id="a8ca2-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8ca2-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ca2-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a8ca2-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ca2-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8ca2-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ca2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8ca2-108">DESCRIPTION</span></span>
<span data-ttu-id="a8ca2-109">При **этом связанная** служба удаляется из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="a8ca2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8ca2-110">EXAMPLES</span></span>

### <span data-ttu-id="a8ca2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8ca2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="a8ca2-112">Эта команда удаляет связанную службу с именем ContosoLinkedService из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a8ca2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a8ca2-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="a8ca2-114">Эта команда удаляет связанную службу с именем ContosoLinkedService из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a8ca2-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a8ca2-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="a8ca2-116">Эта команда удаляет связанную службу с именем ContosoLinkedService из рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a8ca2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8ca2-117">PARAMETERS</span></span>

### <span data-ttu-id="a8ca2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8ca2-118">-AsJob</span></span>
<span data-ttu-id="a8ca2-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a8ca2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8ca2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ca2-120">-DefaultProfile</span></span>
<span data-ttu-id="a8ca2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ca2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a8ca2-122">-Force</span></span>
<span data-ttu-id="a8ca2-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a8ca2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ca2-124">-InputObject</span></span>
<span data-ttu-id="a8ca2-125">Связанный объект службы.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ca2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a8ca2-126">-Name</span></span>
<span data-ttu-id="a8ca2-127">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ca2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ca2-128">-PassThru</span></span>
<span data-ttu-id="a8ca2-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a8ca2-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a8ca2-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a8ca2-131">-WorkspaceName</span></span>
<span data-ttu-id="a8ca2-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a8ca2-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a8ca2-133">-WorkspaceObject</span></span>
<span data-ttu-id="a8ca2-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a8ca2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8ca2-135">-Confirm</span></span>
<span data-ttu-id="a8ca2-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ca2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ca2-137">-WhatIf</span></span>
<span data-ttu-id="a8ca2-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8ca2-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ca2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ca2-140">CommonParameters</span></span>
<span data-ttu-id="a8ca2-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ca2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ca2-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8ca2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ca2-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8ca2-143">INPUTS</span></span>

### <span data-ttu-id="a8ca2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a8ca2-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a8ca2-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="a8ca2-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a8ca2-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8ca2-146">OUTPUTS</span></span>

### <span data-ttu-id="a8ca2-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="a8ca2-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="a8ca2-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8ca2-148">NOTES</span></span>

## <span data-ttu-id="a8ca2-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8ca2-149">RELATED LINKS</span></span>
