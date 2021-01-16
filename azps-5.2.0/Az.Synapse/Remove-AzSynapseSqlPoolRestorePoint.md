---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: e9c4c68f794b5ea0c20b0e1fe57677b329b02622
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399863"
---
# <span data-ttu-id="20867-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="20867-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="20867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20867-102">SYNOPSIS</span></span>
<span data-ttu-id="20867-103">Удаляет синапсексическую аналитику SQL точки восстановления пула.</span><span class="sxs-lookup"><span data-stu-id="20867-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="20867-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20867-104">SYNTAX</span></span>

### <span data-ttu-id="20867-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20867-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -SqlPoolName <String> -Name <String> 
[-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20867-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20867-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -Name <String> -SqlPoolObject <PSSynapseSqlPool> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20867-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20867-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20867-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20867-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20867-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20867-109">DESCRIPTION</span></span>
<span data-ttu-id="20867-110">Cmdlet **Remove-AzSynapseSqlPoolRestorePoint** окончательно удаляет точку восстановления пула Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="20867-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="20867-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20867-111">EXAMPLES</span></span>

### <span data-ttu-id="20867-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20867-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="20867-113">Эта команда удаляет точки восстановления пула SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="20867-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="20867-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="20867-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="20867-115">Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="20867-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="20867-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="20867-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="20867-117">Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="20867-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="20867-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="20867-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="20867-119">Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="20867-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="20867-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20867-120">PARAMETERS</span></span>

### <span data-ttu-id="20867-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20867-121">-AsJob</span></span>
<span data-ttu-id="20867-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="20867-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20867-123">-Force</span><span class="sxs-lookup"><span data-stu-id="20867-123">-Force</span></span>
<span data-ttu-id="20867-124">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="20867-124">Do not ask for confirmation.</span></span>

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


### <span data-ttu-id="20867-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20867-125">-InputObject</span></span>
<span data-ttu-id="20867-126">SQL создания точки восстановления пула входной объект времени создания, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="20867-126">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20867-127">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="20867-127">-RestorePointCreationDate</span></span>
<span data-ttu-id="20867-128">Имя синапсеи SQL даты создания точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="20867-128">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20867-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20867-129">-PassThru</span></span>
<span data-ttu-id="20867-130">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20867-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="20867-131">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="20867-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="20867-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20867-132">-ResourceGroupName</span></span>
<span data-ttu-id="20867-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20867-133">Resource group name.</span></span>

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

### <span data-ttu-id="20867-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20867-134">-ResourceId</span></span>
<span data-ttu-id="20867-135">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="20867-135">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20867-136">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="20867-136">-SqlPoolName</span></span>
<span data-ttu-id="20867-137">Имя SQL-пула Synapse.</span><span class="sxs-lookup"><span data-stu-id="20867-137">Name of Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20867-138">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="20867-138">-SqlPoolObject</span></span>
<span data-ttu-id="20867-139">Входной объект SQL Pool обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="20867-139">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20867-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20867-140">-WorkspaceName</span></span>
<span data-ttu-id="20867-141">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="20867-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20867-142">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="20867-142">-WorkspaceObject</span></span>
<span data-ttu-id="20867-143">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="20867-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20867-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20867-144">-Confirm</span></span>
<span data-ttu-id="20867-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20867-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20867-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20867-146">-WhatIf</span></span>
<span data-ttu-id="20867-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20867-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20867-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="20867-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20867-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20867-149">CommonParameters</span></span>
<span data-ttu-id="20867-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20867-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20867-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20867-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20867-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20867-152">INPUTS</span></span>

### <span data-ttu-id="20867-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="20867-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="20867-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="20867-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="20867-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="20867-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="20867-156">System.String</span><span class="sxs-lookup"><span data-stu-id="20867-156">System.String</span></span>

## <span data-ttu-id="20867-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20867-157">OUTPUTS</span></span>

### <span data-ttu-id="20867-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20867-158">System.Boolean</span></span>

## <span data-ttu-id="20867-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20867-159">NOTES</span></span>

## <span data-ttu-id="20867-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20867-160">RELATED LINKS</span></span>
