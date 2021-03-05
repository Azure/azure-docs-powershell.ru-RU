---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9b4e55f701b956fc653cf08cddb87997a998315e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987468"
---
# <span data-ttu-id="cb7c1-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="cb7c1-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="cb7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7c1-103">Удаляет дополнительные параметры защиты от угроз из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="cb7c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb7c1-104">SYNTAX</span></span>

### <span data-ttu-id="cb7c1-105">ClearByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb7c1-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7c1-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7c1-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb7c1-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7c1-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb7c1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb7c1-108">DESCRIPTION</span></span>
<span data-ttu-id="cb7c1-109">Cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** удаляет дополнительные параметры защиты от угроз из рабочей области Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cb7c1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb7c1-110">EXAMPLES</span></span>

### <span data-ttu-id="cb7c1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb7c1-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cb7c1-112">Эта команда удаляет дополнительные параметры защиты от угроз из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cb7c1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb7c1-113">PARAMETERS</span></span>

### <span data-ttu-id="cb7c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb7c1-114">-AsJob</span></span>
<span data-ttu-id="cb7c1-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cb7c1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb7c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7c1-116">-DefaultProfile</span></span>
<span data-ttu-id="cb7c1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb7c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb7c1-118">-InputObject</span></span>
<span data-ttu-id="cb7c1-119">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cb7c1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb7c1-120">-PassThru</span></span>
<span data-ttu-id="cb7c1-121">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cb7c1-122">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cb7c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb7c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb7c1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-124">Resource group name.</span></span>

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

### <span data-ttu-id="cb7c1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb7c1-125">-ResourceId</span></span>
<span data-ttu-id="cb7c1-126">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cb7c1-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb7c1-127">-WorkspaceName</span></span>
<span data-ttu-id="cb7c1-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cb7c1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb7c1-129">-Confirm</span></span>
<span data-ttu-id="cb7c1-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb7c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb7c1-131">-WhatIf</span></span>
<span data-ttu-id="cb7c1-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb7c1-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb7c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7c1-134">CommonParameters</span></span>
<span data-ttu-id="cb7c1-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7c1-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb7c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7c1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb7c1-137">INPUTS</span></span>

### <span data-ttu-id="cb7c1-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cb7c1-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cb7c1-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb7c1-139">OUTPUTS</span></span>

### <span data-ttu-id="cb7c1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb7c1-140">System.Boolean</span></span>

## <span data-ttu-id="cb7c1-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb7c1-141">NOTES</span></span>

## <span data-ttu-id="cb7c1-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb7c1-142">RELATED LINKS</span></span>
