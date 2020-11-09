---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317528"
---
# <span data-ttu-id="abd9e-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="abd9e-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="abd9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abd9e-102">SYNOPSIS</span></span>
<span data-ttu-id="abd9e-103">Получает сведения о узле среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="abd9e-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="abd9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abd9e-104">SYNTAX</span></span>

### <span data-ttu-id="abd9e-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="abd9e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abd9e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd9e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abd9e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd9e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abd9e-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd9e-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd9e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd9e-109">DESCRIPTION</span></span>
<span data-ttu-id="abd9e-110">Командлет **Get-AzSynapseIntegrationRuntimeNode** получает подробные сведения об узле среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="abd9e-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="abd9e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abd9e-111">EXAMPLES</span></span>

### <span data-ttu-id="abd9e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="abd9e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="abd9e-113">Командлет получает сведения о узле "Node_1" в саморазмещенной среде выполнения Test-SelfHost-IR в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="abd9e-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="abd9e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="abd9e-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="abd9e-115">Командлет получает сведения о узле с именем "Node_1" в исполняющей среде для самообслуживания интеграции "Test-SelfHost-IR" в рабочей области "Test-DF-Eu2", включая IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="abd9e-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="abd9e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abd9e-116">PARAMETERS</span></span>

### <span data-ttu-id="abd9e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd9e-117">-DefaultProfile</span></span>
<span data-ttu-id="abd9e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abd9e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd9e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abd9e-119">-InputObject</span></span>
<span data-ttu-id="abd9e-120">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="abd9e-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="abd9e-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="abd9e-122">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd9e-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="abd9e-123">-IpAddress</span></span>
<span data-ttu-id="abd9e-124">IP-адрес узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd9e-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="abd9e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="abd9e-125">-Name</span></span>
<span data-ttu-id="abd9e-126">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="abd9e-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd9e-127">-ResourceGroupName</span></span>
<span data-ttu-id="abd9e-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="abd9e-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abd9e-129">-ResourceId</span></span>
<span data-ttu-id="abd9e-130">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="abd9e-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="abd9e-131">-WorkspaceName</span></span>
<span data-ttu-id="abd9e-132">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="abd9e-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="abd9e-133">-WorkspaceObject</span></span>
<span data-ttu-id="abd9e-134">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="abd9e-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abd9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd9e-135">CommonParameters</span></span>
<span data-ttu-id="abd9e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abd9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd9e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abd9e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd9e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abd9e-138">INPUTS</span></span>

### <span data-ttu-id="abd9e-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="abd9e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="abd9e-140">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abd9e-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="abd9e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd9e-141">OUTPUTS</span></span>

### <span data-ttu-id="abd9e-142">Microsoft. Azure. Commands. Synapse. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="abd9e-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="abd9e-143">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="abd9e-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="abd9e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="abd9e-144">NOTES</span></span>

## <span data-ttu-id="abd9e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abd9e-145">RELATED LINKS</span></span>
