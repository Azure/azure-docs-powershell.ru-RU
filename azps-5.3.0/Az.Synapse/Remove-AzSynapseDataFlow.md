---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: 2d0bec0c86f51771e971ca2c6b5a22c32f8ee687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507982"
---
# <span data-ttu-id="9c545-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="9c545-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="9c545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c545-102">SYNOPSIS</span></span>
<span data-ttu-id="9c545-103">Удаляет поток данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9c545-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="9c545-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9c545-104">SYNTAX</span></span>

### <span data-ttu-id="9c545-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c545-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c545-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9c545-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c545-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c545-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c545-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c545-108">DESCRIPTION</span></span>
<span data-ttu-id="9c545-109">Чтобы **удалить поток данных из** рабочей области, удалите поток данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9c545-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="9c545-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9c545-110">EXAMPLES</span></span>

### <span data-ttu-id="9c545-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9c545-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="9c545-112">Эта команда удаляет поток данных ContosoDataFlow из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="9c545-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9c545-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c545-113">PARAMETERS</span></span>

### <span data-ttu-id="9c545-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c545-114">-AsJob</span></span>
<span data-ttu-id="9c545-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9c545-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c545-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c545-116">-DefaultProfile</span></span>
<span data-ttu-id="9c545-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c545-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c545-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9c545-118">-Force</span></span>
<span data-ttu-id="9c545-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9c545-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9c545-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c545-120">-InputObject</span></span>
<span data-ttu-id="9c545-121">Объект потока данных.</span><span class="sxs-lookup"><span data-stu-id="9c545-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c545-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9c545-122">-Name</span></span>
<span data-ttu-id="9c545-123">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="9c545-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c545-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c545-124">-PassThru</span></span>
<span data-ttu-id="9c545-125">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c545-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9c545-126">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="9c545-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9c545-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9c545-127">-WorkspaceName</span></span>
<span data-ttu-id="9c545-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="9c545-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9c545-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9c545-129">-WorkspaceObject</span></span>
<span data-ttu-id="9c545-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="9c545-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9c545-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c545-131">-Confirm</span></span>
<span data-ttu-id="9c545-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9c545-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c545-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c545-133">-WhatIf</span></span>
<span data-ttu-id="9c545-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c545-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c545-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9c545-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c545-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c545-136">CommonParameters</span></span>
<span data-ttu-id="9c545-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c545-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c545-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c545-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c545-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c545-139">INPUTS</span></span>

### <span data-ttu-id="9c545-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9c545-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9c545-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="9c545-141">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="9c545-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9c545-142">OUTPUTS</span></span>

### <span data-ttu-id="9c545-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c545-143">System.Boolean</span></span>

## <span data-ttu-id="9c545-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9c545-144">NOTES</span></span>

## <span data-ttu-id="9c545-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c545-145">RELATED LINKS</span></span>