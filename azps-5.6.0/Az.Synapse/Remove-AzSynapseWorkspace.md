---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: f8fc68c94142f9c215a6662e7bf41423c1b5de40
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993138"
---
# <span data-ttu-id="233b4-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="233b4-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="233b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="233b4-102">SYNOPSIS</span></span>
<span data-ttu-id="233b4-103">Удаляет рабочее пространство Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="233b4-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="233b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="233b4-104">SYNTAX</span></span>

### <span data-ttu-id="233b4-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="233b4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="233b4-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="233b4-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="233b4-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="233b4-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="233b4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="233b4-108">DESCRIPTION</span></span>
<span data-ttu-id="233b4-109">Командлет **Remove-AzSynapseWorkspace** окончательно удаляет рабочее пространство Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="233b4-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="233b4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="233b4-110">EXAMPLES</span></span>

### <span data-ttu-id="233b4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="233b4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="233b4-112">Эта команда удаляет рабочее пространство Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="233b4-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="233b4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="233b4-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="233b4-114">Эта команда удаляет через конвейер рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="233b4-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="233b4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="233b4-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="233b4-116">Эта команда удаляет рабочее пространство Azure Synapse Analytics через канал с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="233b4-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="233b4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="233b4-117">PARAMETERS</span></span>

### <span data-ttu-id="233b4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="233b4-118">-AsJob</span></span>
<span data-ttu-id="233b4-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="233b4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="233b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="233b4-120">-DefaultProfile</span></span>
<span data-ttu-id="233b4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="233b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="233b4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="233b4-122">-Force</span></span>
<span data-ttu-id="233b4-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="233b4-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="233b4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="233b4-124">-InputObject</span></span>
<span data-ttu-id="233b4-125">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="233b4-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="233b4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="233b4-126">-Name</span></span>
<span data-ttu-id="233b4-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="233b4-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233b4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="233b4-128">-PassThru</span></span>
<span data-ttu-id="233b4-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="233b4-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="233b4-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="233b4-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="233b4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="233b4-131">-ResourceGroupName</span></span>
<span data-ttu-id="233b4-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="233b4-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233b4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="233b4-133">-ResourceId</span></span>
<span data-ttu-id="233b4-134">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="233b4-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="233b4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="233b4-135">-Confirm</span></span>
<span data-ttu-id="233b4-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="233b4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="233b4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="233b4-137">-WhatIf</span></span>
<span data-ttu-id="233b4-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="233b4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="233b4-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="233b4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="233b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="233b4-140">CommonParameters</span></span>
<span data-ttu-id="233b4-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="233b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="233b4-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="233b4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="233b4-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="233b4-143">INPUTS</span></span>

### <span data-ttu-id="233b4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="233b4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="233b4-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="233b4-145">OUTPUTS</span></span>

### <span data-ttu-id="233b4-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="233b4-146">System.Boolean</span></span>

## <span data-ttu-id="233b4-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="233b4-147">NOTES</span></span>

## <span data-ttu-id="233b4-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="233b4-148">RELATED LINKS</span></span>
