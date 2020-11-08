---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245146"
---
# <span data-ttu-id="180b1-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="180b1-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="180b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="180b1-102">SYNOPSIS</span></span>
<span data-ttu-id="180b1-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="180b1-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="180b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="180b1-104">SYNTAX</span></span>

### <span data-ttu-id="180b1-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="180b1-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="180b1-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="180b1-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="180b1-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="180b1-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="180b1-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="180b1-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="180b1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="180b1-109">DESCRIPTION</span></span>
<span data-ttu-id="180b1-110">Командлет **Update-AzSynapseIntegrationRuntime** обновляет свойства среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="180b1-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="180b1-111">В настоящее время командлет поддерживает обновление "автоматическое обновление" и "AutoUpdateDelayOffset" для самостоятельной среды интеграции.</span><span class="sxs-lookup"><span data-stu-id="180b1-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="180b1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="180b1-112">EXAMPLES</span></span>

### <span data-ttu-id="180b1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="180b1-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="180b1-114">Командлет обновляет саморазмещенную среду интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="180b1-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="180b1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="180b1-115">PARAMETERS</span></span>

### <span data-ttu-id="180b1-116">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="180b1-116">-AutoUpdate</span></span>
<span data-ttu-id="180b1-117">Включите или отключите автоматическое обновление среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="180b1-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="180b1-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="180b1-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="180b1-119">Время, в течение которого осуществляется автоматическое обновление среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="180b1-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="180b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180b1-120">-DefaultProfile</span></span>
<span data-ttu-id="180b1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="180b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="180b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="180b1-122">-InputObject</span></span>
<span data-ttu-id="180b1-123">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="180b1-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="180b1-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="180b1-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="180b1-125">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="180b1-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="180b1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180b1-126">-ResourceGroupName</span></span>
<span data-ttu-id="180b1-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="180b1-127">Resource group name.</span></span>

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

### <span data-ttu-id="180b1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="180b1-128">-ResourceId</span></span>
<span data-ttu-id="180b1-129">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="180b1-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="180b1-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="180b1-130">-WorkspaceName</span></span>
<span data-ttu-id="180b1-131">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="180b1-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="180b1-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="180b1-132">-WorkspaceObject</span></span>
<span data-ttu-id="180b1-133">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="180b1-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="180b1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="180b1-134">-Confirm</span></span>
<span data-ttu-id="180b1-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="180b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="180b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="180b1-136">-WhatIf</span></span>
<span data-ttu-id="180b1-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="180b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="180b1-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="180b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="180b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180b1-139">CommonParameters</span></span>
<span data-ttu-id="180b1-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="180b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180b1-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="180b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180b1-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="180b1-142">INPUTS</span></span>

### <span data-ttu-id="180b1-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="180b1-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="180b1-144">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="180b1-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="180b1-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="180b1-145">OUTPUTS</span></span>

### <span data-ttu-id="180b1-146">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="180b1-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="180b1-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="180b1-147">NOTES</span></span>

## <span data-ttu-id="180b1-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="180b1-148">RELATED LINKS</span></span>
