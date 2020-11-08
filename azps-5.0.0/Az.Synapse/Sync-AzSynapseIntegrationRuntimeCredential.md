---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245160"
---
# <span data-ttu-id="31d4a-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="31d4a-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="31d4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="31d4a-103">Синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="31d4a-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="31d4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31d4a-104">SYNTAX</span></span>

### <span data-ttu-id="31d4a-105">StopByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31d4a-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31d4a-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31d4a-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31d4a-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31d4a-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31d4a-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31d4a-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31d4a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31d4a-109">DESCRIPTION</span></span>
<span data-ttu-id="31d4a-110">Командлет **Sync-AzSynapseIntegrationRuntimeCredential** синхронизирует локальные учетные данные между узлами среды выполнения интеграции, что приводит к идентичности учетных данных на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="31d4a-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="31d4a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31d4a-111">EXAMPLES</span></span>

### <span data-ttu-id="31d4a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31d4a-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="31d4a-113">Синхронизирует учетные данные между узлами среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="31d4a-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="31d4a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31d4a-114">PARAMETERS</span></span>

### <span data-ttu-id="31d4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d4a-115">-DefaultProfile</span></span>
<span data-ttu-id="31d4a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31d4a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31d4a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="31d4a-117">-Force</span></span>
<span data-ttu-id="31d4a-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="31d4a-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="31d4a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31d4a-119">-InputObject</span></span>
<span data-ttu-id="31d4a-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="31d4a-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31d4a-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="31d4a-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="31d4a-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="31d4a-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31d4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="31d4a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31d4a-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d4a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31d4a-125">-ResourceId</span></span>
<span data-ttu-id="31d4a-126">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="31d4a-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d4a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31d4a-127">-WorkspaceName</span></span>
<span data-ttu-id="31d4a-128">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="31d4a-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d4a-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31d4a-129">-WorkspaceObject</span></span>
<span data-ttu-id="31d4a-130">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="31d4a-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31d4a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31d4a-131">-Confirm</span></span>
<span data-ttu-id="31d4a-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31d4a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31d4a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31d4a-133">-WhatIf</span></span>
<span data-ttu-id="31d4a-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31d4a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31d4a-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31d4a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31d4a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d4a-136">CommonParameters</span></span>
<span data-ttu-id="31d4a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31d4a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d4a-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31d4a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d4a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31d4a-139">INPUTS</span></span>

### <span data-ttu-id="31d4a-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="31d4a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="31d4a-141">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="31d4a-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="31d4a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31d4a-142">OUTPUTS</span></span>

### <span data-ttu-id="31d4a-143">System. void</span><span class="sxs-lookup"><span data-stu-id="31d4a-143">System.Void</span></span>

## <span data-ttu-id="31d4a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="31d4a-144">NOTES</span></span>

## <span data-ttu-id="31d4a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31d4a-145">RELATED LINKS</span></span>
