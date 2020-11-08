---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078564"
---
# <span data-ttu-id="def80-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="def80-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="def80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="def80-102">SYNOPSIS</span></span>
<span data-ttu-id="def80-103">Получение сведений о записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="def80-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="def80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="def80-104">SYNTAX</span></span>

### <span data-ttu-id="def80-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="def80-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="def80-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="def80-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="def80-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="def80-107">DESCRIPTION</span></span>
<span data-ttu-id="def80-108">Командлет **Get-AzSynapseNotebook** получает сведения о записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="def80-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="def80-109">Если вы укажете имя записной книжки, командлет получит сведения о записной книжке.</span><span class="sxs-lookup"><span data-stu-id="def80-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="def80-110">Если имя не задано, командлет получает сведения обо всех записных книжках в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="def80-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="def80-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="def80-111">EXAMPLES</span></span>

### <span data-ttu-id="def80-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="def80-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="def80-113">Получает список всех записных книжек в ContosoWorkspace рабочей области.</span><span class="sxs-lookup"><span data-stu-id="def80-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="def80-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="def80-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="def80-115">Возвращает одну записную книжку с именем ContosoNotebook в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="def80-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="def80-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="def80-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="def80-117">Возвращает одну записную книжку с именем ContosoNotebook в рабочей области ContosoWorkspace через конвейер.</span><span class="sxs-lookup"><span data-stu-id="def80-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="def80-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="def80-118">PARAMETERS</span></span>

### <span data-ttu-id="def80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def80-119">-DefaultProfile</span></span>
<span data-ttu-id="def80-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="def80-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def80-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="def80-121">-Name</span></span>
<span data-ttu-id="def80-122">Имя записной книжки.</span><span class="sxs-lookup"><span data-stu-id="def80-122">The notebook name.</span></span>

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

### <span data-ttu-id="def80-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="def80-123">-WorkspaceName</span></span>
<span data-ttu-id="def80-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="def80-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="def80-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="def80-125">-WorkspaceObject</span></span>
<span data-ttu-id="def80-126">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="def80-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="def80-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def80-127">CommonParameters</span></span>
<span data-ttu-id="def80-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="def80-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def80-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="def80-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def80-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="def80-130">INPUTS</span></span>

### <span data-ttu-id="def80-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="def80-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="def80-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="def80-132">OUTPUTS</span></span>

### <span data-ttu-id="def80-133">Microsoft. Azure. Commands. Synapse. Models. PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="def80-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="def80-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="def80-134">NOTES</span></span>

## <span data-ttu-id="def80-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="def80-135">RELATED LINKS</span></span>
