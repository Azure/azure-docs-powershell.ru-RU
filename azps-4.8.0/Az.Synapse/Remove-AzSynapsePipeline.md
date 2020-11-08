---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079909"
---
# <span data-ttu-id="c25d9-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="c25d9-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="c25d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c25d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c25d9-103">Удаляет канал из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c25d9-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="c25d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c25d9-104">SYNTAX</span></span>

### <span data-ttu-id="c25d9-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c25d9-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25d9-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c25d9-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25d9-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="c25d9-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c25d9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c25d9-108">DESCRIPTION</span></span>
<span data-ttu-id="c25d9-109">Командлет **Remove-AzSynapsePipeline** удаляет канал из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c25d9-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="c25d9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c25d9-110">EXAMPLES</span></span>

### <span data-ttu-id="c25d9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c25d9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="c25d9-112">Этот командлет удаляет конвейер с именем ContosoPipeline из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c25d9-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c25d9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c25d9-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="c25d9-114">Этот командлет удаляет конвейер с именем ContosoPipeline из рабочей области с именем ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c25d9-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c25d9-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c25d9-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="c25d9-116">Этот командлет удаляет конвейер с именем ContosoPipeline из рабочей области с именем ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c25d9-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c25d9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c25d9-117">PARAMETERS</span></span>

### <span data-ttu-id="c25d9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c25d9-118">-AsJob</span></span>
<span data-ttu-id="c25d9-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c25d9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c25d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25d9-120">-DefaultProfile</span></span>
<span data-ttu-id="c25d9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c25d9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25d9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c25d9-122">-InputObject</span></span>
<span data-ttu-id="c25d9-123">Объект конвейера.</span><span class="sxs-lookup"><span data-stu-id="c25d9-123">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c25d9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c25d9-124">-Name</span></span>
<span data-ttu-id="c25d9-125">Имя конвейера.</span><span class="sxs-lookup"><span data-stu-id="c25d9-125">The pipeline name.</span></span>

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

### <span data-ttu-id="c25d9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c25d9-126">-PassThru</span></span>
<span data-ttu-id="c25d9-127">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c25d9-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c25d9-128">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="c25d9-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c25d9-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c25d9-129">-WorkspaceName</span></span>
<span data-ttu-id="c25d9-130">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c25d9-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c25d9-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c25d9-131">-WorkspaceObject</span></span>
<span data-ttu-id="c25d9-132">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c25d9-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c25d9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c25d9-133">-Confirm</span></span>
<span data-ttu-id="c25d9-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c25d9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25d9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25d9-135">-WhatIf</span></span>
<span data-ttu-id="c25d9-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c25d9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25d9-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c25d9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25d9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25d9-138">CommonParameters</span></span>
<span data-ttu-id="c25d9-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c25d9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25d9-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c25d9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25d9-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c25d9-141">INPUTS</span></span>

### <span data-ttu-id="c25d9-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c25d9-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c25d9-143">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="c25d9-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="c25d9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c25d9-144">OUTPUTS</span></span>

### <span data-ttu-id="c25d9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c25d9-145">System.Boolean</span></span>

## <span data-ttu-id="c25d9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c25d9-146">NOTES</span></span>

## <span data-ttu-id="c25d9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c25d9-147">RELATED LINKS</span></span>
