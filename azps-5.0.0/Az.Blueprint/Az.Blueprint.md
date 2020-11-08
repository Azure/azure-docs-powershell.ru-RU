---
Module Name: Az.Blueprint
Module Guid: ef36c942-4a71-4e19-9450-05a35843deb6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.blueprint
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
ms.openlocfilehash: 1722032406a81253ebf580f79172be85aa23c55f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246917"
---
# <span data-ttu-id="a35b8-101">AZ. Проектный модуль</span><span class="sxs-lookup"><span data-stu-id="a35b8-101">Az.Blueprint Module</span></span>
## <span data-ttu-id="a35b8-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="a35b8-102">Description</span></span>
<span data-ttu-id="a35b8-103">В этом разделе приведены командлеты Azure PowerShell для чертежей Azure в инфраструктуре Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a35b8-103">The topics in this section document the Azure PowerShell cmdlets for Azure Blueprints in the Azure Resource Manager framework.</span></span> <span data-ttu-id="a35b8-104">Командлеты существуют в пространстве имен Microsoft. Azure. PowerShell. командлеты.</span><span class="sxs-lookup"><span data-stu-id="a35b8-104">The cmdlets exist in the Microsoft.Azure.PowerShell.Cmdlets.Blueprint namespace.</span></span>

## <span data-ttu-id="a35b8-105">Командлеты AZ. для чертежей</span><span class="sxs-lookup"><span data-stu-id="a35b8-105">Az.Blueprint Cmdlets</span></span>
### [<span data-ttu-id="a35b8-106">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a35b8-106">Export-AzBlueprintWithArtifact</span></span>](Export-AzBlueprintWithArtifact.md)
<span data-ttu-id="a35b8-107">Экспортировать определение указанного чертежа в указанное расположение выходных файлов в виде JSON-файла.</span><span class="sxs-lookup"><span data-stu-id="a35b8-107">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

### [<span data-ttu-id="a35b8-108">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a35b8-108">Get-AzBlueprint</span></span>](Get-AzBlueprint.md)
<span data-ttu-id="a35b8-109">Получение одного или нескольких определений чертежей.</span><span class="sxs-lookup"><span data-stu-id="a35b8-109">Get one or more blueprint definitions.</span></span>

### [<span data-ttu-id="a35b8-110">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a35b8-110">Get-AzBlueprintArtifact</span></span>](Get-AzBlueprintArtifact.md)
<span data-ttu-id="a35b8-111">Получение артефактов из определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="a35b8-111">Retrieve artifacts from a blueprint definition.</span></span>

### [<span data-ttu-id="a35b8-112">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a35b8-112">Get-AzBlueprintAssignment</span></span>](Get-AzBlueprintAssignment.md)
<span data-ttu-id="a35b8-113">Получение одного или нескольких назначений для чертежей.</span><span class="sxs-lookup"><span data-stu-id="a35b8-113">Get one or more blueprint assignments.</span></span>

### [<span data-ttu-id="a35b8-114">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a35b8-114">Import-AzBlueprintWithArtifact</span></span>](Import-AzBlueprintWithArtifact.md)
<span data-ttu-id="a35b8-115">Импортируйте файл в формате JSON в объект чертежа и сохраните его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="a35b8-115">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="a35b8-116">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a35b8-116">New-AzBlueprint</span></span>](New-AzBlueprint.md)
<span data-ttu-id="a35b8-117">Создание нового определения чертежа и сохранение его в указанной подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="a35b8-117">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="a35b8-118">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a35b8-118">New-AzBlueprintArtifact</span></span>](New-AzBlueprintArtifact.md)
<span data-ttu-id="a35b8-119">Создайте новый артефакт и сохраните его в определении чертежа.</span><span class="sxs-lookup"><span data-stu-id="a35b8-119">Create a new artifact and save it within a blueprint definition.</span></span>

### [<span data-ttu-id="a35b8-120">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a35b8-120">New-AzBlueprintAssignment</span></span>](New-AzBlueprintAssignment.md)
<span data-ttu-id="a35b8-121">Назначение определения плана подписке или группе управления.</span><span class="sxs-lookup"><span data-stu-id="a35b8-121">Assign a blueprint definition to a subscription or a management group.</span></span>

### [<span data-ttu-id="a35b8-122">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a35b8-122">Publish-AzBlueprint</span></span>](Publish-AzBlueprint.md)
<span data-ttu-id="a35b8-123">Опубликуйте новую версию чертежа.</span><span class="sxs-lookup"><span data-stu-id="a35b8-123">Publish a new version of a blueprint.</span></span>

### [<span data-ttu-id="a35b8-124">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a35b8-124">Remove-AzBlueprintAssignment</span></span>](Remove-AzBlueprintAssignment.md)
<span data-ttu-id="a35b8-125">Удаление назначения из подписки или группы управления.</span><span class="sxs-lookup"><span data-stu-id="a35b8-125">Remove a blueprint assignment from a subscription or a management group.</span></span>

### [<span data-ttu-id="a35b8-126">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a35b8-126">Set-AzBlueprint</span></span>](Set-AzBlueprint.md)
<span data-ttu-id="a35b8-127">Обновите определение чертежа.</span><span class="sxs-lookup"><span data-stu-id="a35b8-127">Update a blueprint definition.</span></span>

### [<span data-ttu-id="a35b8-128">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a35b8-128">Set-AzBlueprintArtifact</span></span>](Set-AzBlueprintArtifact.md)
<span data-ttu-id="a35b8-129">Обновление артефакта в определении чертежа.</span><span class="sxs-lookup"><span data-stu-id="a35b8-129">Update an artifact in a blueprint definition.</span></span>

### [<span data-ttu-id="a35b8-130">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a35b8-130">Set-AzBlueprintAssignment</span></span>](Set-AzBlueprintAssignment.md)
<span data-ttu-id="a35b8-131">Обновление существующего задания в виде чертежей.</span><span class="sxs-lookup"><span data-stu-id="a35b8-131">Update an existing blueprint assignment.</span></span>

