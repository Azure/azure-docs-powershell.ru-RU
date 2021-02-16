---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243072"
---
# <span data-ttu-id="cef28-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cef28-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cef28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef28-102">SYNOPSIS</span></span>
<span data-ttu-id="cef28-103">Удаляет дополнительные параметры защиты от угроз из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cef28-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="cef28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cef28-104">SYNTAX</span></span>

### <span data-ttu-id="cef28-105">ClearByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef28-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef28-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef28-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef28-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cef28-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef28-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef28-108">DESCRIPTION</span></span>
<span data-ttu-id="cef28-109">Cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** удаляет дополнительные параметры защиты от угроз из рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cef28-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cef28-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cef28-110">EXAMPLES</span></span>

### <span data-ttu-id="cef28-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cef28-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cef28-112">Эта команда удаляет дополнительные параметры защиты от угроз из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cef28-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cef28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cef28-113">PARAMETERS</span></span>

### <span data-ttu-id="cef28-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cef28-114">-AsJob</span></span>
<span data-ttu-id="cef28-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cef28-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cef28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef28-116">-DefaultProfile</span></span>
<span data-ttu-id="cef28-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cef28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef28-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef28-118">-InputObject</span></span>
<span data-ttu-id="cef28-119">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cef28-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cef28-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cef28-120">-PassThru</span></span>
<span data-ttu-id="cef28-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cef28-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cef28-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="cef28-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cef28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef28-123">-ResourceGroupName</span></span>
<span data-ttu-id="cef28-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cef28-124">Resource group name.</span></span>

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

### <span data-ttu-id="cef28-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cef28-125">-ResourceId</span></span>
<span data-ttu-id="cef28-126">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cef28-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cef28-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cef28-127">-WorkspaceName</span></span>
<span data-ttu-id="cef28-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cef28-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cef28-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef28-129">-Confirm</span></span>
<span data-ttu-id="cef28-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef28-131">-WhatIf</span></span>
<span data-ttu-id="cef28-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef28-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef28-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cef28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef28-134">CommonParameters</span></span>
<span data-ttu-id="cef28-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef28-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cef28-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef28-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cef28-137">INPUTS</span></span>

### <span data-ttu-id="cef28-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cef28-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cef28-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cef28-139">OUTPUTS</span></span>

### <span data-ttu-id="cef28-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cef28-140">System.Boolean</span></span>

## <span data-ttu-id="cef28-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cef28-141">NOTES</span></span>

## <span data-ttu-id="cef28-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef28-142">RELATED LINKS</span></span>
