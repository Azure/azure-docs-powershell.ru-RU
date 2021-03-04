---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 298077ced1b7cb308bae4a8a5d27e13893c4b4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999169"
---
# <span data-ttu-id="6471b-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6471b-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6471b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6471b-102">SYNOPSIS</span></span>
<span data-ttu-id="6471b-103">Удаляет пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="6471b-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6471b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6471b-104">SYNTAX</span></span>

### <span data-ttu-id="6471b-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6471b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6471b-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6471b-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6471b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6471b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6471b-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6471b-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6471b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6471b-109">DESCRIPTION</span></span>
<span data-ttu-id="6471b-110">Cmdlet **Remove-AzSynapseSqlPool** окончательно удаляет пул аналитики Azure Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="6471b-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6471b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6471b-111">EXAMPLES</span></span>

### <span data-ttu-id="6471b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6471b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6471b-113">Эта команда удаляет пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="6471b-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="6471b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6471b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="6471b-115">Эта команда удаляет пул Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="6471b-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="6471b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6471b-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="6471b-117">Эта команда удаляет пул Azure Synapse Analytics SQL через канал.</span><span class="sxs-lookup"><span data-stu-id="6471b-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="6471b-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6471b-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="6471b-119">Эта команда удаляет пул Azure Synapse Analytics SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="6471b-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="6471b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6471b-120">PARAMETERS</span></span>

### <span data-ttu-id="6471b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6471b-121">-AsJob</span></span>
<span data-ttu-id="6471b-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6471b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6471b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6471b-123">-DefaultProfile</span></span>
<span data-ttu-id="6471b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6471b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6471b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6471b-125">-Force</span></span>
<span data-ttu-id="6471b-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6471b-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6471b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6471b-127">-InputObject</span></span>
<span data-ttu-id="6471b-128">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="6471b-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6471b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6471b-129">-Name</span></span>
<span data-ttu-id="6471b-130">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6471b-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6471b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6471b-131">-PassThru</span></span>
<span data-ttu-id="6471b-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6471b-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6471b-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="6471b-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6471b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6471b-134">-ResourceGroupName</span></span>
<span data-ttu-id="6471b-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6471b-135">Resource group name.</span></span>

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

### <span data-ttu-id="6471b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6471b-136">-ResourceId</span></span>
<span data-ttu-id="6471b-137">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6471b-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6471b-138">-Version</span><span class="sxs-lookup"><span data-stu-id="6471b-138">-Version</span></span>
<span data-ttu-id="6471b-139">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6471b-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="6471b-140">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="6471b-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="6471b-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6471b-141">-WorkspaceName</span></span>
<span data-ttu-id="6471b-142">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="6471b-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6471b-143">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6471b-143">-WorkspaceObject</span></span>
<span data-ttu-id="6471b-144">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="6471b-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6471b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6471b-145">-Confirm</span></span>
<span data-ttu-id="6471b-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6471b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6471b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6471b-147">-WhatIf</span></span>
<span data-ttu-id="6471b-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6471b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6471b-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6471b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6471b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6471b-150">CommonParameters</span></span>
<span data-ttu-id="6471b-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6471b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6471b-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6471b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6471b-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6471b-153">INPUTS</span></span>

### <span data-ttu-id="6471b-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6471b-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6471b-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6471b-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="6471b-156">System.String</span><span class="sxs-lookup"><span data-stu-id="6471b-156">System.String</span></span>

## <span data-ttu-id="6471b-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6471b-157">OUTPUTS</span></span>

### <span data-ttu-id="6471b-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6471b-158">System.Boolean</span></span>

## <span data-ttu-id="6471b-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6471b-159">NOTES</span></span>

## <span data-ttu-id="6471b-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6471b-160">RELATED LINKS</span></span>
