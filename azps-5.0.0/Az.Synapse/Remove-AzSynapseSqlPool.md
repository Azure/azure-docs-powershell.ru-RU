---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247137"
---
# <span data-ttu-id="e3d39-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e3d39-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e3d39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3d39-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d39-103">Удаление пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="e3d39-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e3d39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3d39-104">SYNTAX</span></span>

### <span data-ttu-id="e3d39-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3d39-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d39-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3d39-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d39-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3d39-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d39-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3d39-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d39-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3d39-109">DESCRIPTION</span></span>
<span data-ttu-id="e3d39-110">Командлет **Remove-AzSynapseSqlPool** окончательно УДАЛЯЕТ пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3d39-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e3d39-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3d39-111">EXAMPLES</span></span>

### <span data-ttu-id="e3d39-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3d39-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e3d39-113">Эта команда удаляет пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3d39-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="e3d39-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e3d39-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="e3d39-115">Эта команда удаляет пул SQL Azure Synapse Analytics из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e3d39-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e3d39-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e3d39-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="e3d39-117">Эта команда удаляет пул SQL Azure Synapse Analytics из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e3d39-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="e3d39-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e3d39-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="e3d39-119">Эта команда удаляет пул SQL Azure Synapse Analytics с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="e3d39-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="e3d39-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3d39-120">PARAMETERS</span></span>

### <span data-ttu-id="e3d39-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3d39-121">-AsJob</span></span>
<span data-ttu-id="e3d39-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e3d39-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3d39-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d39-123">-DefaultProfile</span></span>
<span data-ttu-id="e3d39-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d39-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d39-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3d39-125">-InputObject</span></span>
<span data-ttu-id="e3d39-126">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e3d39-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e3d39-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3d39-127">-Name</span></span>
<span data-ttu-id="e3d39-128">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e3d39-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e3d39-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3d39-129">-PassThru</span></span>
<span data-ttu-id="e3d39-130">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e3d39-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="e3d39-131">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="e3d39-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e3d39-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d39-132">-ResourceGroupName</span></span>
<span data-ttu-id="e3d39-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3d39-133">Resource group name.</span></span>

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

### <span data-ttu-id="e3d39-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3d39-134">-ResourceId</span></span>
<span data-ttu-id="e3d39-135">Идентификатор ресурса пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e3d39-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="e3d39-136">-Version</span><span class="sxs-lookup"><span data-stu-id="e3d39-136">-Version</span></span>
<span data-ttu-id="e3d39-137">Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="e3d39-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e3d39-138">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="e3d39-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="e3d39-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e3d39-139">-WorkspaceName</span></span>
<span data-ttu-id="e3d39-140">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e3d39-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e3d39-141">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e3d39-141">-WorkspaceObject</span></span>
<span data-ttu-id="e3d39-142">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e3d39-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e3d39-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3d39-143">-Confirm</span></span>
<span data-ttu-id="e3d39-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3d39-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d39-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d39-145">-WhatIf</span></span>
<span data-ttu-id="e3d39-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3d39-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d39-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3d39-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d39-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d39-148">CommonParameters</span></span>
<span data-ttu-id="e3d39-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3d39-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d39-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3d39-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d39-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3d39-151">INPUTS</span></span>

### <span data-ttu-id="e3d39-152">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3d39-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e3d39-153">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e3d39-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="e3d39-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e3d39-154">System.String</span></span>

## <span data-ttu-id="e3d39-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3d39-155">OUTPUTS</span></span>

### <span data-ttu-id="e3d39-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3d39-156">System.Boolean</span></span>

## <span data-ttu-id="e3d39-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3d39-157">NOTES</span></span>

## <span data-ttu-id="e3d39-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3d39-158">RELATED LINKS</span></span>
