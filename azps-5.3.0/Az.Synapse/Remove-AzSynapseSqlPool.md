---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424132"
---
# <span data-ttu-id="286b5-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="286b5-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="286b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286b5-102">SYNOPSIS</span></span>
<span data-ttu-id="286b5-103">Удаляет пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="286b5-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="286b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="286b5-104">SYNTAX</span></span>

### <span data-ttu-id="286b5-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="286b5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="286b5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286b5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286b5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286b5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286b5-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="286b5-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286b5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="286b5-109">DESCRIPTION</span></span>
<span data-ttu-id="286b5-110">Cmdlet **Remove-AzSynapseSqlPool** окончательно удаляет пул аналитики Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="286b5-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="286b5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="286b5-111">EXAMPLES</span></span>

### <span data-ttu-id="286b5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="286b5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="286b5-113">Эта команда удаляет пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="286b5-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="286b5-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="286b5-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="286b5-115">Эта команда удаляет пул Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="286b5-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="286b5-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="286b5-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="286b5-117">Эта команда удаляет пул Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="286b5-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="286b5-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="286b5-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="286b5-119">Эта команда удаляет пул Azure Synapse Analytics SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="286b5-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="286b5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="286b5-120">PARAMETERS</span></span>

### <span data-ttu-id="286b5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="286b5-121">-AsJob</span></span>
<span data-ttu-id="286b5-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="286b5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="286b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286b5-123">-DefaultProfile</span></span>
<span data-ttu-id="286b5-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="286b5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286b5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="286b5-125">-Force</span></span>
<span data-ttu-id="286b5-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="286b5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="286b5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="286b5-127">-InputObject</span></span>
<span data-ttu-id="286b5-128">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="286b5-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="286b5-129">-Name</span></span>
<span data-ttu-id="286b5-130">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="286b5-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="286b5-131">-PassThru</span></span>
<span data-ttu-id="286b5-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="286b5-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="286b5-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="286b5-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="286b5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286b5-134">-ResourceGroupName</span></span>
<span data-ttu-id="286b5-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="286b5-135">Resource group name.</span></span>

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

### <span data-ttu-id="286b5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="286b5-136">-ResourceId</span></span>
<span data-ttu-id="286b5-137">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="286b5-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="286b5-138">-Версия</span><span class="sxs-lookup"><span data-stu-id="286b5-138">-Version</span></span>
<span data-ttu-id="286b5-139">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="286b5-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="286b5-140">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="286b5-140">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286b5-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="286b5-141">-WorkspaceName</span></span>
<span data-ttu-id="286b5-142">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="286b5-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="286b5-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="286b5-143">-WorkspaceObject</span></span>
<span data-ttu-id="286b5-144">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="286b5-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="286b5-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="286b5-145">-Confirm</span></span>
<span data-ttu-id="286b5-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286b5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286b5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286b5-147">-WhatIf</span></span>
<span data-ttu-id="286b5-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286b5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286b5-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="286b5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286b5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286b5-150">CommonParameters</span></span>
<span data-ttu-id="286b5-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286b5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286b5-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="286b5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286b5-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="286b5-153">INPUTS</span></span>

### <span data-ttu-id="286b5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="286b5-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="286b5-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="286b5-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="286b5-156">System.String</span><span class="sxs-lookup"><span data-stu-id="286b5-156">System.String</span></span>

## <span data-ttu-id="286b5-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="286b5-157">OUTPUTS</span></span>

### <span data-ttu-id="286b5-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="286b5-158">System.Boolean</span></span>

## <span data-ttu-id="286b5-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="286b5-159">NOTES</span></span>

## <span data-ttu-id="286b5-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="286b5-160">RELATED LINKS</span></span>
