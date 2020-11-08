---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 712aa1012269c6207b078fefa3a04a46bea4c573
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249289"
---
# <span data-ttu-id="7f9b0-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="7f9b0-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="7f9b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9b0-103">Удаляет набор данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="7f9b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f9b0-104">SYNTAX</span></span>

### <span data-ttu-id="7f9b0-105">RemoveByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f9b0-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9b0-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7f9b0-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f9b0-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7f9b0-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f9b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f9b0-108">DESCRIPTION</span></span>
<span data-ttu-id="7f9b0-109">Командлет **Remove-AzSynapseDataset** удаляет набор данных из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="7f9b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f9b0-110">EXAMPLES</span></span>

### <span data-ttu-id="7f9b0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f9b0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="7f9b0-112">Эта команда удаляет набор данных с именем ContosoDataset из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7f9b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f9b0-113">PARAMETERS</span></span>

### <span data-ttu-id="7f9b0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f9b0-114">-AsJob</span></span>
<span data-ttu-id="7f9b0-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7f9b0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f9b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9b0-116">-DefaultProfile</span></span>
<span data-ttu-id="7f9b0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f9b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f9b0-118">-InputObject</span></span>
<span data-ttu-id="7f9b0-119">Объект DataSet.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-119">The dataset object.</span></span>

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

### <span data-ttu-id="7f9b0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f9b0-120">-Name</span></span>
<span data-ttu-id="7f9b0-121">Имя набора данных.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-121">The dataset name.</span></span>

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

### <span data-ttu-id="7f9b0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f9b0-122">-PassThru</span></span>
<span data-ttu-id="7f9b0-123">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7f9b0-124">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7f9b0-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f9b0-125">-WorkspaceName</span></span>
<span data-ttu-id="7f9b0-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7f9b0-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7f9b0-127">-WorkspaceObject</span></span>
<span data-ttu-id="7f9b0-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7f9b0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f9b0-129">-Confirm</span></span>
<span data-ttu-id="7f9b0-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f9b0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9b0-131">-WhatIf</span></span>
<span data-ttu-id="7f9b0-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f9b0-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f9b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9b0-134">CommonParameters</span></span>
<span data-ttu-id="7f9b0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f9b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9b0-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f9b0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9b0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f9b0-137">INPUTS</span></span>

### <span data-ttu-id="7f9b0-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7f9b0-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7f9b0-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="7f9b0-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="7f9b0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f9b0-140">OUTPUTS</span></span>

### <span data-ttu-id="7f9b0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f9b0-141">System.Boolean</span></span>

## <span data-ttu-id="7f9b0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f9b0-142">NOTES</span></span>

## <span data-ttu-id="7f9b0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f9b0-143">RELATED LINKS</span></span>
