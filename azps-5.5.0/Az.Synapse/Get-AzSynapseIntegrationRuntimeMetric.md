---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229700"
---
# <span data-ttu-id="53265-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="53265-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="53265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53265-102">SYNOPSIS</span></span>
<span data-ttu-id="53265-103">Получает метрические данные для интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="53265-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="53265-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53265-104">SYNTAX</span></span>

### <span data-ttu-id="53265-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53265-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53265-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53265-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53265-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53265-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53265-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53265-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53265-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53265-109">DESCRIPTION</span></span>
<span data-ttu-id="53265-110">Cmdlet **Get-AzSynapseIntegrationRuntimeMetric** получает метрические данные об интеграции рабочего времени в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="53265-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="53265-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53265-111">EXAMPLES</span></span>

### <span data-ttu-id="53265-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53265-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="53265-113">Эта команда отображает метрические данные об интегрированном рабочем времени "test-selfhost-ir" в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="53265-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="53265-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53265-114">PARAMETERS</span></span>

### <span data-ttu-id="53265-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53265-115">-DefaultProfile</span></span>
<span data-ttu-id="53265-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53265-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53265-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53265-117">-InputObject</span></span>
<span data-ttu-id="53265-118">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="53265-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="53265-119">-Name</span><span class="sxs-lookup"><span data-stu-id="53265-119">-Name</span></span>
<span data-ttu-id="53265-120">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="53265-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="53265-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53265-121">-ResourceGroupName</span></span>
<span data-ttu-id="53265-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53265-122">Resource group name.</span></span>

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

### <span data-ttu-id="53265-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53265-123">-ResourceId</span></span>
<span data-ttu-id="53265-124">Идентификатор ресурса для времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="53265-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="53265-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53265-125">-WorkspaceName</span></span>
<span data-ttu-id="53265-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="53265-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="53265-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53265-127">-WorkspaceObject</span></span>
<span data-ttu-id="53265-128">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="53265-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="53265-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53265-129">CommonParameters</span></span>
<span data-ttu-id="53265-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53265-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53265-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53265-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53265-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53265-132">INPUTS</span></span>

### <span data-ttu-id="53265-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53265-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="53265-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="53265-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="53265-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53265-135">OUTPUTS</span></span>

### <span data-ttu-id="53265-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="53265-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="53265-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53265-137">NOTES</span></span>

## <span data-ttu-id="53265-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53265-138">RELATED LINKS</span></span>
