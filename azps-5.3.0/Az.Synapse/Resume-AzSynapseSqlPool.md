---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ff2a68d7e0ae0ad94f685bbe1cfb795f7cd6a706
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424060"
---
# <span data-ttu-id="33183-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="33183-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="33183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33183-102">SYNOPSIS</span></span>
<span data-ttu-id="33183-103">Возобновление пула средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="33183-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="33183-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="33183-104">SYNTAX</span></span>

### <span data-ttu-id="33183-105">ResumeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="33183-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33183-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33183-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33183-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33183-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33183-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33183-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33183-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33183-109">DESCRIPTION</span></span>
<span data-ttu-id="33183-110">С **его** SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="33183-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="33183-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="33183-111">EXAMPLES</span></span>

### <span data-ttu-id="33183-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33183-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="33183-113">Эта команда возобновляет приостановленный пул службы аналитики Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="33183-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="33183-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33183-114">PARAMETERS</span></span>

### <span data-ttu-id="33183-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33183-115">-AsJob</span></span>
<span data-ttu-id="33183-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="33183-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33183-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33183-117">-DefaultProfile</span></span>
<span data-ttu-id="33183-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33183-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33183-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33183-119">-InputObject</span></span>
<span data-ttu-id="33183-120">SQL пула входных данных, как правило, передается по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="33183-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33183-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33183-121">-Name</span></span>
<span data-ttu-id="33183-122">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="33183-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33183-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33183-123">-PassThru</span></span>
<span data-ttu-id="33183-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="33183-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="33183-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="33183-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="33183-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33183-126">-ResourceGroupName</span></span>
<span data-ttu-id="33183-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="33183-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33183-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33183-128">-ResourceId</span></span>
<span data-ttu-id="33183-129">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="33183-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33183-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="33183-130">-WorkspaceName</span></span>
<span data-ttu-id="33183-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="33183-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33183-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="33183-132">-WorkspaceObject</span></span>
<span data-ttu-id="33183-133">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="33183-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33183-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33183-134">-Confirm</span></span>
<span data-ttu-id="33183-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33183-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33183-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33183-136">-WhatIf</span></span>
<span data-ttu-id="33183-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33183-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33183-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="33183-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33183-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33183-139">CommonParameters</span></span>
<span data-ttu-id="33183-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33183-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33183-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33183-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33183-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33183-142">INPUTS</span></span>

### <span data-ttu-id="33183-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="33183-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="33183-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="33183-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="33183-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="33183-145">OUTPUTS</span></span>

### <span data-ttu-id="33183-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="33183-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="33183-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="33183-147">NOTES</span></span>

## <span data-ttu-id="33183-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33183-148">RELATED LINKS</span></span>
