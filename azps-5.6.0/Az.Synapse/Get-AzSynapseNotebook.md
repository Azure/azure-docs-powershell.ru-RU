---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: df22eb6fa435c3cf8bca4b339e460b3415991964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967203"
---
# <span data-ttu-id="cb91d-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="cb91d-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="cb91d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb91d-102">SYNOPSIS</span></span>
<span data-ttu-id="cb91d-103">Получает сведения о записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb91d-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="cb91d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb91d-104">SYNTAX</span></span>

### <span data-ttu-id="cb91d-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb91d-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb91d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="cb91d-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb91d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb91d-107">DESCRIPTION</span></span>
<span data-ttu-id="cb91d-108">Чтобы получить сведения о записных книжках в рабочей области, можно использовать **cmdletNotebook Get-AzSynapseNotebook.**</span><span class="sxs-lookup"><span data-stu-id="cb91d-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="cb91d-109">Если указать имя записной книжки, он получит сведения о записной книжке.</span><span class="sxs-lookup"><span data-stu-id="cb91d-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="cb91d-110">Если имя не указано, он получает сведения обо всех записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cb91d-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="cb91d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb91d-111">EXAMPLES</span></span>

### <span data-ttu-id="cb91d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb91d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="cb91d-113">Возвращает список всех записных книг в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb91d-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cb91d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cb91d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="cb91d-115">Получает одну записную книжку с названием ContosoNotebook в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cb91d-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="cb91d-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cb91d-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="cb91d-117">Получает одну записную книжку с названием ContosoNotebook в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="cb91d-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cb91d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb91d-118">PARAMETERS</span></span>

### <span data-ttu-id="cb91d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb91d-119">-DefaultProfile</span></span>
<span data-ttu-id="cb91d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb91d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb91d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cb91d-121">-Name</span></span>
<span data-ttu-id="cb91d-122">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="cb91d-122">The notebook name.</span></span>

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

### <span data-ttu-id="cb91d-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cb91d-123">-WorkspaceName</span></span>
<span data-ttu-id="cb91d-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cb91d-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb91d-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cb91d-125">-WorkspaceObject</span></span>
<span data-ttu-id="cb91d-126">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cb91d-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb91d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb91d-127">CommonParameters</span></span>
<span data-ttu-id="cb91d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb91d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb91d-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb91d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb91d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb91d-130">INPUTS</span></span>

### <span data-ttu-id="cb91d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cb91d-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cb91d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb91d-132">OUTPUTS</span></span>

### <span data-ttu-id="cb91d-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="cb91d-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="cb91d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb91d-134">NOTES</span></span>

## <span data-ttu-id="cb91d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb91d-135">RELATED LINKS</span></span>
