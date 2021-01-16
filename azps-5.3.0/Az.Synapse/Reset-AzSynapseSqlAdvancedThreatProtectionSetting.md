---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507969"
---
# <span data-ttu-id="c074f-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="c074f-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="c074f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c074f-102">SYNOPSIS</span></span>
<span data-ttu-id="c074f-103">Удаляет дополнительные параметры защиты от угроз из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c074f-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="c074f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c074f-104">SYNTAX</span></span>

### <span data-ttu-id="c074f-105">ClearByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c074f-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c074f-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c074f-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c074f-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c074f-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c074f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c074f-108">DESCRIPTION</span></span>
<span data-ttu-id="c074f-109">Cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** удаляет дополнительные параметры защиты от угроз из рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c074f-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="c074f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c074f-110">EXAMPLES</span></span>

### <span data-ttu-id="c074f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c074f-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c074f-112">Эта команда удаляет дополнительные параметры защиты от угроз из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c074f-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c074f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c074f-113">PARAMETERS</span></span>

### <span data-ttu-id="c074f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c074f-114">-AsJob</span></span>
<span data-ttu-id="c074f-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c074f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c074f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c074f-116">-DefaultProfile</span></span>
<span data-ttu-id="c074f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c074f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c074f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c074f-118">-InputObject</span></span>
<span data-ttu-id="c074f-119">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="c074f-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c074f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c074f-120">-PassThru</span></span>
<span data-ttu-id="c074f-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c074f-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c074f-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="c074f-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c074f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c074f-123">-ResourceGroupName</span></span>
<span data-ttu-id="c074f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c074f-124">Resource group name.</span></span>

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

### <span data-ttu-id="c074f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c074f-125">-ResourceId</span></span>
<span data-ttu-id="c074f-126">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c074f-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="c074f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c074f-127">-WorkspaceName</span></span>
<span data-ttu-id="c074f-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c074f-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c074f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c074f-129">-Confirm</span></span>
<span data-ttu-id="c074f-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c074f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c074f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c074f-131">-WhatIf</span></span>
<span data-ttu-id="c074f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c074f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c074f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c074f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c074f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c074f-134">CommonParameters</span></span>
<span data-ttu-id="c074f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c074f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c074f-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c074f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c074f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c074f-137">INPUTS</span></span>

### <span data-ttu-id="c074f-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c074f-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c074f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c074f-139">OUTPUTS</span></span>

### <span data-ttu-id="c074f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c074f-140">System.Boolean</span></span>

## <span data-ttu-id="c074f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c074f-141">NOTES</span></span>

## <span data-ttu-id="c074f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c074f-142">RELATED LINKS</span></span>
