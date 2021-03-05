---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963459"
---
# <span data-ttu-id="ddbe5-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="ddbe5-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="ddbe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddbe5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbe5-103">Удаляет набор данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="ddbe5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ddbe5-104">SYNTAX</span></span>

### <span data-ttu-id="ddbe5-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddbe5-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddbe5-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ddbe5-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddbe5-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="ddbe5-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddbe5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddbe5-108">DESCRIPTION</span></span>
<span data-ttu-id="ddbe5-109">Чтобы **удалить набор данных** из рабочей области, удалите его из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="ddbe5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ddbe5-110">EXAMPLES</span></span>

### <span data-ttu-id="ddbe5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddbe5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="ddbe5-112">Эта команда удаляет набор данных ContosoDataset из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ddbe5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddbe5-113">PARAMETERS</span></span>

### <span data-ttu-id="ddbe5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddbe5-114">-AsJob</span></span>
<span data-ttu-id="ddbe5-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ddbe5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddbe5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbe5-116">-DefaultProfile</span></span>
<span data-ttu-id="ddbe5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddbe5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ddbe5-118">-Force</span></span>
<span data-ttu-id="ddbe5-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ddbe5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddbe5-120">-InputObject</span></span>
<span data-ttu-id="ddbe5-121">Объект наборов данных.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbe5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ddbe5-122">-Name</span></span>
<span data-ttu-id="ddbe5-123">Имя наборов данных.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddbe5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddbe5-124">-PassThru</span></span>
<span data-ttu-id="ddbe5-125">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ddbe5-126">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ddbe5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ddbe5-127">-WorkspaceName</span></span>
<span data-ttu-id="ddbe5-128">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ddbe5-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ddbe5-129">-WorkspaceObject</span></span>
<span data-ttu-id="ddbe5-130">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ddbe5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddbe5-131">-Confirm</span></span>
<span data-ttu-id="ddbe5-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbe5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbe5-133">-WhatIf</span></span>
<span data-ttu-id="ddbe5-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddbe5-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddbe5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbe5-136">CommonParameters</span></span>
<span data-ttu-id="ddbe5-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbe5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbe5-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddbe5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbe5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddbe5-139">INPUTS</span></span>

### <span data-ttu-id="ddbe5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ddbe5-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ddbe5-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="ddbe5-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="ddbe5-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ddbe5-142">OUTPUTS</span></span>

### <span data-ttu-id="ddbe5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddbe5-143">System.Boolean</span></span>

## <span data-ttu-id="ddbe5-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ddbe5-144">NOTES</span></span>

## <span data-ttu-id="ddbe5-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddbe5-145">RELATED LINKS</span></span>
