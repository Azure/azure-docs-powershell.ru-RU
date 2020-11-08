---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235193"
---
# <span data-ttu-id="2cde1-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="2cde1-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="2cde1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cde1-102">SYNOPSIS</span></span>
<span data-ttu-id="2cde1-103">Обновляет среду интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="2cde1-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="2cde1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cde1-104">SYNTAX</span></span>

### <span data-ttu-id="2cde1-105">InvokeByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cde1-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cde1-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cde1-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cde1-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cde1-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cde1-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cde1-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cde1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cde1-109">DESCRIPTION</span></span>
<span data-ttu-id="2cde1-110">Командлет **Invoke-AzSynapseIntegrationRuntimeUpgrade** обновляет саморазмещенную среду интеграции, если доступна новая версия.</span><span class="sxs-lookup"><span data-stu-id="2cde1-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="2cde1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cde1-111">EXAMPLES</span></span>

### <span data-ttu-id="2cde1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cde1-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="2cde1-113">Командлет обновляет самостоятельную среду интеграции с именем Test-SelfHost-IR в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2cde1-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="2cde1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cde1-114">PARAMETERS</span></span>

### <span data-ttu-id="2cde1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cde1-115">-DefaultProfile</span></span>
<span data-ttu-id="2cde1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cde1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cde1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cde1-117">-InputObject</span></span>
<span data-ttu-id="2cde1-118">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="2cde1-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cde1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2cde1-119">-Name</span></span>
<span data-ttu-id="2cde1-120">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2cde1-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cde1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cde1-121">-ResourceGroupName</span></span>
<span data-ttu-id="2cde1-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cde1-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cde1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cde1-123">-ResourceId</span></span>
<span data-ttu-id="2cde1-124">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="2cde1-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cde1-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2cde1-125">-WorkspaceName</span></span>
<span data-ttu-id="2cde1-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2cde1-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cde1-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2cde1-127">-WorkspaceObject</span></span>
<span data-ttu-id="2cde1-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="2cde1-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cde1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cde1-129">-Confirm</span></span>
<span data-ttu-id="2cde1-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cde1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cde1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cde1-131">-WhatIf</span></span>
<span data-ttu-id="2cde1-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cde1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cde1-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cde1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cde1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cde1-134">CommonParameters</span></span>
<span data-ttu-id="2cde1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cde1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cde1-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cde1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cde1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cde1-137">INPUTS</span></span>

### <span data-ttu-id="2cde1-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2cde1-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2cde1-139">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2cde1-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2cde1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cde1-140">OUTPUTS</span></span>

### <span data-ttu-id="2cde1-141">System. void</span><span class="sxs-lookup"><span data-stu-id="2cde1-141">System.Void</span></span>

## <span data-ttu-id="2cde1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cde1-142">NOTES</span></span>

## <span data-ttu-id="2cde1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cde1-143">RELATED LINKS</span></span>
