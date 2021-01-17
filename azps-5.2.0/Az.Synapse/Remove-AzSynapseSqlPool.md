---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cce6c35fa1186829760bab7c69d9e149cedfc015
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395908"
---
# <span data-ttu-id="14c8a-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="14c8a-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="14c8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="14c8a-103">Удаляет пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="14c8a-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="14c8a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14c8a-104">SYNTAX</span></span>

### <span data-ttu-id="14c8a-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14c8a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14c8a-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c8a-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14c8a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c8a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14c8a-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c8a-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14c8a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14c8a-109">DESCRIPTION</span></span>
<span data-ttu-id="14c8a-110">Cmdlet **Remove-AzSynapseSqlPool** окончательно удаляет пул аналитики Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="14c8a-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="14c8a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14c8a-111">EXAMPLES</span></span>

### <span data-ttu-id="14c8a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="14c8a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="14c8a-113">Эта команда удаляет пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="14c8a-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="14c8a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="14c8a-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="14c8a-115">Эта команда удаляет пул Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="14c8a-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="14c8a-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="14c8a-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="14c8a-117">Эта команда удаляет пул Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="14c8a-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="14c8a-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="14c8a-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="14c8a-119">Эта команда удаляет пул Azure Synapse Analytics SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="14c8a-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="14c8a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14c8a-120">PARAMETERS</span></span>

### <span data-ttu-id="14c8a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14c8a-121">-AsJob</span></span>
<span data-ttu-id="14c8a-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="14c8a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14c8a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c8a-123">-DefaultProfile</span></span>
<span data-ttu-id="14c8a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14c8a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c8a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="14c8a-125">-Force</span></span>
<span data-ttu-id="14c8a-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="14c8a-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="14c8a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14c8a-127">-InputObject</span></span>
<span data-ttu-id="14c8a-128">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="14c8a-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="14c8a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="14c8a-129">-Name</span></span>
<span data-ttu-id="14c8a-130">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="14c8a-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="14c8a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14c8a-131">-PassThru</span></span>
<span data-ttu-id="14c8a-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14c8a-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="14c8a-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="14c8a-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="14c8a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c8a-134">-ResourceGroupName</span></span>
<span data-ttu-id="14c8a-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14c8a-135">Resource group name.</span></span>

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

### <span data-ttu-id="14c8a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14c8a-136">-ResourceId</span></span>
<span data-ttu-id="14c8a-137">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="14c8a-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="14c8a-138">-Версия</span><span class="sxs-lookup"><span data-stu-id="14c8a-138">-Version</span></span>
<span data-ttu-id="14c8a-139">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="14c8a-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="14c8a-140">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="14c8a-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="14c8a-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="14c8a-141">-WorkspaceName</span></span>
<span data-ttu-id="14c8a-142">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="14c8a-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14c8a-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="14c8a-143">-WorkspaceObject</span></span>
<span data-ttu-id="14c8a-144">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="14c8a-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="14c8a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14c8a-145">-Confirm</span></span>
<span data-ttu-id="14c8a-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="14c8a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14c8a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14c8a-147">-WhatIf</span></span>
<span data-ttu-id="14c8a-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14c8a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14c8a-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="14c8a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14c8a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c8a-150">CommonParameters</span></span>
<span data-ttu-id="14c8a-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c8a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c8a-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14c8a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c8a-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14c8a-153">INPUTS</span></span>

### <span data-ttu-id="14c8a-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14c8a-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="14c8a-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="14c8a-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="14c8a-156">System.String</span><span class="sxs-lookup"><span data-stu-id="14c8a-156">System.String</span></span>

## <span data-ttu-id="14c8a-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14c8a-157">OUTPUTS</span></span>

### <span data-ttu-id="14c8a-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14c8a-158">System.Boolean</span></span>

## <span data-ttu-id="14c8a-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14c8a-159">NOTES</span></span>

## <span data-ttu-id="14c8a-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14c8a-160">RELATED LINKS</span></span>
