---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 988d2f53ebf0bf69806bf06fedb5e2db31c9d0c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973064"
---
# <span data-ttu-id="83899-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="83899-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="83899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83899-102">SYNOPSIS</span></span>
<span data-ttu-id="83899-103">Получает сведения о триггерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="83899-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="83899-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83899-104">SYNTAX</span></span>

### <span data-ttu-id="83899-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83899-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83899-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="83899-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83899-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83899-107">DESCRIPTION</span></span>
<span data-ttu-id="83899-108">Для получения сведений о триггерах в рабочей области возвращается **cmdlet Get-AzSynapseTrigger.**</span><span class="sxs-lookup"><span data-stu-id="83899-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="83899-109">Если указать имя триггера, он получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="83899-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="83899-110">Если имя не указано, он получает сведения обо всех триггерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="83899-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="83899-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83899-111">EXAMPLES</span></span>

### <span data-ttu-id="83899-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83899-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="83899-113">Возвращает список всех триггеров, созданных в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="83899-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="83899-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="83899-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="83899-115">Получает один триггер ContosoTrigger в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="83899-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="83899-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="83899-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="83899-117">Получает один триггер ContosoTrigger в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="83899-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="83899-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83899-118">PARAMETERS</span></span>

### <span data-ttu-id="83899-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83899-119">-DefaultProfile</span></span>
<span data-ttu-id="83899-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83899-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83899-121">-Name</span><span class="sxs-lookup"><span data-stu-id="83899-121">-Name</span></span>
<span data-ttu-id="83899-122">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="83899-122">The trigger name.</span></span>

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

### <span data-ttu-id="83899-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="83899-123">-WorkspaceName</span></span>
<span data-ttu-id="83899-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="83899-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="83899-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="83899-125">-WorkspaceObject</span></span>
<span data-ttu-id="83899-126">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="83899-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="83899-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83899-127">CommonParameters</span></span>
<span data-ttu-id="83899-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83899-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83899-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83899-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83899-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83899-130">INPUTS</span></span>

### <span data-ttu-id="83899-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="83899-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="83899-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83899-132">OUTPUTS</span></span>

### <span data-ttu-id="83899-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="83899-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="83899-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83899-134">NOTES</span></span>

## <span data-ttu-id="83899-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83899-135">RELATED LINKS</span></span>
