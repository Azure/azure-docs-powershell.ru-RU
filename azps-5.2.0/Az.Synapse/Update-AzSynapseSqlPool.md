---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400415"
---
# <span data-ttu-id="922fc-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="922fc-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="922fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="922fc-102">SYNOPSIS</span></span>
<span data-ttu-id="922fc-103">Обновляет пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="922fc-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="922fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="922fc-104">SYNTAX</span></span>

### <span data-ttu-id="922fc-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="922fc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fc-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fc-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fc-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fc-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="922fc-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="922fc-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="922fc-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="922fc-109">DESCRIPTION</span></span>
<span data-ttu-id="922fc-110">Для пула azure Synapse Analytics обновляется SQL **Update-AzSynapseSqlPool.**</span><span class="sxs-lookup"><span data-stu-id="922fc-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="922fc-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="922fc-111">EXAMPLES</span></span>

### <span data-ttu-id="922fc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="922fc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="922fc-113">Эта команда обновляет пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="922fc-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="922fc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="922fc-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="922fc-115">Эта команда обновляет пул Azure Synapse Analytics SQL по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="922fc-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="922fc-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="922fc-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="922fc-117">Эта команда обновляет пул Azure Synapse Analytics SQL по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="922fc-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="922fc-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="922fc-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="922fc-119">Эта команда обновляет пул azure Synapse Analytics SQL с помощью ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="922fc-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="922fc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="922fc-120">PARAMETERS</span></span>

### <span data-ttu-id="922fc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="922fc-121">-AsJob</span></span>
<span data-ttu-id="922fc-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="922fc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="922fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922fc-123">-DefaultProfile</span></span>
<span data-ttu-id="922fc-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="922fc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922fc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="922fc-125">-InputObject</span></span>
<span data-ttu-id="922fc-126">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="922fc-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="922fc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="922fc-127">-Name</span></span>
<span data-ttu-id="922fc-128">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="922fc-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="922fc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="922fc-129">-PassThru</span></span>
<span data-ttu-id="922fc-130">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="922fc-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="922fc-131">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="922fc-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="922fc-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="922fc-132">-PerformanceLevel</span></span>
<span data-ttu-id="922fc-133">Уровень SQL и уровень производительности службы, которые нужно назначить SQL пулу.</span><span class="sxs-lookup"><span data-stu-id="922fc-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="922fc-134">Например, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="922fc-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="922fc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="922fc-135">-ResourceGroupName</span></span>
<span data-ttu-id="922fc-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="922fc-136">Resource group name.</span></span>

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

### <span data-ttu-id="922fc-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="922fc-137">-ResourceId</span></span>
<span data-ttu-id="922fc-138">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="922fc-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="922fc-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="922fc-139">-Tag</span></span>
<span data-ttu-id="922fc-140">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="922fc-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="922fc-141">-Version</span><span class="sxs-lookup"><span data-stu-id="922fc-141">-Version</span></span>
<span data-ttu-id="922fc-142">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="922fc-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="922fc-143">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="922fc-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="922fc-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="922fc-144">-WorkspaceName</span></span>
<span data-ttu-id="922fc-145">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="922fc-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="922fc-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="922fc-146">-WorkspaceObject</span></span>
<span data-ttu-id="922fc-147">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="922fc-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="922fc-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="922fc-148">-Confirm</span></span>
<span data-ttu-id="922fc-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="922fc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922fc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922fc-150">-WhatIf</span></span>
<span data-ttu-id="922fc-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="922fc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922fc-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="922fc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922fc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922fc-153">CommonParameters</span></span>
<span data-ttu-id="922fc-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922fc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922fc-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="922fc-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922fc-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="922fc-156">INPUTS</span></span>

### <span data-ttu-id="922fc-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="922fc-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="922fc-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="922fc-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="922fc-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="922fc-159">OUTPUTS</span></span>

### <span data-ttu-id="922fc-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="922fc-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="922fc-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="922fc-161">NOTES</span></span>

## <span data-ttu-id="922fc-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="922fc-162">RELATED LINKS</span></span>
