---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224676"
---
# <span data-ttu-id="8559d-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8559d-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="8559d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8559d-102">SYNOPSIS</span></span>
<span data-ttu-id="8559d-103">Получите состояние подписки для триггера события для указанных событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="8559d-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="8559d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8559d-104">SYNTAX</span></span>

### <span data-ttu-id="8559d-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8559d-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8559d-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="8559d-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8559d-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8559d-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8559d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8559d-108">DESCRIPTION</span></span>
<span data-ttu-id="8559d-109">Cmdlet **Get-AzSynapseTriggerSubscriptionStatus** получает состояние подписки для триггера события, указанного для указанной внешней службы.</span><span class="sxs-lookup"><span data-stu-id="8559d-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="8559d-110">Триггер нельзя запускать, пока не будет возвращено состояние "Включено".</span><span class="sxs-lookup"><span data-stu-id="8559d-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="8559d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8559d-111">EXAMPLES</span></span>

### <span data-ttu-id="8559d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8559d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="8559d-113">Эта команда получит состояние подписки на триггер ContosoTrigger для событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="8559d-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="8559d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8559d-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="8559d-115">Эта команда будет получать состояние подписки на триггер ContosoTrigger для событий внешней службы через канал.</span><span class="sxs-lookup"><span data-stu-id="8559d-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="8559d-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8559d-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="8559d-117">Эта команда будет получать состояние подписки на триггер ContosoTrigger для событий внешней службы через канал.</span><span class="sxs-lookup"><span data-stu-id="8559d-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="8559d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8559d-118">PARAMETERS</span></span>

### <span data-ttu-id="8559d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8559d-119">-DefaultProfile</span></span>
<span data-ttu-id="8559d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8559d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8559d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8559d-121">-InputObject</span></span>
<span data-ttu-id="8559d-122">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="8559d-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8559d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8559d-123">-Name</span></span>
<span data-ttu-id="8559d-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="8559d-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8559d-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8559d-125">-WorkspaceName</span></span>
<span data-ttu-id="8559d-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8559d-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8559d-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8559d-127">-WorkspaceObject</span></span>
<span data-ttu-id="8559d-128">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8559d-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8559d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8559d-129">CommonParameters</span></span>
<span data-ttu-id="8559d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8559d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8559d-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8559d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8559d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8559d-132">INPUTS</span></span>

### <span data-ttu-id="8559d-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8559d-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8559d-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="8559d-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="8559d-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8559d-135">OUTPUTS</span></span>

### <span data-ttu-id="8559d-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8559d-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="8559d-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8559d-137">NOTES</span></span>

## <span data-ttu-id="8559d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8559d-138">RELATED LINKS</span></span>
