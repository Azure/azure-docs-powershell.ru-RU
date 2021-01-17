---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414308"
---
# <span data-ttu-id="fa557-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fa557-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="fa557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa557-102">SYNOPSIS</span></span>
<span data-ttu-id="fa557-103">Приостановка работы пула средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="fa557-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fa557-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa557-104">SYNTAX</span></span>

### <span data-ttu-id="fa557-105">SuspendByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa557-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa557-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa557-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa557-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa557-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa557-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa557-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa557-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa557-109">DESCRIPTION</span></span>
<span data-ttu-id="fa557-110">Приостановка пула аналитики Azure Synapse Analytics для **Suspend-AzSynapseSqlPool** SQL.</span><span class="sxs-lookup"><span data-stu-id="fa557-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fa557-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa557-111">EXAMPLES</span></span>

### <span data-ttu-id="fa557-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa557-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="fa557-113">Эта команда приостанавливать активный пул azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="fa557-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="fa557-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa557-114">PARAMETERS</span></span>

### <span data-ttu-id="fa557-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa557-115">-AsJob</span></span>
<span data-ttu-id="fa557-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fa557-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa557-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa557-117">-DefaultProfile</span></span>
<span data-ttu-id="fa557-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa557-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa557-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa557-119">-InputObject</span></span>
<span data-ttu-id="fa557-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="fa557-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa557-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa557-121">-Name</span></span>
<span data-ttu-id="fa557-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fa557-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa557-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa557-123">-PassThru</span></span>
<span data-ttu-id="fa557-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fa557-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fa557-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="fa557-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fa557-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa557-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa557-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa557-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa557-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa557-128">-ResourceId</span></span>
<span data-ttu-id="fa557-129">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fa557-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa557-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fa557-130">-WorkspaceName</span></span>
<span data-ttu-id="fa557-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="fa557-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa557-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fa557-132">-WorkspaceObject</span></span>
<span data-ttu-id="fa557-133">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fa557-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa557-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa557-134">-Confirm</span></span>
<span data-ttu-id="fa557-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fa557-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa557-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa557-136">-WhatIf</span></span>
<span data-ttu-id="fa557-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa557-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa557-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa557-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa557-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa557-139">CommonParameters</span></span>
<span data-ttu-id="fa557-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa557-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa557-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa557-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa557-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa557-142">INPUTS</span></span>

### <span data-ttu-id="fa557-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa557-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fa557-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fa557-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fa557-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa557-145">OUTPUTS</span></span>

### <span data-ttu-id="fa557-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fa557-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fa557-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa557-147">NOTES</span></span>

## <span data-ttu-id="fa557-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa557-148">RELATED LINKS</span></span>
