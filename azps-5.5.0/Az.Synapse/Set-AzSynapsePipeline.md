---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222841"
---
# <span data-ttu-id="6ab33-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="6ab33-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="6ab33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab33-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab33-103">Создает канал в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6ab33-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="6ab33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ab33-104">SYNTAX</span></span>

### <span data-ttu-id="6ab33-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ab33-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ab33-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="6ab33-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ab33-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ab33-107">DESCRIPTION</span></span>
<span data-ttu-id="6ab33-108">Для создания конвейера в рабочей области будет создан **cmdlet Set-AzSynapsePipeline.**</span><span class="sxs-lookup"><span data-stu-id="6ab33-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="6ab33-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ab33-109">EXAMPLES</span></span>

### <span data-ttu-id="6ab33-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ab33-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="6ab33-111">Эта команда создает канал ContosoPipeline в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6ab33-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="6ab33-112">Эта команда будет базой данных в канале, pipeline.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="6ab33-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="6ab33-113">Этот файл содержит сведения о действиях.</span><span class="sxs-lookup"><span data-stu-id="6ab33-113">This file includes information about activities.</span></span>

### <span data-ttu-id="6ab33-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6ab33-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="6ab33-115">Эта команда создает канал ContosoPipeline в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="6ab33-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="6ab33-116">Эта команда будет базой данных в канале, pipeline.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="6ab33-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="6ab33-117">Этот файл содержит сведения о действиях.</span><span class="sxs-lookup"><span data-stu-id="6ab33-117">This file includes information about activities.</span></span>

## <span data-ttu-id="6ab33-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ab33-118">PARAMETERS</span></span>

### <span data-ttu-id="6ab33-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ab33-119">-AsJob</span></span>
<span data-ttu-id="6ab33-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6ab33-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ab33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab33-121">-DefaultProfile</span></span>
<span data-ttu-id="6ab33-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab33-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab33-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6ab33-123">-DefinitionFile</span></span>
<span data-ttu-id="6ab33-124">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="6ab33-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab33-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6ab33-125">-Name</span></span>
<span data-ttu-id="6ab33-126">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="6ab33-126">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab33-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ab33-127">-WorkspaceName</span></span>
<span data-ttu-id="6ab33-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="6ab33-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab33-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6ab33-129">-WorkspaceObject</span></span>
<span data-ttu-id="6ab33-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="6ab33-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab33-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ab33-131">-Confirm</span></span>
<span data-ttu-id="6ab33-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab33-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab33-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab33-133">-WhatIf</span></span>
<span data-ttu-id="6ab33-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab33-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ab33-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ab33-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab33-136">CommonParameters</span></span>
<span data-ttu-id="6ab33-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab33-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ab33-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab33-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab33-139">INPUTS</span></span>

### <span data-ttu-id="6ab33-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6ab33-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6ab33-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ab33-141">OUTPUTS</span></span>

### <span data-ttu-id="6ab33-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="6ab33-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="6ab33-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ab33-143">NOTES</span></span>

## <span data-ttu-id="6ab33-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ab33-144">RELATED LINKS</span></span>
