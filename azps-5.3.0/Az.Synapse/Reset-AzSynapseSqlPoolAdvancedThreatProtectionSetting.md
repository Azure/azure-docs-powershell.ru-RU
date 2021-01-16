---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507970"
---
# <span data-ttu-id="37da4-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="37da4-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="37da4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37da4-102">SYNOPSIS</span></span>
<span data-ttu-id="37da4-103">Удаляет дополнительные параметры защиты от угроз из SQL пула.</span><span class="sxs-lookup"><span data-stu-id="37da4-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="37da4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37da4-104">SYNTAX</span></span>

### <span data-ttu-id="37da4-105">ClearByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37da4-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37da4-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37da4-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37da4-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37da4-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37da4-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37da4-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37da4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37da4-109">DESCRIPTION</span></span>
<span data-ttu-id="37da4-110">Из  пула Azure Synapse Analytics расширенные параметры защиты от угроз удаляются с SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="37da4-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="37da4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37da4-111">EXAMPLES</span></span>

### <span data-ttu-id="37da4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37da4-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="37da4-113">Эта команда удаляет дополнительные параметры защиты от SQL ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="37da4-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="37da4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37da4-114">PARAMETERS</span></span>

### <span data-ttu-id="37da4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37da4-115">-AsJob</span></span>
<span data-ttu-id="37da4-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="37da4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37da4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37da4-117">-DefaultProfile</span></span>
<span data-ttu-id="37da4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37da4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37da4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37da4-119">-InputObject</span></span>
<span data-ttu-id="37da4-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="37da4-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37da4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="37da4-121">-Name</span></span>
<span data-ttu-id="37da4-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="37da4-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37da4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37da4-123">-PassThru</span></span>
<span data-ttu-id="37da4-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37da4-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="37da4-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="37da4-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="37da4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37da4-126">-ResourceGroupName</span></span>
<span data-ttu-id="37da4-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37da4-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37da4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37da4-128">-ResourceId</span></span>
<span data-ttu-id="37da4-129">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="37da4-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37da4-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37da4-130">-WorkspaceName</span></span>
<span data-ttu-id="37da4-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="37da4-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37da4-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="37da4-132">-WorkspaceObject</span></span>
<span data-ttu-id="37da4-133">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="37da4-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37da4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37da4-134">-Confirm</span></span>
<span data-ttu-id="37da4-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="37da4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37da4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37da4-136">-WhatIf</span></span>
<span data-ttu-id="37da4-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37da4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37da4-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="37da4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37da4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37da4-139">CommonParameters</span></span>
<span data-ttu-id="37da4-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37da4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37da4-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37da4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37da4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37da4-142">INPUTS</span></span>

### <span data-ttu-id="37da4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="37da4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="37da4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="37da4-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="37da4-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37da4-145">OUTPUTS</span></span>

### <span data-ttu-id="37da4-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37da4-146">System.Boolean</span></span>

## <span data-ttu-id="37da4-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37da4-147">NOTES</span></span>

## <span data-ttu-id="37da4-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37da4-148">RELATED LINKS</span></span>
