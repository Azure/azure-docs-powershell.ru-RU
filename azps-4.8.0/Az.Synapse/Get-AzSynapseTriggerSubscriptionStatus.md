---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077477"
---
# <span data-ttu-id="b6ed9-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="b6ed9-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="b6ed9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ed9-103">Получение состояния подписки для триггера событий для указанных внешних событий службы.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="b6ed9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6ed9-104">SYNTAX</span></span>

### <span data-ttu-id="b6ed9-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6ed9-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ed9-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="b6ed9-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6ed9-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6ed9-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6ed9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6ed9-108">DESCRIPTION</span></span>
<span data-ttu-id="b6ed9-109">Командлет **Get-AzSynapseTriggerSubscriptionStatus** получает состояние подписки для триггера событий на указанные внешние события службы.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="b6ed9-110">Триггер не может быть запущен, пока не будет возвращено состояние "включено".</span><span class="sxs-lookup"><span data-stu-id="b6ed9-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="b6ed9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6ed9-111">EXAMPLES</span></span>

### <span data-ttu-id="b6ed9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6ed9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="b6ed9-113">Эта команда получит состояние subscribtion для триггера, именуемого ContosoTrigger, с внешними событиями службы.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="b6ed9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b6ed9-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="b6ed9-115">Эта команда получит состояние subscribtion для триггера, именуемого ContosoTrigger, к внешним событиям службы через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="b6ed9-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b6ed9-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="b6ed9-117">Эта команда получит состояние subscribtion для триггера, именуемого ContosoTrigger, к внешним событиям службы через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="b6ed9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6ed9-118">PARAMETERS</span></span>

### <span data-ttu-id="b6ed9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ed9-119">-DefaultProfile</span></span>
<span data-ttu-id="b6ed9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6ed9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6ed9-121">-InputObject</span></span>
<span data-ttu-id="b6ed9-122">Объект триггера.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-122">The trigger object.</span></span>

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

### <span data-ttu-id="b6ed9-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6ed9-123">-Name</span></span>
<span data-ttu-id="b6ed9-124">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-124">The trigger name.</span></span>

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

### <span data-ttu-id="b6ed9-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6ed9-125">-WorkspaceName</span></span>
<span data-ttu-id="b6ed9-126">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b6ed9-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b6ed9-127">-WorkspaceObject</span></span>
<span data-ttu-id="b6ed9-128">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b6ed9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ed9-129">CommonParameters</span></span>
<span data-ttu-id="b6ed9-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6ed9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ed9-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6ed9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ed9-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6ed9-132">INPUTS</span></span>

### <span data-ttu-id="b6ed9-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6ed9-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b6ed9-134">Microsoft. Azure. Commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="b6ed9-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="b6ed9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6ed9-135">OUTPUTS</span></span>

### <span data-ttu-id="b6ed9-136">Microsoft. Azure. Commands. Synapse. Models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b6ed9-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="b6ed9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6ed9-137">NOTES</span></span>

## <span data-ttu-id="b6ed9-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6ed9-138">RELATED LINKS</span></span>
