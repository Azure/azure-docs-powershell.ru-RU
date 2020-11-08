---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235697"
---
# <span data-ttu-id="2fcb3-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="2fcb3-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="2fcb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fcb3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcb3-103">Получение сведений о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="2fcb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fcb3-104">SYNTAX</span></span>

### <span data-ttu-id="2fcb3-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fcb3-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fcb3-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="2fcb3-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fcb3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fcb3-107">DESCRIPTION</span></span>
<span data-ttu-id="2fcb3-108">Командлет **Get-AzSynapsePipeline** получает сведения о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="2fcb3-109">Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="2fcb3-110">Если имя не задано, этот командлет получает сведения обо всех конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="2fcb3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fcb3-111">EXAMPLES</span></span>

### <span data-ttu-id="2fcb3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2fcb3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2fcb3-113">Эта команда получает сведения обо всех конвейерах в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2fcb3-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2fcb3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="2fcb3-115">Эта команда получает сведения о конвейере с именем ContosoPipeline в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="2fcb3-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2fcb3-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="2fcb3-117">Эта команда получает сведения о конвейере с именем ContosoPipeline в рабочей области с именем ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2fcb3-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fcb3-118">PARAMETERS</span></span>

### <span data-ttu-id="2fcb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fcb3-119">-DefaultProfile</span></span>
<span data-ttu-id="2fcb3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fcb3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fcb3-121">-Name</span></span>
<span data-ttu-id="2fcb3-122">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-122">The pipeline name.</span></span>

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

### <span data-ttu-id="2fcb3-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2fcb3-123">-WorkspaceName</span></span>
<span data-ttu-id="2fcb3-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2fcb3-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2fcb3-125">-WorkspaceObject</span></span>
<span data-ttu-id="2fcb3-126">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2fcb3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcb3-127">CommonParameters</span></span>
<span data-ttu-id="2fcb3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fcb3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcb3-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fcb3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcb3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fcb3-130">INPUTS</span></span>

### <span data-ttu-id="2fcb3-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2fcb3-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2fcb3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fcb3-132">OUTPUTS</span></span>

### <span data-ttu-id="2fcb3-133">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="2fcb3-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="2fcb3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fcb3-134">NOTES</span></span>

## <span data-ttu-id="2fcb3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fcb3-135">RELATED LINKS</span></span>