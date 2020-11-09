---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317534"
---
# <span data-ttu-id="50cd5-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="50cd5-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="50cd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="50cd5-103">Возвращает данные метрик для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="50cd5-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="50cd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50cd5-104">SYNTAX</span></span>

### <span data-ttu-id="50cd5-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50cd5-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50cd5-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50cd5-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50cd5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50cd5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50cd5-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50cd5-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50cd5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50cd5-109">DESCRIPTION</span></span>
<span data-ttu-id="50cd5-110">Командлет **Get-AzSynapseIntegrationRuntimeMetric** получает данные метрик о среде выполнения интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="50cd5-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="50cd5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50cd5-111">EXAMPLES</span></span>

### <span data-ttu-id="50cd5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50cd5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="50cd5-113">Эта команда отображает данные метрик о среде выполнения интеграции с именем Test-SelfHost-IR в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="50cd5-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="50cd5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50cd5-114">PARAMETERS</span></span>

### <span data-ttu-id="50cd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cd5-115">-DefaultProfile</span></span>
<span data-ttu-id="50cd5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50cd5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50cd5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50cd5-117">-InputObject</span></span>
<span data-ttu-id="50cd5-118">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="50cd5-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="50cd5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50cd5-119">-Name</span></span>
<span data-ttu-id="50cd5-120">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="50cd5-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cd5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cd5-121">-ResourceGroupName</span></span>
<span data-ttu-id="50cd5-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50cd5-122">Resource group name.</span></span>

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

### <span data-ttu-id="50cd5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50cd5-123">-ResourceId</span></span>
<span data-ttu-id="50cd5-124">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="50cd5-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="50cd5-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50cd5-125">-WorkspaceName</span></span>
<span data-ttu-id="50cd5-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="50cd5-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="50cd5-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="50cd5-127">-WorkspaceObject</span></span>
<span data-ttu-id="50cd5-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="50cd5-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="50cd5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cd5-129">CommonParameters</span></span>
<span data-ttu-id="50cd5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50cd5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cd5-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50cd5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cd5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50cd5-132">INPUTS</span></span>

### <span data-ttu-id="50cd5-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="50cd5-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="50cd5-134">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="50cd5-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="50cd5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50cd5-135">OUTPUTS</span></span>

### <span data-ttu-id="50cd5-136">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="50cd5-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="50cd5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="50cd5-137">NOTES</span></span>

## <span data-ttu-id="50cd5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50cd5-138">RELATED LINKS</span></span>
