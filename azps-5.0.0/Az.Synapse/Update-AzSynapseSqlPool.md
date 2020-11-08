---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246315"
---
# <span data-ttu-id="6b92b-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6b92b-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6b92b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b92b-102">SYNOPSIS</span></span>
<span data-ttu-id="6b92b-103">Обновляет пул SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="6b92b-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6b92b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b92b-104">SYNTAX</span></span>

### <span data-ttu-id="6b92b-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b92b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b92b-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b92b-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b92b-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b92b-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b92b-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b92b-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b92b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b92b-109">DESCRIPTION</span></span>
<span data-ttu-id="6b92b-110">Командлет **Update-AzSynapseSqlPool** ОБНОВЛЯЕТ пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b92b-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6b92b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b92b-111">EXAMPLES</span></span>

### <span data-ttu-id="6b92b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b92b-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="6b92b-113">Эта команда обновляет пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b92b-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="6b92b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6b92b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="6b92b-115">Эта команда обновляет пул SQL Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="6b92b-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="6b92b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6b92b-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="6b92b-117">Эта команда обновляет пул SQL Azure Synapse Analytics с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="6b92b-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="6b92b-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6b92b-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="6b92b-119">Эта команда обновляет пул SQL Azure Synapse Analytics с ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b92b-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="6b92b-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b92b-120">PARAMETERS</span></span>

### <span data-ttu-id="6b92b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b92b-121">-AsJob</span></span>
<span data-ttu-id="6b92b-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6b92b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b92b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b92b-123">-DefaultProfile</span></span>
<span data-ttu-id="6b92b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b92b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b92b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b92b-125">-InputObject</span></span>
<span data-ttu-id="6b92b-126">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6b92b-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6b92b-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b92b-127">-Name</span></span>
<span data-ttu-id="6b92b-128">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6b92b-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b92b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b92b-129">-PassThru</span></span>
<span data-ttu-id="6b92b-130">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b92b-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6b92b-131">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="6b92b-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6b92b-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="6b92b-132">-PerformanceLevel</span></span>
<span data-ttu-id="6b92b-133">Уровень производительности служб SQL, который нужно назначить пулу SQL.</span><span class="sxs-lookup"><span data-stu-id="6b92b-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="6b92b-134">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="6b92b-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="6b92b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b92b-135">-ResourceGroupName</span></span>
<span data-ttu-id="6b92b-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b92b-136">Resource group name.</span></span>

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

### <span data-ttu-id="6b92b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b92b-137">-ResourceId</span></span>
<span data-ttu-id="6b92b-138">Идентификатор ресурса пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6b92b-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6b92b-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="6b92b-139">-Tag</span></span>
<span data-ttu-id="6b92b-140">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="6b92b-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="6b92b-141">-Version</span><span class="sxs-lookup"><span data-stu-id="6b92b-141">-Version</span></span>
<span data-ttu-id="6b92b-142">Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="6b92b-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="6b92b-143">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="6b92b-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="6b92b-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6b92b-144">-WorkspaceName</span></span>
<span data-ttu-id="6b92b-145">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6b92b-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6b92b-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6b92b-146">-WorkspaceObject</span></span>
<span data-ttu-id="6b92b-147">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6b92b-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6b92b-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b92b-148">-Confirm</span></span>
<span data-ttu-id="6b92b-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b92b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b92b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b92b-150">-WhatIf</span></span>
<span data-ttu-id="6b92b-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b92b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b92b-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b92b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b92b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b92b-153">CommonParameters</span></span>
<span data-ttu-id="6b92b-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b92b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b92b-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b92b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b92b-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b92b-156">INPUTS</span></span>

### <span data-ttu-id="6b92b-157">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6b92b-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6b92b-158">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6b92b-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6b92b-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b92b-159">OUTPUTS</span></span>

### <span data-ttu-id="6b92b-160">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6b92b-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6b92b-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b92b-161">NOTES</span></span>

## <span data-ttu-id="6b92b-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b92b-162">RELATED LINKS</span></span>
