---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6161a0ca463973fad1ac7bac5df6487cf23cd0e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967192"
---
# <span data-ttu-id="b9c73-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="b9c73-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="b9c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c73-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c73-103">Сведения о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b9c73-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="b9c73-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9c73-104">SYNTAX</span></span>

### <span data-ttu-id="b9c73-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9c73-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c73-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b9c73-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c73-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9c73-107">DESCRIPTION</span></span>
<span data-ttu-id="b9c73-108">Для получения сведений о конвейерах в рабочей области возвращается **cmdlet Get-AzSynapsePipeline.**</span><span class="sxs-lookup"><span data-stu-id="b9c73-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="b9c73-109">Если указать имя конвейера, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="b9c73-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="b9c73-110">Если имя не указано, этот cmdlet получает сведения обо всех конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b9c73-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="b9c73-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9c73-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c73-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9c73-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b9c73-113">Эта команда получает сведения обо всех конвейерах в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b9c73-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b9c73-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b9c73-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="b9c73-115">Эта команда получает сведения о конвейере ContosoPipeline в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b9c73-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b9c73-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b9c73-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="b9c73-117">Эта команда получает сведения о конвейере ContosoPipeline в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="b9c73-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b9c73-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9c73-118">PARAMETERS</span></span>

### <span data-ttu-id="b9c73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c73-119">-DefaultProfile</span></span>
<span data-ttu-id="b9c73-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c73-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b9c73-121">-Name</span></span>
<span data-ttu-id="b9c73-122">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="b9c73-122">The pipeline name.</span></span>

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

### <span data-ttu-id="b9c73-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9c73-123">-WorkspaceName</span></span>
<span data-ttu-id="b9c73-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="b9c73-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9c73-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9c73-125">-WorkspaceObject</span></span>
<span data-ttu-id="b9c73-126">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b9c73-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9c73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c73-127">CommonParameters</span></span>
<span data-ttu-id="b9c73-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c73-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9c73-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c73-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9c73-130">INPUTS</span></span>

### <span data-ttu-id="b9c73-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9c73-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b9c73-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9c73-132">OUTPUTS</span></span>

### <span data-ttu-id="b9c73-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="b9c73-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="b9c73-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9c73-134">NOTES</span></span>

## <span data-ttu-id="b9c73-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9c73-135">RELATED LINKS</span></span>
