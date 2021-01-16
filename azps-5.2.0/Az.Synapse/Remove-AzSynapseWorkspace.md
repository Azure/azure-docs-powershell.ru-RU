---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394268"
---
# <span data-ttu-id="a6164-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6164-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="a6164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6164-102">SYNOPSIS</span></span>
<span data-ttu-id="a6164-103">Удаляет рабочее пространство Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6164-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a6164-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6164-104">SYNTAX</span></span>

### <span data-ttu-id="a6164-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6164-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6164-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6164-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6164-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6164-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6164-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6164-108">DESCRIPTION</span></span>
<span data-ttu-id="a6164-109">Командлет **Remove-AzSynapseWorkspace** окончательно удаляет рабочее пространство Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6164-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a6164-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6164-110">EXAMPLES</span></span>

### <span data-ttu-id="a6164-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6164-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="a6164-112">Эта команда удаляет рабочее пространство Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6164-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="a6164-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6164-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="a6164-114">Эта команда удаляет через конвейер рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a6164-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="a6164-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a6164-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="a6164-116">Эта команда удаляет рабочее пространство Azure Synapse Analytics через канал с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6164-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="a6164-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6164-117">PARAMETERS</span></span>

### <span data-ttu-id="a6164-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6164-118">-AsJob</span></span>
<span data-ttu-id="a6164-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a6164-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6164-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6164-120">-DefaultProfile</span></span>
<span data-ttu-id="a6164-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6164-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6164-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a6164-122">-Force</span></span>
<span data-ttu-id="a6164-123">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a6164-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6164-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6164-124">-InputObject</span></span>
<span data-ttu-id="a6164-125">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="a6164-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a6164-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a6164-126">-Name</span></span>
<span data-ttu-id="a6164-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6164-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a6164-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6164-128">-PassThru</span></span>
<span data-ttu-id="a6164-129">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6164-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a6164-130">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="a6164-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a6164-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6164-131">-ResourceGroupName</span></span>
<span data-ttu-id="a6164-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6164-132">Resource group name.</span></span>

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

### <span data-ttu-id="a6164-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6164-133">-ResourceId</span></span>
<span data-ttu-id="a6164-134">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6164-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a6164-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6164-135">-Confirm</span></span>
<span data-ttu-id="a6164-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6164-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6164-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6164-137">-WhatIf</span></span>
<span data-ttu-id="a6164-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6164-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6164-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6164-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6164-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6164-140">CommonParameters</span></span>
<span data-ttu-id="a6164-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6164-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6164-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6164-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6164-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6164-143">INPUTS</span></span>

### <span data-ttu-id="a6164-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6164-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a6164-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6164-145">OUTPUTS</span></span>

### <span data-ttu-id="a6164-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6164-146">System.Boolean</span></span>

## <span data-ttu-id="a6164-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6164-147">NOTES</span></span>

## <span data-ttu-id="a6164-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6164-148">RELATED LINKS</span></span>
