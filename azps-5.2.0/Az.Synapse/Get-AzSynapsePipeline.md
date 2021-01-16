---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397244"
---
# <span data-ttu-id="e37aa-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="e37aa-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="e37aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e37aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e37aa-103">Сведения о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e37aa-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="e37aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e37aa-104">SYNTAX</span></span>

### <span data-ttu-id="e37aa-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e37aa-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e37aa-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="e37aa-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e37aa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e37aa-107">DESCRIPTION</span></span>
<span data-ttu-id="e37aa-108">Для получения сведений о конвейерах в рабочей области возвращается **cmdlet Get-AzSynapsePipeline.**</span><span class="sxs-lookup"><span data-stu-id="e37aa-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="e37aa-109">Если указать имя конвейера, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="e37aa-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="e37aa-110">Если имя не указано, этот cmdlet получает сведения обо всех конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e37aa-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="e37aa-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e37aa-111">EXAMPLES</span></span>

### <span data-ttu-id="e37aa-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e37aa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e37aa-113">Эта команда получает сведения обо всех конвейерах в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e37aa-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e37aa-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e37aa-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="e37aa-115">Эта команда получает сведения о конвейере ContosoPipeline в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e37aa-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e37aa-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e37aa-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="e37aa-117">Эта команда получает сведения о конвейере ContosoPipeline в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="e37aa-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e37aa-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e37aa-118">PARAMETERS</span></span>

### <span data-ttu-id="e37aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e37aa-119">-DefaultProfile</span></span>
<span data-ttu-id="e37aa-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e37aa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e37aa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e37aa-121">-Name</span></span>
<span data-ttu-id="e37aa-122">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="e37aa-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37aa-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e37aa-123">-WorkspaceName</span></span>
<span data-ttu-id="e37aa-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="e37aa-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e37aa-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e37aa-125">-WorkspaceObject</span></span>
<span data-ttu-id="e37aa-126">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e37aa-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e37aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e37aa-127">CommonParameters</span></span>
<span data-ttu-id="e37aa-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e37aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e37aa-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e37aa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e37aa-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e37aa-130">INPUTS</span></span>

### <span data-ttu-id="e37aa-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e37aa-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e37aa-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e37aa-132">OUTPUTS</span></span>

### <span data-ttu-id="e37aa-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="e37aa-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="e37aa-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e37aa-134">NOTES</span></span>

## <span data-ttu-id="e37aa-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e37aa-135">RELATED LINKS</span></span>
