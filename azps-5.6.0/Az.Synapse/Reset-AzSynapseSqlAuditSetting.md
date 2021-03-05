---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 00d9682eb6562cfbfb9d06a4c8a6bac3b149cea1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973704"
---
# <span data-ttu-id="617a1-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="617a1-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="617a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="617a1-102">SYNOPSIS</span></span>
<span data-ttu-id="617a1-103">Удаляет параметры аудита рабочей области аналитики Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="617a1-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="617a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="617a1-104">SYNTAX</span></span>

### <span data-ttu-id="617a1-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="617a1-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617a1-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="617a1-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="617a1-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="617a1-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="617a1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="617a1-108">DESCRIPTION</span></span>
<span data-ttu-id="617a1-109">Для **параметра Reset-AzSynapseSqlAuditSetting** удаляются параметры аудита рабочей области аналитики Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="617a1-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="617a1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="617a1-110">EXAMPLES</span></span>

### <span data-ttu-id="617a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="617a1-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="617a1-112">Эта команда удаляет параметры аудита рабочей области Azure Synapse Analytics с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="617a1-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="617a1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="617a1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="617a1-114">Эта команда удаляет параметры аудита рабочей области Azure Synapse Analytics с именем ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="617a1-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="617a1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="617a1-115">PARAMETERS</span></span>

### <span data-ttu-id="617a1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="617a1-116">-AsJob</span></span>
<span data-ttu-id="617a1-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="617a1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="617a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617a1-118">-DefaultProfile</span></span>
<span data-ttu-id="617a1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="617a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="617a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="617a1-120">-InputObject</span></span>
<span data-ttu-id="617a1-121">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="617a1-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="617a1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="617a1-122">-PassThru</span></span>
<span data-ttu-id="617a1-123">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="617a1-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="617a1-124">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="617a1-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="617a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="617a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="617a1-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="617a1-126">Resource group name.</span></span>

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

### <span data-ttu-id="617a1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="617a1-127">-ResourceId</span></span>
<span data-ttu-id="617a1-128">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="617a1-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="617a1-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="617a1-129">-WorkspaceName</span></span>
<span data-ttu-id="617a1-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="617a1-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="617a1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="617a1-131">-Confirm</span></span>
<span data-ttu-id="617a1-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="617a1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="617a1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="617a1-133">-WhatIf</span></span>
<span data-ttu-id="617a1-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="617a1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="617a1-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="617a1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="617a1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="617a1-136">CommonParameters</span></span>
<span data-ttu-id="617a1-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="617a1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="617a1-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="617a1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="617a1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="617a1-139">INPUTS</span></span>

### <span data-ttu-id="617a1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="617a1-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="617a1-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="617a1-141">OUTPUTS</span></span>

### <span data-ttu-id="617a1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="617a1-142">System.Boolean</span></span>

## <span data-ttu-id="617a1-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="617a1-143">NOTES</span></span>

## <span data-ttu-id="617a1-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="617a1-144">RELATED LINKS</span></span>
