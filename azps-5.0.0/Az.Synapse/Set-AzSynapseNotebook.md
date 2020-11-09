---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseNotebook.md
ms.openlocfilehash: da4907200bef198afa1d57b51069c6379d28c8f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318194"
---
# <span data-ttu-id="60baf-101">Set-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="60baf-101">Set-AzSynapseNotebook</span></span>

## <span data-ttu-id="60baf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60baf-102">SYNOPSIS</span></span>
<span data-ttu-id="60baf-103">Создание или обновление записной книжки в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="60baf-103">Creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="60baf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60baf-104">SYNTAX</span></span>

### <span data-ttu-id="60baf-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60baf-105">SetByName (Default)</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60baf-106">SetByNameAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="60baf-106">SetByNameAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -SparkPoolName <String> [-ExecutorSize <String>]
 -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60baf-107">SetByObject</span><span class="sxs-lookup"><span data-stu-id="60baf-107">SetByObject</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60baf-108">SetByObjectAndSparkPool</span><span class="sxs-lookup"><span data-stu-id="60baf-108">SetByObjectAndSparkPool</span></span>
```
Set-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -SparkPoolName <String>
 [-ExecutorSize <String>] -ExecutorCount <Int32> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60baf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60baf-109">DESCRIPTION</span></span>
<span data-ttu-id="60baf-110">Командлет **Set-AzSynapseNotebook** создает или обновляет записную книжку в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="60baf-110">The **Set-AzSynapseNotebook** cmdlet creates or updates a notebook in a workspace.</span></span>

## <span data-ttu-id="60baf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60baf-111">EXAMPLES</span></span>

### <span data-ttu-id="60baf-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60baf-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb"

    WorkspaceName : ContosoWorkspace
    Properties    : Microsoft.Azure.Commands.Synapse.Models.PSNotebook
    Name          : notebook
```

<span data-ttu-id="60baf-113">Эта команда создает или обновляет записную книжку из записной книжки для файла записной книжкы. ipynb в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="60baf-113">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="60baf-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="60baf-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseNotebook -DefinitionFile "C:\\samples\\notebook.ipynb"
```

<span data-ttu-id="60baf-115">Эта команда создает или обновляет записную книжку из записной книжки файлового файла. ipynb в рабочей области с именем ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="60baf-115">This command creates or updates a notebook from notebook file notebook.ipynb in the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="60baf-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="60baf-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseNotebook -WorkspaceName ContosoWorkspace -DefinitionFile "C:\\samples\\notebook.ipynb" -SparkPoolName ContosoSparkPool -ExecutorCount 2
```

<span data-ttu-id="60baf-117">Эта команда позволяет создать или обновить записную книжку из записной книжки записной книжкы. ipynb, которая вкладывается в ContosoSparkPool и использует 2 исполнителя в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="60baf-117">This command creates or updates a notebook from notebook file notebook.ipynb which attaches to ContosoSparkPool and uses 2 executors in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="60baf-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60baf-118">PARAMETERS</span></span>

### <span data-ttu-id="60baf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60baf-119">-AsJob</span></span>
<span data-ttu-id="60baf-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="60baf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60baf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60baf-121">-DefaultProfile</span></span>
<span data-ttu-id="60baf-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60baf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60baf-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="60baf-123">-DefinitionFile</span></span>
<span data-ttu-id="60baf-124">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="60baf-124">The JSON file path.</span></span>

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

### <span data-ttu-id="60baf-125">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="60baf-125">-ExecutorCount</span></span>
<span data-ttu-id="60baf-126">Количество исполнителей, которые должны быть выделены в указанном пуле Spark для задания.</span><span class="sxs-lookup"><span data-stu-id="60baf-126">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="60baf-127">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="60baf-127">-ExecutorSize</span></span>
<span data-ttu-id="60baf-128">Число ядер и памяти, используемых для исполнителей, выделенных в указанном пуле Spark для задания.</span><span class="sxs-lookup"><span data-stu-id="60baf-128">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="60baf-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="60baf-129">-Name</span></span>
<span data-ttu-id="60baf-130">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="60baf-130">The notebook name.</span></span>

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

### <span data-ttu-id="60baf-131">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="60baf-131">-SparkPoolName</span></span>
<span data-ttu-id="60baf-132">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="60baf-132">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="60baf-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="60baf-133">-WorkspaceName</span></span>
<span data-ttu-id="60baf-134">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="60baf-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="60baf-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="60baf-135">-WorkspaceObject</span></span>
<span data-ttu-id="60baf-136">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="60baf-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="60baf-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60baf-137">-Confirm</span></span>
<span data-ttu-id="60baf-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60baf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60baf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60baf-139">-WhatIf</span></span>
<span data-ttu-id="60baf-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60baf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60baf-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60baf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60baf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60baf-142">CommonParameters</span></span>
<span data-ttu-id="60baf-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60baf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60baf-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60baf-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60baf-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60baf-145">INPUTS</span></span>

### <span data-ttu-id="60baf-146">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="60baf-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="60baf-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60baf-147">OUTPUTS</span></span>

### <span data-ttu-id="60baf-148">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="60baf-148">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="60baf-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="60baf-149">NOTES</span></span>

## <span data-ttu-id="60baf-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60baf-150">RELATED LINKS</span></span>
