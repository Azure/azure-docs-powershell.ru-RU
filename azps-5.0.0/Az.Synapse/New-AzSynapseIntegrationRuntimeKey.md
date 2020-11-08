---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247934"
---
# <span data-ttu-id="fb7d1-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="fb7d1-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="fb7d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7d1-103">Повторное создание ключа среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="fb7d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb7d1-104">SYNTAX</span></span>

### <span data-ttu-id="fb7d1-105">NewByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb7d1-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb7d1-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7d1-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d1-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7d1-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7d1-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7d1-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7d1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb7d1-109">DESCRIPTION</span></span>
<span data-ttu-id="fb7d1-110">Командлет **New-AzSynapseIntegrationRuntimeKey** повторно создает ключ среды выполнения Integration с именем ключа, заданным параметром keyName.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="fb7d1-111">Предыдущий ключ не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="fb7d1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb7d1-112">EXAMPLES</span></span>

### <span data-ttu-id="fb7d1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb7d1-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="fb7d1-114">Командлет повторно создает ключ "authKey2" для среды выполнения интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="fb7d1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb7d1-115">PARAMETERS</span></span>

### <span data-ttu-id="fb7d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7d1-116">-DefaultProfile</span></span>
<span data-ttu-id="fb7d1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7d1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fb7d1-118">-Force</span></span>
<span data-ttu-id="fb7d1-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fb7d1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb7d1-120">-InputObject</span></span>
<span data-ttu-id="fb7d1-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="fb7d1-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fb7d1-122">-KeyName</span></span>
<span data-ttu-id="fb7d1-123">Имя ключа проверки подлинности в среде выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="fb7d1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb7d1-124">-Name</span></span>
<span data-ttu-id="fb7d1-125">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="fb7d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb7d1-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-127">Resource group name.</span></span>

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

### <span data-ttu-id="fb7d1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7d1-128">-ResourceId</span></span>
<span data-ttu-id="fb7d1-129">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="fb7d1-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb7d1-130">-WorkspaceName</span></span>
<span data-ttu-id="fb7d1-131">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fb7d1-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb7d1-132">-WorkspaceObject</span></span>
<span data-ttu-id="fb7d1-133">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fb7d1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb7d1-134">-Confirm</span></span>
<span data-ttu-id="fb7d1-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7d1-136">-WhatIf</span></span>
<span data-ttu-id="fb7d1-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7d1-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7d1-139">CommonParameters</span></span>
<span data-ttu-id="fb7d1-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb7d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7d1-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb7d1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7d1-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb7d1-142">INPUTS</span></span>

### <span data-ttu-id="fb7d1-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb7d1-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fb7d1-144">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fb7d1-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fb7d1-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb7d1-145">OUTPUTS</span></span>

### <span data-ttu-id="fb7d1-146">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="fb7d1-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="fb7d1-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb7d1-147">NOTES</span></span>

## <span data-ttu-id="fb7d1-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb7d1-148">RELATED LINKS</span></span>
