---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247914"
---
# <span data-ttu-id="c9c72-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9c72-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="c9c72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9c72-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c72-103">Удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="c9c72-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="c9c72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9c72-104">SYNTAX</span></span>

### <span data-ttu-id="c9c72-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9c72-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c72-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c72-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c72-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c72-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c72-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c72-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c72-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9c72-109">DESCRIPTION</span></span>
<span data-ttu-id="c9c72-110">Командлет **Remove-AzSynapseIntegrationRuntime** удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="c9c72-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="c9c72-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9c72-111">EXAMPLES</span></span>

### <span data-ttu-id="c9c72-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9c72-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="c9c72-113">Эта команда удаляет среду выполнения интеграции с именем "тест-зарезервирован — IR" из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c9c72-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c9c72-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9c72-114">PARAMETERS</span></span>

### <span data-ttu-id="c9c72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c72-115">-DefaultProfile</span></span>
<span data-ttu-id="c9c72-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9c72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c72-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c9c72-117">-Force</span></span>
<span data-ttu-id="c9c72-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c9c72-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c9c72-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c72-119">-InputObject</span></span>
<span data-ttu-id="c9c72-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="c9c72-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="c9c72-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9c72-121">-Name</span></span>
<span data-ttu-id="c9c72-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="c9c72-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c72-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c72-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9c72-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9c72-124">Resource group name.</span></span>

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

### <span data-ttu-id="c9c72-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9c72-125">-ResourceId</span></span>
<span data-ttu-id="c9c72-126">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="c9c72-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c9c72-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9c72-127">-WorkspaceName</span></span>
<span data-ttu-id="c9c72-128">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c9c72-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c9c72-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c9c72-129">-WorkspaceObject</span></span>
<span data-ttu-id="c9c72-130">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c9c72-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c9c72-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9c72-131">-Confirm</span></span>
<span data-ttu-id="c9c72-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9c72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c72-133">-WhatIf</span></span>
<span data-ttu-id="c9c72-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9c72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c72-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9c72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c72-136">CommonParameters</span></span>
<span data-ttu-id="c9c72-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9c72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c72-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9c72-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c72-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9c72-139">INPUTS</span></span>

### <span data-ttu-id="c9c72-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9c72-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c9c72-141">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c9c72-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c9c72-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9c72-142">OUTPUTS</span></span>

### <span data-ttu-id="c9c72-143">System. void</span><span class="sxs-lookup"><span data-stu-id="c9c72-143">System.Void</span></span>

## <span data-ttu-id="c9c72-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9c72-144">NOTES</span></span>

## <span data-ttu-id="c9c72-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9c72-145">RELATED LINKS</span></span>
