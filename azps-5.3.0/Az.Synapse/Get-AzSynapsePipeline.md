---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424516"
---
# <span data-ttu-id="a6362-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="a6362-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="a6362-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6362-102">SYNOPSIS</span></span>
<span data-ttu-id="a6362-103">Сведения о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a6362-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="a6362-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6362-104">SYNTAX</span></span>

### <span data-ttu-id="a6362-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6362-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6362-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a6362-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6362-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6362-107">DESCRIPTION</span></span>
<span data-ttu-id="a6362-108">Для получения сведений о конвейерах в рабочей области возвращается **cmdlet Get-AzSynapsePipeline.**</span><span class="sxs-lookup"><span data-stu-id="a6362-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="a6362-109">Если указать имя конвейера, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="a6362-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="a6362-110">Если имя не указано, этот cmdlet получает сведения обо всех конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a6362-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="a6362-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6362-111">EXAMPLES</span></span>

### <span data-ttu-id="a6362-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6362-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a6362-113">Эта команда получает сведения обо всех конвейерах в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6362-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a6362-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6362-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="a6362-115">Эта команда получает сведения о конвейере ContosoPipeline в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a6362-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a6362-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a6362-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="a6362-117">Эта команда получает сведения о конвейере ContosoPipeline в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="a6362-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a6362-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6362-118">PARAMETERS</span></span>

### <span data-ttu-id="a6362-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6362-119">-DefaultProfile</span></span>
<span data-ttu-id="a6362-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6362-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6362-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a6362-121">-Name</span></span>
<span data-ttu-id="a6362-122">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="a6362-122">The pipeline name.</span></span>

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

### <span data-ttu-id="a6362-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a6362-123">-WorkspaceName</span></span>
<span data-ttu-id="a6362-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="a6362-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a6362-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a6362-125">-WorkspaceObject</span></span>
<span data-ttu-id="a6362-126">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="a6362-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a6362-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6362-127">CommonParameters</span></span>
<span data-ttu-id="a6362-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6362-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6362-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6362-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6362-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6362-130">INPUTS</span></span>

### <span data-ttu-id="a6362-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6362-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a6362-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6362-132">OUTPUTS</span></span>

### <span data-ttu-id="a6362-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="a6362-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="a6362-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6362-134">NOTES</span></span>

## <span data-ttu-id="a6362-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6362-135">RELATED LINKS</span></span>
