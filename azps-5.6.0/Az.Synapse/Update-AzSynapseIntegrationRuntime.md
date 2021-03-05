---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 004cfc8e0bd22be1f57a320cf10aa7d7f53cbb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990713"
---
# <span data-ttu-id="acf9a-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="acf9a-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="acf9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acf9a-102">SYNOPSIS</span></span>
<span data-ttu-id="acf9a-103">Обновляет время интеграции.</span><span class="sxs-lookup"><span data-stu-id="acf9a-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="acf9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acf9a-104">SYNTAX</span></span>

### <span data-ttu-id="acf9a-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acf9a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf9a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf9a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acf9a-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf9a-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acf9a-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acf9a-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acf9a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acf9a-109">DESCRIPTION</span></span>
<span data-ttu-id="acf9a-110">Для свойств интеграции со временем запуска обновляется **cmdlet Update-AzSynapseIntegrationRuntime.**</span><span class="sxs-lookup"><span data-stu-id="acf9a-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="acf9a-111">В настоящее время для самостоятельной интеграции с этой службой можно обновить только автоматическое обновление и автоматическое обновлениеDelayOffset.</span><span class="sxs-lookup"><span data-stu-id="acf9a-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="acf9a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acf9a-112">EXAMPLES</span></span>

### <span data-ttu-id="acf9a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acf9a-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="acf9a-114">Для самостоятельной интеграции с этой службой обновляется процесс самостоятельной интеграции с именем test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="acf9a-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="acf9a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acf9a-115">PARAMETERS</span></span>

### <span data-ttu-id="acf9a-116">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="acf9a-116">-AutoUpdate</span></span>
<span data-ttu-id="acf9a-117">Включите или отключите автоматическое обновление автоматического обновления для самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="acf9a-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="acf9a-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="acf9a-119">Время суток для автоматического обновления времени самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="acf9a-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf9a-120">-DefaultProfile</span></span>
<span data-ttu-id="acf9a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acf9a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf9a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acf9a-122">-InputObject</span></span>
<span data-ttu-id="acf9a-123">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="acf9a-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="acf9a-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="acf9a-125">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="acf9a-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf9a-126">-ResourceGroupName</span></span>
<span data-ttu-id="acf9a-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acf9a-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acf9a-128">-ResourceId</span></span>
<span data-ttu-id="acf9a-129">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="acf9a-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="acf9a-130">-WorkspaceName</span></span>
<span data-ttu-id="acf9a-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="acf9a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="acf9a-132">-WorkspaceObject</span></span>
<span data-ttu-id="acf9a-133">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="acf9a-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acf9a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acf9a-134">-Confirm</span></span>
<span data-ttu-id="acf9a-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf9a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf9a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf9a-136">-WhatIf</span></span>
<span data-ttu-id="acf9a-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf9a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf9a-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="acf9a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf9a-139">CommonParameters</span></span>
<span data-ttu-id="acf9a-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf9a-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acf9a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf9a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acf9a-142">INPUTS</span></span>

### <span data-ttu-id="acf9a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="acf9a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="acf9a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="acf9a-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="acf9a-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acf9a-145">OUTPUTS</span></span>

### <span data-ttu-id="acf9a-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="acf9a-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="acf9a-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acf9a-147">NOTES</span></span>

## <span data-ttu-id="acf9a-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acf9a-148">RELATED LINKS</span></span>
