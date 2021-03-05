---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971608"
---
# <span data-ttu-id="24f9f-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="24f9f-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="24f9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="24f9f-103">Удаляет синапсексическую аналитику SQL точки восстановления пула.</span><span class="sxs-lookup"><span data-stu-id="24f9f-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="24f9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24f9f-104">SYNTAX</span></span>

### <span data-ttu-id="24f9f-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24f9f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f9f-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24f9f-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24f9f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24f9f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f9f-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24f9f-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f9f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24f9f-109">DESCRIPTION</span></span>
<span data-ttu-id="24f9f-110">С **его** SQL точки восстановления пула навсегда удаляется SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="24f9f-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="24f9f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24f9f-111">EXAMPLES</span></span>

### <span data-ttu-id="24f9f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24f9f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="24f9f-113">Эта команда удаляет точки восстановления пула SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="24f9f-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="24f9f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="24f9f-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="24f9f-115">Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="24f9f-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="24f9f-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="24f9f-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="24f9f-117">Эта команда удаляет точки восстановления пула Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="24f9f-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="24f9f-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="24f9f-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="24f9f-119">Эта команда удаляет точки SQL Azure Synapse Analytics с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="24f9f-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="24f9f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24f9f-120">PARAMETERS</span></span>

### <span data-ttu-id="24f9f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24f9f-121">-AsJob</span></span>
<span data-ttu-id="24f9f-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="24f9f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24f9f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f9f-123">-DefaultProfile</span></span>
<span data-ttu-id="24f9f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24f9f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f9f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="24f9f-125">-Force</span></span>
<span data-ttu-id="24f9f-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="24f9f-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="24f9f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24f9f-127">-InputObject</span></span>
<span data-ttu-id="24f9f-128">SQL создания точки восстановления пула входной объект времени создания, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="24f9f-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="24f9f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="24f9f-129">-Name</span></span>
<span data-ttu-id="24f9f-130">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="24f9f-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f9f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24f9f-131">-PassThru</span></span>
<span data-ttu-id="24f9f-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24f9f-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="24f9f-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="24f9f-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="24f9f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f9f-134">-ResourceGroupName</span></span>
<span data-ttu-id="24f9f-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24f9f-135">Resource group name.</span></span>

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

### <span data-ttu-id="24f9f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24f9f-136">-ResourceId</span></span>
<span data-ttu-id="24f9f-137">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="24f9f-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="24f9f-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="24f9f-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="24f9f-139">Имя синтаксиса SQL даты создания точки восстановления.</span><span class="sxs-lookup"><span data-stu-id="24f9f-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f9f-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="24f9f-140">-SqlPoolObject</span></span>
<span data-ttu-id="24f9f-141">Входной объект SQL Pool обычно передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="24f9f-141">Sql Pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="24f9f-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24f9f-142">-WorkspaceName</span></span>
<span data-ttu-id="24f9f-143">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="24f9f-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="24f9f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24f9f-144">-Confirm</span></span>
<span data-ttu-id="24f9f-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f9f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f9f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f9f-146">-WhatIf</span></span>
<span data-ttu-id="24f9f-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24f9f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f9f-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="24f9f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f9f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f9f-149">CommonParameters</span></span>
<span data-ttu-id="24f9f-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f9f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f9f-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24f9f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f9f-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24f9f-152">INPUTS</span></span>

### <span data-ttu-id="24f9f-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24f9f-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="24f9f-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="24f9f-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="24f9f-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="24f9f-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="24f9f-156">System.String</span><span class="sxs-lookup"><span data-stu-id="24f9f-156">System.String</span></span>

## <span data-ttu-id="24f9f-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24f9f-157">OUTPUTS</span></span>

### <span data-ttu-id="24f9f-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="24f9f-158">System.Boolean</span></span>

## <span data-ttu-id="24f9f-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24f9f-159">NOTES</span></span>

## <span data-ttu-id="24f9f-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24f9f-160">RELATED LINKS</span></span>
