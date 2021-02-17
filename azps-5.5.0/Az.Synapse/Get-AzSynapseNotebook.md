---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241749"
---
# <span data-ttu-id="d5ed0-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="d5ed0-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="d5ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ed0-103">Получает сведения о записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="d5ed0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5ed0-104">SYNTAX</span></span>

### <span data-ttu-id="d5ed0-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5ed0-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5ed0-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d5ed0-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5ed0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5ed0-107">DESCRIPTION</span></span>
<span data-ttu-id="d5ed0-108">Чтобы получить сведения о записных книжках в рабочей области, можно использовать **cmdletNotebook Get-AzSynapseNotebook.**</span><span class="sxs-lookup"><span data-stu-id="d5ed0-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="d5ed0-109">Если указать имя записной книжки, он получит сведения о записной книжке.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="d5ed0-110">Если имя не указано, он получает сведения обо всех записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="d5ed0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5ed0-111">EXAMPLES</span></span>

### <span data-ttu-id="d5ed0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5ed0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="d5ed0-113">Возвращает список всех записных книг в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d5ed0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d5ed0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="d5ed0-115">Получает одну записную книжку с названием ContosoNotebook в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d5ed0-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d5ed0-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="d5ed0-117">Получает одну записную книжку с названием ContosoNotebook в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d5ed0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-118">PARAMETERS</span></span>

### <span data-ttu-id="d5ed0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ed0-119">-DefaultProfile</span></span>
<span data-ttu-id="d5ed0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ed0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d5ed0-121">-Name</span></span>
<span data-ttu-id="d5ed0-122">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-122">The notebook name.</span></span>

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

### <span data-ttu-id="d5ed0-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5ed0-123">-WorkspaceName</span></span>
<span data-ttu-id="d5ed0-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d5ed0-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5ed0-125">-WorkspaceObject</span></span>
<span data-ttu-id="d5ed0-126">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d5ed0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ed0-127">CommonParameters</span></span>
<span data-ttu-id="d5ed0-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ed0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ed0-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5ed0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ed0-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-130">INPUTS</span></span>

### <span data-ttu-id="d5ed0-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5ed0-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d5ed0-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5ed0-132">OUTPUTS</span></span>

### <span data-ttu-id="d5ed0-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="d5ed0-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="d5ed0-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5ed0-134">NOTES</span></span>

## <span data-ttu-id="d5ed0-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5ed0-135">RELATED LINKS</span></span>
