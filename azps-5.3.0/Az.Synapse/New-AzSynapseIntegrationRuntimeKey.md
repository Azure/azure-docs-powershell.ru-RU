---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424276"
---
# <span data-ttu-id="d42ba-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d42ba-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="d42ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d42ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d42ba-103">Повторно сгенерировать ключ времени запуска интеграции для самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="d42ba-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="d42ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d42ba-104">SYNTAX</span></span>

### <span data-ttu-id="d42ba-105">NewByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d42ba-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d42ba-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d42ba-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d42ba-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d42ba-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d42ba-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d42ba-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d42ba-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d42ba-109">DESCRIPTION</span></span>
<span data-ttu-id="d42ba-110">Cmdlet **New-AzSynapseIntegrationRuntimeKey** повторно сгенерирует ключ интеграции runtime с именем ключа, заданным параметром KeyName.</span><span class="sxs-lookup"><span data-stu-id="d42ba-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="d42ba-111">Предыдущий ключ недействителен.</span><span class="sxs-lookup"><span data-stu-id="d42ba-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="d42ba-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d42ba-112">EXAMPLES</span></span>

### <span data-ttu-id="d42ba-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d42ba-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="d42ba-114">Этот cmdlet повторно сгенерирует ключ authKey2 для интеграции runtime test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="d42ba-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d42ba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d42ba-115">PARAMETERS</span></span>

### <span data-ttu-id="d42ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42ba-116">-DefaultProfile</span></span>
<span data-ttu-id="d42ba-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d42ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d42ba-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d42ba-118">-Force</span></span>
<span data-ttu-id="d42ba-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d42ba-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d42ba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d42ba-120">-InputObject</span></span>
<span data-ttu-id="d42ba-121">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="d42ba-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d42ba-122">-KeyName</span></span>
<span data-ttu-id="d42ba-123">Имя ключа проверки подлинности для самостоятельной интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="d42ba-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d42ba-124">-Name</span></span>
<span data-ttu-id="d42ba-125">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="d42ba-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d42ba-126">-ResourceGroupName</span></span>
<span data-ttu-id="d42ba-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d42ba-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d42ba-128">-ResourceId</span></span>
<span data-ttu-id="d42ba-129">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="d42ba-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d42ba-130">-WorkspaceName</span></span>
<span data-ttu-id="d42ba-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d42ba-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d42ba-132">-WorkspaceObject</span></span>
<span data-ttu-id="d42ba-133">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d42ba-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d42ba-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d42ba-134">-Confirm</span></span>
<span data-ttu-id="d42ba-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d42ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d42ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d42ba-136">-WhatIf</span></span>
<span data-ttu-id="d42ba-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d42ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d42ba-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d42ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d42ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42ba-139">CommonParameters</span></span>
<span data-ttu-id="d42ba-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d42ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42ba-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d42ba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42ba-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d42ba-142">INPUTS</span></span>

### <span data-ttu-id="d42ba-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d42ba-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d42ba-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d42ba-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d42ba-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d42ba-145">OUTPUTS</span></span>

### <span data-ttu-id="d42ba-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="d42ba-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d42ba-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d42ba-147">NOTES</span></span>

## <span data-ttu-id="d42ba-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d42ba-148">RELATED LINKS</span></span>
