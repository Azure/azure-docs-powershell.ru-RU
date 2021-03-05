---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: c0c1b83f177b568e7058b973b788a633cfefe48c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970131"
---
# <span data-ttu-id="29580-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="29580-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="29580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29580-102">SYNOPSIS</span></span>
<span data-ttu-id="29580-103">Получите состояние подписки для триггера события для указанных событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="29580-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="29580-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29580-104">SYNTAX</span></span>

### <span data-ttu-id="29580-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29580-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29580-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="29580-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29580-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="29580-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29580-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29580-108">DESCRIPTION</span></span>
<span data-ttu-id="29580-109">Cmdlet **Get-AzSynapseTriggerSubscriptionStatus** получает состояние подписки для триггера события, указанного для указанной внешней службы.</span><span class="sxs-lookup"><span data-stu-id="29580-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="29580-110">Триггер нельзя запускать, пока не будет возвращено состояние "Включено".</span><span class="sxs-lookup"><span data-stu-id="29580-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="29580-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29580-111">EXAMPLES</span></span>

### <span data-ttu-id="29580-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29580-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="29580-113">Эта команда получит состояние подписки на триггер ContosoTrigger для событий внешней службы.</span><span class="sxs-lookup"><span data-stu-id="29580-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="29580-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="29580-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="29580-115">Эта команда будет получать состояние подписки на триггер ContosoTrigger для событий внешней службы через канал.</span><span class="sxs-lookup"><span data-stu-id="29580-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="29580-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="29580-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="29580-117">Эта команда будет получать состояние подписки на триггер ContosoTrigger для событий внешней службы через канал.</span><span class="sxs-lookup"><span data-stu-id="29580-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="29580-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29580-118">PARAMETERS</span></span>

### <span data-ttu-id="29580-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29580-119">-DefaultProfile</span></span>
<span data-ttu-id="29580-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29580-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29580-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29580-121">-InputObject</span></span>
<span data-ttu-id="29580-122">Объект-триггер.</span><span class="sxs-lookup"><span data-stu-id="29580-122">The trigger object.</span></span>

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

### <span data-ttu-id="29580-123">-Name</span><span class="sxs-lookup"><span data-stu-id="29580-123">-Name</span></span>
<span data-ttu-id="29580-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="29580-124">The trigger name.</span></span>

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

### <span data-ttu-id="29580-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="29580-125">-WorkspaceName</span></span>
<span data-ttu-id="29580-126">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="29580-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="29580-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="29580-127">-WorkspaceObject</span></span>
<span data-ttu-id="29580-128">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="29580-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="29580-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29580-129">CommonParameters</span></span>
<span data-ttu-id="29580-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29580-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29580-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29580-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29580-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29580-132">INPUTS</span></span>

### <span data-ttu-id="29580-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="29580-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="29580-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="29580-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="29580-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29580-135">OUTPUTS</span></span>

### <span data-ttu-id="29580-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="29580-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="29580-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29580-137">NOTES</span></span>

## <span data-ttu-id="29580-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29580-138">RELATED LINKS</span></span>
