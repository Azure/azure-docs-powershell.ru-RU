---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235690"
---
# <span data-ttu-id="ec398-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="ec398-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="ec398-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec398-102">SYNOPSIS</span></span>
<span data-ttu-id="ec398-103">Получение сведений о триггерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ec398-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="ec398-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec398-104">SYNTAX</span></span>

### <span data-ttu-id="ec398-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec398-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec398-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="ec398-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec398-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec398-107">DESCRIPTION</span></span>
<span data-ttu-id="ec398-108">Командлет **Get-AzSynapseTrigger** получает сведения о триггерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ec398-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="ec398-109">Если вы задаете имя триггера, командлет получает сведения об этом триггере.</span><span class="sxs-lookup"><span data-stu-id="ec398-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="ec398-110">Если имя не задано, командлет получает сведения обо всех триггерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ec398-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="ec398-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec398-111">EXAMPLES</span></span>

### <span data-ttu-id="ec398-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec398-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ec398-113">Получает список всех триггеров, созданных в ContosoWorkspace рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ec398-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="ec398-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ec398-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="ec398-115">Возвращает один триггер с именем ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ec398-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="ec398-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ec398-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="ec398-117">Получает один триггер с именем ContosoTrigger в рабочей области ContosoWorkspace с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="ec398-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ec398-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec398-118">PARAMETERS</span></span>

### <span data-ttu-id="ec398-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec398-119">-DefaultProfile</span></span>
<span data-ttu-id="ec398-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec398-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec398-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec398-121">-Name</span></span>
<span data-ttu-id="ec398-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="ec398-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec398-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ec398-123">-WorkspaceName</span></span>
<span data-ttu-id="ec398-124">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ec398-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ec398-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ec398-125">-WorkspaceObject</span></span>
<span data-ttu-id="ec398-126">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ec398-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ec398-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec398-127">CommonParameters</span></span>
<span data-ttu-id="ec398-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec398-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec398-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec398-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec398-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec398-130">INPUTS</span></span>

### <span data-ttu-id="ec398-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec398-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ec398-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec398-132">OUTPUTS</span></span>

### <span data-ttu-id="ec398-133">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="ec398-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="ec398-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec398-134">NOTES</span></span>

## <span data-ttu-id="ec398-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec398-135">RELATED LINKS</span></span>
