---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249747"
---
# <span data-ttu-id="e468f-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="e468f-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="e468f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e468f-102">SYNOPSIS</span></span>
<span data-ttu-id="e468f-103">Создание или обновление набора данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e468f-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="e468f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e468f-104">SYNTAX</span></span>

### <span data-ttu-id="e468f-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e468f-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e468f-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="e468f-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e468f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e468f-107">DESCRIPTION</span></span>
<span data-ttu-id="e468f-108">Командлет **Set-AzSynapseDataset** создает набор данных или обновляет существующий набор данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e468f-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="e468f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e468f-109">EXAMPLES</span></span>

### <span data-ttu-id="e468f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e468f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="e468f-111">Эта команда создает набор данных с именем ContosoDataset в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e468f-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="e468f-112">В команде набор данных заосновывается на сведениях в Dataset.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="e468f-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="e468f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e468f-113">PARAMETERS</span></span>

### <span data-ttu-id="e468f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e468f-114">-AsJob</span></span>
<span data-ttu-id="e468f-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e468f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e468f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e468f-116">-DefaultProfile</span></span>
<span data-ttu-id="e468f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e468f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e468f-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e468f-118">-DefinitionFile</span></span>
<span data-ttu-id="e468f-119">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="e468f-119">The JSON file path.</span></span>

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

### <span data-ttu-id="e468f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e468f-120">-Name</span></span>
<span data-ttu-id="e468f-121">Имя набора данных.</span><span class="sxs-lookup"><span data-stu-id="e468f-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e468f-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e468f-122">-WorkspaceName</span></span>
<span data-ttu-id="e468f-123">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e468f-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e468f-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e468f-124">-WorkspaceObject</span></span>
<span data-ttu-id="e468f-125">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e468f-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e468f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e468f-126">-Confirm</span></span>
<span data-ttu-id="e468f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e468f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e468f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e468f-128">-WhatIf</span></span>
<span data-ttu-id="e468f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e468f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e468f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e468f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e468f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e468f-131">CommonParameters</span></span>
<span data-ttu-id="e468f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e468f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e468f-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e468f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e468f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e468f-134">INPUTS</span></span>

### <span data-ttu-id="e468f-135">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e468f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e468f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e468f-136">OUTPUTS</span></span>

### <span data-ttu-id="e468f-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="e468f-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="e468f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e468f-138">NOTES</span></span>

## <span data-ttu-id="e468f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e468f-139">RELATED LINKS</span></span>
