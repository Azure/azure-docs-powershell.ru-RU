---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232401"
---
# <span data-ttu-id="4983f-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="4983f-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="4983f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4983f-102">SYNOPSIS</span></span>
<span data-ttu-id="4983f-103">Создает или обновляет набор данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4983f-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="4983f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4983f-104">SYNTAX</span></span>

### <span data-ttu-id="4983f-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4983f-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4983f-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="4983f-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4983f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4983f-107">DESCRIPTION</span></span>
<span data-ttu-id="4983f-108">Для создания или обновления существующего набора данных в рабочей области будет создан или обновлен набор данных **Set-AzSynapseDataset.**</span><span class="sxs-lookup"><span data-stu-id="4983f-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="4983f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4983f-109">EXAMPLES</span></span>

### <span data-ttu-id="4983f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4983f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="4983f-111">Эта команда создает набор данных ContosoDataset в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4983f-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="4983f-112">Эта команда будет базой данных на данных из Dataset.jsфайла.</span><span class="sxs-lookup"><span data-stu-id="4983f-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="4983f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4983f-113">PARAMETERS</span></span>

### <span data-ttu-id="4983f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4983f-114">-AsJob</span></span>
<span data-ttu-id="4983f-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4983f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4983f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4983f-116">-DefaultProfile</span></span>
<span data-ttu-id="4983f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4983f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4983f-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4983f-118">-DefinitionFile</span></span>
<span data-ttu-id="4983f-119">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="4983f-119">The JSON file path.</span></span>

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

### <span data-ttu-id="4983f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4983f-120">-Name</span></span>
<span data-ttu-id="4983f-121">Имя наборов данных.</span><span class="sxs-lookup"><span data-stu-id="4983f-121">The dataset name.</span></span>

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

### <span data-ttu-id="4983f-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4983f-122">-WorkspaceName</span></span>
<span data-ttu-id="4983f-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="4983f-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4983f-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4983f-124">-WorkspaceObject</span></span>
<span data-ttu-id="4983f-125">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="4983f-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4983f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4983f-126">-Confirm</span></span>
<span data-ttu-id="4983f-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4983f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4983f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4983f-128">-WhatIf</span></span>
<span data-ttu-id="4983f-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4983f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4983f-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4983f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4983f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4983f-131">CommonParameters</span></span>
<span data-ttu-id="4983f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4983f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4983f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4983f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4983f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4983f-134">INPUTS</span></span>

### <span data-ttu-id="4983f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4983f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4983f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4983f-136">OUTPUTS</span></span>

### <span data-ttu-id="4983f-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="4983f-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="4983f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4983f-138">NOTES</span></span>

## <span data-ttu-id="4983f-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4983f-139">RELATED LINKS</span></span>
