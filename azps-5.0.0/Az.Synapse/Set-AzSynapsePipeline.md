---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: 2bce821f55b5f8ff39f56fa8a6960cb1f99b47d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247905"
---
# <span data-ttu-id="c97cf-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="c97cf-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="c97cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c97cf-102">SYNOPSIS</span></span>
<span data-ttu-id="c97cf-103">Создание конвейера в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c97cf-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="c97cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c97cf-104">SYNTAX</span></span>

### <span data-ttu-id="c97cf-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c97cf-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97cf-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="c97cf-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c97cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c97cf-107">DESCRIPTION</span></span>
<span data-ttu-id="c97cf-108">Командлет **Set-AzSynapsePipeline** создает конвейер в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c97cf-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="c97cf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c97cf-109">EXAMPLES</span></span>

### <span data-ttu-id="c97cf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c97cf-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="c97cf-111">Эта команда создает конвейер с именем ContosoPipeline в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c97cf-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="c97cf-112">Команда основывается на сведениях в pipeline.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="c97cf-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="c97cf-113">Этот файл содержит сведения о действиях.</span><span class="sxs-lookup"><span data-stu-id="c97cf-113">This file includes information about activities.</span></span>

### <span data-ttu-id="c97cf-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c97cf-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="c97cf-115">Эта команда создает конвейер с именем ContosoPipeline в рабочей области с именем ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="c97cf-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="c97cf-116">Команда основывается на сведениях в pipeline.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="c97cf-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="c97cf-117">Этот файл содержит сведения о действиях.</span><span class="sxs-lookup"><span data-stu-id="c97cf-117">This file includes information about activities.</span></span>

## <span data-ttu-id="c97cf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c97cf-118">PARAMETERS</span></span>

### <span data-ttu-id="c97cf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c97cf-119">-AsJob</span></span>
<span data-ttu-id="c97cf-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c97cf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c97cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97cf-121">-DefaultProfile</span></span>
<span data-ttu-id="c97cf-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c97cf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97cf-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c97cf-123">-DefinitionFile</span></span>
<span data-ttu-id="c97cf-124">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="c97cf-124">The JSON file path.</span></span>

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

### <span data-ttu-id="c97cf-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c97cf-125">-Name</span></span>
<span data-ttu-id="c97cf-126">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="c97cf-126">The pipeline name.</span></span>

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

### <span data-ttu-id="c97cf-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c97cf-127">-WorkspaceName</span></span>
<span data-ttu-id="c97cf-128">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c97cf-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c97cf-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c97cf-129">-WorkspaceObject</span></span>
<span data-ttu-id="c97cf-130">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c97cf-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c97cf-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c97cf-131">-Confirm</span></span>
<span data-ttu-id="c97cf-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c97cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97cf-133">-WhatIf</span></span>
<span data-ttu-id="c97cf-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c97cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97cf-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c97cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97cf-136">CommonParameters</span></span>
<span data-ttu-id="c97cf-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c97cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97cf-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c97cf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97cf-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c97cf-139">INPUTS</span></span>

### <span data-ttu-id="c97cf-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c97cf-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c97cf-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c97cf-141">OUTPUTS</span></span>

### <span data-ttu-id="c97cf-142">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="c97cf-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="c97cf-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c97cf-143">NOTES</span></span>

## <span data-ttu-id="c97cf-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c97cf-144">RELATED LINKS</span></span>
