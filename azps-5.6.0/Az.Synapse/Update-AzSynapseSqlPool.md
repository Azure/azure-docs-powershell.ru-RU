---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959955"
---
# <span data-ttu-id="d389e-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d389e-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d389e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d389e-102">SYNOPSIS</span></span>
<span data-ttu-id="d389e-103">Обновляет пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="d389e-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d389e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d389e-104">SYNTAX</span></span>

### <span data-ttu-id="d389e-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d389e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d389e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d389e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d389e-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d389e-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d389e-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d389e-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d389e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d389e-109">DESCRIPTION</span></span>
<span data-ttu-id="d389e-110">Для пула azure Synapse Analytics обновляется SQL **Update-AzSynapseSqlPool.**</span><span class="sxs-lookup"><span data-stu-id="d389e-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d389e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d389e-111">EXAMPLES</span></span>

### <span data-ttu-id="d389e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d389e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="d389e-113">Эта команда обновляет пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="d389e-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="d389e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d389e-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="d389e-115">Эта команда обновляет пул Azure Synapse Analytics SQL по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d389e-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d389e-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d389e-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="d389e-117">Эта команда обновляет пул Azure Synapse Analytics SQL по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d389e-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="d389e-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d389e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="d389e-119">Эта команда обновляет пул azure Synapse Analytics SQL с помощью ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="d389e-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="d389e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d389e-120">PARAMETERS</span></span>

### <span data-ttu-id="d389e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d389e-121">-AsJob</span></span>
<span data-ttu-id="d389e-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d389e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d389e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d389e-123">-DefaultProfile</span></span>
<span data-ttu-id="d389e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d389e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d389e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d389e-125">-InputObject</span></span>
<span data-ttu-id="d389e-126">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d389e-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d389e-127">-Name</span></span>
<span data-ttu-id="d389e-128">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d389e-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d389e-129">-PassThru</span></span>
<span data-ttu-id="d389e-130">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d389e-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="d389e-131">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="d389e-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d389e-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="d389e-132">-PerformanceLevel</span></span>
<span data-ttu-id="d389e-133">Уровень SQL и уровень производительности службы, которые нужно назначить SQL пулу.</span><span class="sxs-lookup"><span data-stu-id="d389e-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="d389e-134">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="d389e-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d389e-135">-ResourceGroupName</span></span>
<span data-ttu-id="d389e-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d389e-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d389e-137">-ResourceId</span></span>
<span data-ttu-id="d389e-138">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d389e-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d389e-139">-Tag</span></span>
<span data-ttu-id="d389e-140">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="d389e-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-141">-Версия</span><span class="sxs-lookup"><span data-stu-id="d389e-141">-Version</span></span>
<span data-ttu-id="d389e-142">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d389e-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="d389e-143">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="d389e-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="d389e-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d389e-144">-WorkspaceName</span></span>
<span data-ttu-id="d389e-145">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d389e-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d389e-146">-WorkspaceObject</span></span>
<span data-ttu-id="d389e-147">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d389e-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d389e-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d389e-148">-Confirm</span></span>
<span data-ttu-id="d389e-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d389e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d389e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d389e-150">-WhatIf</span></span>
<span data-ttu-id="d389e-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d389e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d389e-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d389e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d389e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d389e-153">CommonParameters</span></span>
<span data-ttu-id="d389e-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d389e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d389e-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d389e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d389e-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d389e-156">INPUTS</span></span>

### <span data-ttu-id="d389e-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d389e-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d389e-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d389e-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d389e-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d389e-159">OUTPUTS</span></span>

### <span data-ttu-id="d389e-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d389e-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d389e-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d389e-161">NOTES</span></span>

## <span data-ttu-id="d389e-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d389e-162">RELATED LINKS</span></span>
