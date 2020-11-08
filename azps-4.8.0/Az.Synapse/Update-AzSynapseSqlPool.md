---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243457"
---
# <span data-ttu-id="0a8c8-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a8c8-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="0a8c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8c8-103">Обновляет пул SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a8c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a8c8-104">SYNTAX</span></span>

### <span data-ttu-id="0a8c8-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a8c8-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8c8-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8c8-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a8c8-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a8c8-117">DESCRIPTION</span></span>
<span data-ttu-id="0a8c8-118">Командлет **Update-AzSynapseSqlPool** ОБНОВЛЯЕТ пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a8c8-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a8c8-119">EXAMPLES</span></span>

### <span data-ttu-id="0a8c8-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a8c8-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="0a8c8-121">Эта команда обновляет пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="0a8c8-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0a8c8-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="0a8c8-123">Эта команда обновляет пул SQL Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="0a8c8-124">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0a8c8-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="0a8c8-125">Эта команда обновляет пул SQL Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="0a8c8-126">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0a8c8-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="0a8c8-127">Эта команда обновляет пул SQL Azure Synapse Analytics с ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="0a8c8-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a8c8-128">PARAMETERS</span></span>

### <span data-ttu-id="0a8c8-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a8c8-129">-AsJob</span></span>
<span data-ttu-id="0a8c8-130">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0a8c8-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a8c8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8c8-131">-DefaultProfile</span></span>
<span data-ttu-id="0a8c8-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a8c8-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8c8-133">-InputObject</span></span>
<span data-ttu-id="0a8c8-134">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a8c8-135">-Name</span></span>
<span data-ttu-id="0a8c8-136">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a8c8-137">-PassThru</span></span>
<span data-ttu-id="0a8c8-138">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0a8c8-139">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0a8c8-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="0a8c8-140">-PerformanceLevel</span></span>
<span data-ttu-id="0a8c8-141">Уровень производительности служб SQL, который нужно назначить пулу SQL.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="0a8c8-142">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8c8-143">-ResourceGroupName</span></span>
<span data-ttu-id="0a8c8-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8c8-145">-ResourceId</span></span>
<span data-ttu-id="0a8c8-146">Идентификатор ресурса пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-147">-Резюме</span><span class="sxs-lookup"><span data-stu-id="0a8c8-147">-Resume</span></span>
<span data-ttu-id="0a8c8-148">Указывает на возобновление работы пула SQL</span><span class="sxs-lookup"><span data-stu-id="0a8c8-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-149">-Suspend</span><span class="sxs-lookup"><span data-stu-id="0a8c8-149">-Suspend</span></span>
<span data-ttu-id="0a8c8-150">Указывает на приостановку пула SQL</span><span class="sxs-lookup"><span data-stu-id="0a8c8-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-151">-Тег</span><span class="sxs-lookup"><span data-stu-id="0a8c8-151">-Tag</span></span>
<span data-ttu-id="0a8c8-152">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-153">-Version</span><span class="sxs-lookup"><span data-stu-id="0a8c8-153">-Version</span></span>
<span data-ttu-id="0a8c8-154">Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="0a8c8-155">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-155">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="0a8c8-156">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a8c8-156">-WorkspaceName</span></span>
<span data-ttu-id="0a8c8-157">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-158">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a8c8-158">-WorkspaceObject</span></span>
<span data-ttu-id="0a8c8-159">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a8c8-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a8c8-160">-Confirm</span></span>
<span data-ttu-id="0a8c8-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a8c8-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8c8-162">-WhatIf</span></span>
<span data-ttu-id="0a8c8-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a8c8-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a8c8-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8c8-165">CommonParameters</span></span>
<span data-ttu-id="0a8c8-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a8c8-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8c8-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a8c8-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8c8-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a8c8-168">INPUTS</span></span>

### <span data-ttu-id="0a8c8-169">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a8c8-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0a8c8-170">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a8c8-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0a8c8-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a8c8-171">OUTPUTS</span></span>

### <span data-ttu-id="0a8c8-172">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a8c8-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0a8c8-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a8c8-173">NOTES</span></span>

## <span data-ttu-id="0a8c8-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a8c8-174">RELATED LINKS</span></span>
