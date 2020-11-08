---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243166"
---
# <span data-ttu-id="2078f-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="2078f-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="2078f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2078f-102">SYNOPSIS</span></span>
<span data-ttu-id="2078f-103">Возвращает данные метрик для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2078f-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="2078f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2078f-104">SYNTAX</span></span>

### <span data-ttu-id="2078f-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2078f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2078f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2078f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2078f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2078f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2078f-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2078f-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2078f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2078f-109">DESCRIPTION</span></span>
<span data-ttu-id="2078f-110">Командлет **Get-AzSynapseIntegrationRuntimeMetric** получает данные метрик о среде выполнения интеграции в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2078f-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="2078f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2078f-111">EXAMPLES</span></span>

### <span data-ttu-id="2078f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2078f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="2078f-113">Эта команда отображает данные метрик о среде выполнения интеграции с именем Test-SelfHost-IR в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2078f-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2078f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2078f-114">PARAMETERS</span></span>

### <span data-ttu-id="2078f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2078f-115">-DefaultProfile</span></span>
<span data-ttu-id="2078f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2078f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2078f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2078f-117">-InputObject</span></span>
<span data-ttu-id="2078f-118">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="2078f-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="2078f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2078f-119">-Name</span></span>
<span data-ttu-id="2078f-120">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2078f-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="2078f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2078f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2078f-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2078f-122">Resource group name.</span></span>

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

### <span data-ttu-id="2078f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2078f-123">-ResourceId</span></span>
<span data-ttu-id="2078f-124">Идентификатор ресурса среды выполнения интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="2078f-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="2078f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2078f-125">-WorkspaceName</span></span>
<span data-ttu-id="2078f-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2078f-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2078f-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2078f-127">-WorkspaceObject</span></span>
<span data-ttu-id="2078f-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="2078f-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2078f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2078f-129">CommonParameters</span></span>
<span data-ttu-id="2078f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2078f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2078f-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2078f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2078f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2078f-132">INPUTS</span></span>

### <span data-ttu-id="2078f-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2078f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2078f-134">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2078f-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2078f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2078f-135">OUTPUTS</span></span>

### <span data-ttu-id="2078f-136">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="2078f-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="2078f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="2078f-137">NOTES</span></span>

## <span data-ttu-id="2078f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2078f-138">RELATED LINKS</span></span>
