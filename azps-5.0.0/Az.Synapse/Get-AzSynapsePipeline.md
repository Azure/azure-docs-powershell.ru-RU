---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248455"
---
# <span data-ttu-id="e413c-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="e413c-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="e413c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e413c-102">SYNOPSIS</span></span>
<span data-ttu-id="e413c-103">Получение сведений о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e413c-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="e413c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e413c-104">SYNTAX</span></span>

### <span data-ttu-id="e413c-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e413c-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e413c-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="e413c-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e413c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e413c-107">DESCRIPTION</span></span>
<span data-ttu-id="e413c-108">Командлет **Get-AzSynapsePipeline** получает сведения о конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e413c-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="e413c-109">Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.</span><span class="sxs-lookup"><span data-stu-id="e413c-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="e413c-110">Если имя не задано, этот командлет получает сведения обо всех конвейерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e413c-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="e413c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e413c-111">EXAMPLES</span></span>

### <span data-ttu-id="e413c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e413c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e413c-113">Эта команда получает сведения обо всех конвейерах в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e413c-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e413c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e413c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="e413c-115">Эта команда получает сведения о конвейере с именем ContosoPipeline в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e413c-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e413c-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e413c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="e413c-117">Эта команда получает сведения о конвейере с именем ContosoPipeline в рабочей области с именем ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e413c-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e413c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e413c-118">PARAMETERS</span></span>

### <span data-ttu-id="e413c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e413c-119">-DefaultProfile</span></span>
<span data-ttu-id="e413c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e413c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e413c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e413c-121">-Name</span></span>
<span data-ttu-id="e413c-122">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="e413c-122">The pipeline name.</span></span>

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

### <span data-ttu-id="e413c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e413c-123">-WorkspaceName</span></span>
<span data-ttu-id="e413c-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e413c-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e413c-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e413c-125">-WorkspaceObject</span></span>
<span data-ttu-id="e413c-126">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e413c-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e413c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e413c-127">CommonParameters</span></span>
<span data-ttu-id="e413c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e413c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e413c-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e413c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e413c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e413c-130">INPUTS</span></span>

### <span data-ttu-id="e413c-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e413c-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e413c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e413c-132">OUTPUTS</span></span>

### <span data-ttu-id="e413c-133">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="e413c-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="e413c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e413c-134">NOTES</span></span>

## <span data-ttu-id="e413c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e413c-135">RELATED LINKS</span></span>
