---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247143"
---
# <span data-ttu-id="08f18-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="08f18-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="08f18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08f18-102">SYNOPSIS</span></span>
<span data-ttu-id="08f18-103">Удаление узла с заданным именем в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="08f18-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="08f18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08f18-104">SYNTAX</span></span>

### <span data-ttu-id="08f18-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08f18-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f18-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f18-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08f18-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f18-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f18-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f18-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f18-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08f18-109">DESCRIPTION</span></span>
<span data-ttu-id="08f18-110">Командлет **Remove-AzSynapseIntegrationRuntimeNode** удаляет узел в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="08f18-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="08f18-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08f18-111">EXAMPLES</span></span>

### <span data-ttu-id="08f18-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08f18-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="08f18-113">Удаление узла с заданным именем в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="08f18-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="08f18-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08f18-114">PARAMETERS</span></span>

### <span data-ttu-id="08f18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f18-115">-DefaultProfile</span></span>
<span data-ttu-id="08f18-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08f18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f18-117">-Force</span><span class="sxs-lookup"><span data-stu-id="08f18-117">-Force</span></span>
<span data-ttu-id="08f18-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="08f18-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="08f18-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08f18-119">-InputObject</span></span>
<span data-ttu-id="08f18-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="08f18-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f18-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="08f18-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="08f18-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="08f18-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="08f18-123">-NodeName</span><span class="sxs-lookup"><span data-stu-id="08f18-123">-NodeName</span></span>
<span data-ttu-id="08f18-124">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="08f18-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f18-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f18-125">-ResourceGroupName</span></span>
<span data-ttu-id="08f18-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08f18-126">Resource group name.</span></span>

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

### <span data-ttu-id="08f18-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08f18-127">-ResourceId</span></span>
<span data-ttu-id="08f18-128">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="08f18-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="08f18-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08f18-129">-WorkspaceName</span></span>
<span data-ttu-id="08f18-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="08f18-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="08f18-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="08f18-131">-WorkspaceObject</span></span>
<span data-ttu-id="08f18-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="08f18-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="08f18-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08f18-133">-Confirm</span></span>
<span data-ttu-id="08f18-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08f18-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f18-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f18-135">-WhatIf</span></span>
<span data-ttu-id="08f18-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08f18-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f18-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08f18-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f18-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f18-138">CommonParameters</span></span>
<span data-ttu-id="08f18-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08f18-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f18-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f18-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f18-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08f18-141">INPUTS</span></span>

### <span data-ttu-id="08f18-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="08f18-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="08f18-143">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="08f18-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="08f18-144">System. String</span><span class="sxs-lookup"><span data-stu-id="08f18-144">System.String</span></span>

## <span data-ttu-id="08f18-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08f18-145">OUTPUTS</span></span>

### <span data-ttu-id="08f18-146">System. void</span><span class="sxs-lookup"><span data-stu-id="08f18-146">System.Void</span></span>

## <span data-ttu-id="08f18-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="08f18-147">NOTES</span></span>

## <span data-ttu-id="08f18-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08f18-148">RELATED LINKS</span></span>