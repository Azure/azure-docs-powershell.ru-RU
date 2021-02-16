---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243053"
---
# <span data-ttu-id="8b929-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="8b929-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="8b929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b929-102">SYNOPSIS</span></span>
<span data-ttu-id="8b929-103">Удаляет дополнительные параметры защиты от угроз из SQL пула.</span><span class="sxs-lookup"><span data-stu-id="8b929-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="8b929-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b929-104">SYNTAX</span></span>

### <span data-ttu-id="8b929-105">ClearByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b929-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b929-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b929-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b929-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b929-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b929-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b929-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b929-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b929-109">DESCRIPTION</span></span>
<span data-ttu-id="8b929-110">Из  пула Azure Synapse Analytics расширенные параметры защиты от угроз удаляются с SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8b929-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8b929-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b929-111">EXAMPLES</span></span>

### <span data-ttu-id="8b929-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b929-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="8b929-113">Эта команда удаляет дополнительные параметры защиты от SQL ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8b929-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8b929-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b929-114">PARAMETERS</span></span>

### <span data-ttu-id="8b929-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b929-115">-AsJob</span></span>
<span data-ttu-id="8b929-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b929-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b929-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b929-117">-DefaultProfile</span></span>
<span data-ttu-id="8b929-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b929-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b929-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b929-119">-InputObject</span></span>
<span data-ttu-id="8b929-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8b929-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8b929-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b929-121">-Name</span></span>
<span data-ttu-id="8b929-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b929-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="8b929-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b929-123">-PassThru</span></span>
<span data-ttu-id="8b929-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8b929-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8b929-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="8b929-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8b929-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b929-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b929-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b929-127">Resource group name.</span></span>

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

### <span data-ttu-id="8b929-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b929-128">-ResourceId</span></span>
<span data-ttu-id="8b929-129">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b929-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="8b929-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b929-130">-WorkspaceName</span></span>
<span data-ttu-id="8b929-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b929-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8b929-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8b929-132">-WorkspaceObject</span></span>
<span data-ttu-id="8b929-133">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8b929-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8b929-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b929-134">-Confirm</span></span>
<span data-ttu-id="8b929-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b929-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b929-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b929-136">-WhatIf</span></span>
<span data-ttu-id="8b929-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b929-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b929-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b929-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b929-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b929-139">CommonParameters</span></span>
<span data-ttu-id="8b929-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b929-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b929-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b929-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b929-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b929-142">INPUTS</span></span>

### <span data-ttu-id="8b929-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b929-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8b929-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8b929-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8b929-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b929-145">OUTPUTS</span></span>

### <span data-ttu-id="8b929-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b929-146">System.Boolean</span></span>

## <span data-ttu-id="8b929-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b929-147">NOTES</span></span>

## <span data-ttu-id="8b929-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b929-148">RELATED LINKS</span></span>
