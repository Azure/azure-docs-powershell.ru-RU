---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981864"
---
# <span data-ttu-id="b458a-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="b458a-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="b458a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b458a-102">SYNOPSIS</span></span>
<span data-ttu-id="b458a-103">Экспорт notbooks.</span><span class="sxs-lookup"><span data-stu-id="b458a-103">Exports notbooks.</span></span>

## <span data-ttu-id="b458a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b458a-104">SYNTAX</span></span>

### <span data-ttu-id="b458a-105">ExportByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b458a-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b458a-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="b458a-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b458a-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="b458a-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b458a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b458a-108">DESCRIPTION</span></span>
<span data-ttu-id="b458a-109">С **его** использованием можно экспортировать записную книжку Azure Synapse в файл записной книжки (IPYNB).</span><span class="sxs-lookup"><span data-stu-id="b458a-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="b458a-110">Имя записной книжки станет именем экспортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="b458a-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="b458a-111">Если указать имя записной книжки, будет экспортироваться ее стеб.</span><span class="sxs-lookup"><span data-stu-id="b458a-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="b458a-112">Если имя не указано, будет экспортироваться все записные книжки в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b458a-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="b458a-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b458a-113">EXAMPLES</span></span>

### <span data-ttu-id="b458a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b458a-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="b458a-115">Экспорт всех записных книг в рабочей области ContosoWorkspace в папку "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="b458a-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="b458a-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b458a-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="b458a-117">Экспорт одной записной книжки с названием ContosoNotebook в рабочей области ContosoWorkspace в папку "C:\Notebook".</span><span class="sxs-lookup"><span data-stu-id="b458a-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="b458a-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b458a-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="b458a-119">Экспорт записной книжки ContosoNotebook в рабочей области ContosoWorkspace в папку "C:\Notebook" через канал.</span><span class="sxs-lookup"><span data-stu-id="b458a-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="b458a-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b458a-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="b458a-121">Экспорт записной книжки ContosoNotebook в рабочей области ContosoWorkspace в папку "C:\Notebook" через канал.</span><span class="sxs-lookup"><span data-stu-id="b458a-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="b458a-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b458a-122">PARAMETERS</span></span>

### <span data-ttu-id="b458a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b458a-123">-AsJob</span></span>
<span data-ttu-id="b458a-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b458a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b458a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b458a-125">-DefaultProfile</span></span>
<span data-ttu-id="b458a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b458a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b458a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b458a-127">-InputObject</span></span>
<span data-ttu-id="b458a-128">Объект записной книжки.</span><span class="sxs-lookup"><span data-stu-id="b458a-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b458a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b458a-129">-Name</span></span>
<span data-ttu-id="b458a-130">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="b458a-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b458a-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="b458a-131">-OutputFolder</span></span>
<span data-ttu-id="b458a-132">Папка, в которой нужно поместить записную книжку.</span><span class="sxs-lookup"><span data-stu-id="b458a-132">The folder where the notebook should be placed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b458a-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b458a-133">-WorkspaceName</span></span>
<span data-ttu-id="b458a-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="b458a-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b458a-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b458a-135">-WorkspaceObject</span></span>
<span data-ttu-id="b458a-136">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b458a-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b458a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b458a-137">CommonParameters</span></span>
<span data-ttu-id="b458a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b458a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b458a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b458a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b458a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b458a-140">INPUTS</span></span>

### <span data-ttu-id="b458a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b458a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b458a-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="b458a-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="b458a-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b458a-143">OUTPUTS</span></span>

### <span data-ttu-id="b458a-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="b458a-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="b458a-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b458a-145">NOTES</span></span>

## <span data-ttu-id="b458a-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b458a-146">RELATED LINKS</span></span>
