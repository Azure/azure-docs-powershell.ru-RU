---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222849"
---
# <span data-ttu-id="c8e44-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="c8e44-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="c8e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8e44-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e44-103">Создает или обновляет записную книжку в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c8e44-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="c8e44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8e44-104">SYNTAX</span></span>

### <span data-ttu-id="c8e44-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8e44-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e44-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="c8e44-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e44-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="c8e44-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8e44-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="c8e44-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8e44-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8e44-109">DESCRIPTION</span></span>
<span data-ttu-id="c8e44-110">Для создания или обновления записной книжки в рабочей области будет создан или обновлена **cmdlet Set-AzSynapseNotebook.**</span><span class="sxs-lookup"><span data-stu-id="c8e44-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="c8e44-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8e44-111">EXAMPLES</span></span>

### <span data-ttu-id="c8e44-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8e44-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="c8e44-113">Эта команда создает или обновляет записную книжку из файла записной книжки notebook.ipynb в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c8e44-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c8e44-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c8e44-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="c8e44-115">Эта команда создает или обновляет записную книжку из записной книжки notebook.ipynb в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="c8e44-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c8e44-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c8e44-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="c8e44-117">Эта команда создает или обновляет записную книжку из файла записной книжки notebook.ipynb, которая вложена в ContosoSparkPool и использует 2 исполняемого файла в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="c8e44-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="c8e44-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8e44-118">PARAMETERS</span></span>

### <span data-ttu-id="c8e44-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8e44-119">-AsJob</span></span>
<span data-ttu-id="c8e44-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c8e44-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8e44-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e44-121">-DefaultProfile</span></span>
<span data-ttu-id="c8e44-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e44-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8e44-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c8e44-123">-DefinitionFile</span></span>
<span data-ttu-id="c8e44-124">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="c8e44-124">The JSON file path.</span></span>

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

### <span data-ttu-id="c8e44-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="c8e44-125">-ExecutorCount</span></span>
<span data-ttu-id="c8e44-126">Количество исполнятелей, которые должны быть выделены в указанном пуле спарков для задания.</span><span class="sxs-lookup"><span data-stu-id="c8e44-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e44-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="c8e44-127">-ExecutorSize</span></span>
<span data-ttu-id="c8e44-128">Количество ядра и памяти, используемых для исполнятелей, выделенных в указанном пуле спарков для задания.</span><span class="sxs-lookup"><span data-stu-id="c8e44-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e44-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c8e44-129">-Name</span></span>
<span data-ttu-id="c8e44-130">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="c8e44-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e44-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c8e44-131">-SparkPoolName</span></span>
<span data-ttu-id="c8e44-132">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8e44-132">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndSparkPool, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e44-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c8e44-133">-WorkspaceName</span></span>
<span data-ttu-id="c8e44-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8e44-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8e44-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c8e44-135">-WorkspaceObject</span></span>
<span data-ttu-id="c8e44-136">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="c8e44-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject, SetByObjectAndSparkPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e44-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8e44-137">-Confirm</span></span>
<span data-ttu-id="c8e44-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c8e44-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8e44-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8e44-139">-WhatIf</span></span>
<span data-ttu-id="c8e44-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8e44-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8e44-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8e44-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8e44-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e44-142">CommonParameters</span></span>
<span data-ttu-id="c8e44-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e44-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e44-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8e44-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e44-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8e44-145">INPUTS</span></span>

### <span data-ttu-id="c8e44-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8e44-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c8e44-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8e44-147">OUTPUTS</span></span>

### <span data-ttu-id="c8e44-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="c8e44-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="c8e44-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8e44-149">NOTES</span></span>

## <span data-ttu-id="c8e44-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8e44-150">RELATED LINKS</span></span>
