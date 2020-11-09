---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316850"
---
# <span data-ttu-id="f3ee0-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f3ee0-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="f3ee0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ee0-103">Возобновление пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f3ee0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3ee0-104">SYNTAX</span></span>

### <span data-ttu-id="f3ee0-105">ResumeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f3ee0-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ee0-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ee0-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ee0-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ee0-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ee0-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ee0-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ee0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3ee0-109">DESCRIPTION</span></span>
<span data-ttu-id="f3ee0-110">Командлет **Resume-AzSynapseSqlPool** возобновляет работу пула SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f3ee0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3ee0-111">EXAMPLES</span></span>

### <span data-ttu-id="f3ee0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3ee0-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f3ee0-113">Эта команда возобновляет приостановленный пул SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f3ee0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3ee0-114">PARAMETERS</span></span>

### <span data-ttu-id="f3ee0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3ee0-115">-AsJob</span></span>
<span data-ttu-id="f3ee0-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f3ee0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3ee0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ee0-117">-DefaultProfile</span></span>
<span data-ttu-id="f3ee0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ee0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3ee0-119">-InputObject</span></span>
<span data-ttu-id="f3ee0-120">Входной объект пула SQL, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f3ee0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3ee0-121">-Name</span></span>
<span data-ttu-id="f3ee0-122">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3ee0-123">-PassThru</span></span>
<span data-ttu-id="f3ee0-124">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f3ee0-125">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f3ee0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ee0-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3ee0-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-127">Resource group name.</span></span>

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

### <span data-ttu-id="f3ee0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ee0-128">-ResourceId</span></span>
<span data-ttu-id="f3ee0-129">Идентификатор ресурса пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f3ee0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3ee0-130">-WorkspaceName</span></span>
<span data-ttu-id="f3ee0-131">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f3ee0-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3ee0-132">-WorkspaceObject</span></span>
<span data-ttu-id="f3ee0-133">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f3ee0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3ee0-134">-Confirm</span></span>
<span data-ttu-id="f3ee0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ee0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ee0-136">-WhatIf</span></span>
<span data-ttu-id="f3ee0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ee0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ee0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ee0-139">CommonParameters</span></span>
<span data-ttu-id="f3ee0-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3ee0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ee0-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3ee0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ee0-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3ee0-142">INPUTS</span></span>

### <span data-ttu-id="f3ee0-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3ee0-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f3ee0-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f3ee0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f3ee0-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3ee0-145">OUTPUTS</span></span>

### <span data-ttu-id="f3ee0-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f3ee0-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f3ee0-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3ee0-147">NOTES</span></span>

## <span data-ttu-id="f3ee0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3ee0-148">RELATED LINKS</span></span>
