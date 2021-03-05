---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 8b47466c2f40ff769c1755ea1d59873a120e5d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010147"
---
# <span data-ttu-id="f0c52-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="f0c52-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="f0c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c52-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c52-103">Удаляет параметры аудита для пула azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="f0c52-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f0c52-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0c52-104">SYNTAX</span></span>

### <span data-ttu-id="f0c52-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0c52-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c52-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c52-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c52-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c52-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0c52-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c52-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c52-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0c52-109">DESCRIPTION</span></span>
<span data-ttu-id="f0c52-110">Для пула аналитики Synapse Azure удаляются параметры аудита, задаваемые SQL Azure **AzSynapseSqlPoolAuditSetting.**</span><span class="sxs-lookup"><span data-stu-id="f0c52-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f0c52-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0c52-111">EXAMPLES</span></span>

### <span data-ttu-id="f0c52-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0c52-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f0c52-113">Эта команда удаляет параметры аудита для SQL ContosoSqlPool в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f0c52-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f0c52-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f0c52-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="f0c52-115">Эта команда удаляет параметры аудита для пула SQL ContosoSqlPool в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="f0c52-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f0c52-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0c52-116">PARAMETERS</span></span>

### <span data-ttu-id="f0c52-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0c52-117">-AsJob</span></span>
<span data-ttu-id="f0c52-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f0c52-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0c52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c52-119">-DefaultProfile</span></span>
<span data-ttu-id="f0c52-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c52-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c52-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0c52-121">-InputObject</span></span>
<span data-ttu-id="f0c52-122">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="f0c52-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c52-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f0c52-123">-Name</span></span>
<span data-ttu-id="f0c52-124">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f0c52-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c52-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0c52-125">-PassThru</span></span>
<span data-ttu-id="f0c52-126">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0c52-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f0c52-127">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="f0c52-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f0c52-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c52-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0c52-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0c52-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c52-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0c52-130">-ResourceId</span></span>
<span data-ttu-id="f0c52-131">Идентификатор ресурса в SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f0c52-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c52-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f0c52-132">-WorkspaceName</span></span>
<span data-ttu-id="f0c52-133">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="f0c52-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c52-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f0c52-134">-WorkspaceObject</span></span>
<span data-ttu-id="f0c52-135">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f0c52-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c52-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0c52-136">-Confirm</span></span>
<span data-ttu-id="f0c52-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f0c52-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c52-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c52-138">-WhatIf</span></span>
<span data-ttu-id="f0c52-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c52-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c52-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0c52-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c52-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c52-141">CommonParameters</span></span>
<span data-ttu-id="f0c52-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c52-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c52-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0c52-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c52-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0c52-144">INPUTS</span></span>

### <span data-ttu-id="f0c52-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f0c52-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f0c52-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f0c52-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f0c52-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0c52-147">OUTPUTS</span></span>

### <span data-ttu-id="f0c52-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0c52-148">System.Boolean</span></span>

## <span data-ttu-id="f0c52-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0c52-149">NOTES</span></span>

## <span data-ttu-id="f0c52-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0c52-150">RELATED LINKS</span></span>
