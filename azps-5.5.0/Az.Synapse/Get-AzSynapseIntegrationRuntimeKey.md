---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216868"
---
# <span data-ttu-id="490d3-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="490d3-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="490d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="490d3-102">SYNOPSIS</span></span>
<span data-ttu-id="490d3-103">Ключи для самостоятельной интеграции во время работы.</span><span class="sxs-lookup"><span data-stu-id="490d3-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="490d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="490d3-104">SYNTAX</span></span>

### <span data-ttu-id="490d3-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="490d3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490d3-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="490d3-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490d3-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="490d3-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="490d3-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="490d3-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="490d3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="490d3-109">DESCRIPTION</span></span>
<span data-ttu-id="490d3-110">Для интеграции runtime можно получить ключи от **cmdlet Get-AzSynapseIntegrationRuntimeKey.**</span><span class="sxs-lookup"><span data-stu-id="490d3-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="490d3-111">Ключи используются для регистрации узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="490d3-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="490d3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="490d3-112">EXAMPLES</span></span>

### <span data-ttu-id="490d3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="490d3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="490d3-114">Он извлекает ключи для интеграции с именем test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="490d3-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="490d3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="490d3-115">PARAMETERS</span></span>

### <span data-ttu-id="490d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490d3-116">-DefaultProfile</span></span>
<span data-ttu-id="490d3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="490d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="490d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="490d3-118">-InputObject</span></span>
<span data-ttu-id="490d3-119">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="490d3-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="490d3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="490d3-120">-Name</span></span>
<span data-ttu-id="490d3-121">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="490d3-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="490d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="490d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="490d3-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="490d3-123">Resource group name.</span></span>

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

### <span data-ttu-id="490d3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="490d3-124">-ResourceId</span></span>
<span data-ttu-id="490d3-125">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="490d3-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="490d3-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="490d3-126">-WorkspaceName</span></span>
<span data-ttu-id="490d3-127">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="490d3-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="490d3-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="490d3-128">-WorkspaceObject</span></span>
<span data-ttu-id="490d3-129">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="490d3-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="490d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490d3-130">CommonParameters</span></span>
<span data-ttu-id="490d3-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490d3-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="490d3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490d3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="490d3-133">INPUTS</span></span>

### <span data-ttu-id="490d3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="490d3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="490d3-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="490d3-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="490d3-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="490d3-136">OUTPUTS</span></span>

### <span data-ttu-id="490d3-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="490d3-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="490d3-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="490d3-138">NOTES</span></span>

## <span data-ttu-id="490d3-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="490d3-139">RELATED LINKS</span></span>
