---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517346"
---
# <span data-ttu-id="404ce-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="404ce-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="404ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="404ce-102">SYNOPSIS</span></span>
<span data-ttu-id="404ce-103">Обновляет описание очереди "Автобусы обслуживания" в указанном пространстве имен "Автобус обслуживания".</span><span class="sxs-lookup"><span data-stu-id="404ce-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="404ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="404ce-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="404ce-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="404ce-105">DESCRIPTION</span></span>
<span data-ttu-id="404ce-106">**Cmdlet Set-AzServiceBusQueue** обновляет описание очереди "Автобус обслуживания" в указанном пространстве имен «Автобус обслуживания».</span><span class="sxs-lookup"><span data-stu-id="404ce-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="404ce-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="404ce-107">EXAMPLES</span></span>

### <span data-ttu-id="404ce-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="404ce-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="404ce-109">Обновляет указанную очередь с новым описанием в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="404ce-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="404ce-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется с **true,** а **SupportOrdering** — **с true.**</span><span class="sxs-lookup"><span data-stu-id="404ce-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="404ce-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="404ce-111">PARAMETERS</span></span>

### <span data-ttu-id="404ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="404ce-112">-DefaultProfile</span></span>
<span data-ttu-id="404ce-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="404ce-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="404ce-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="404ce-114">-InputObject</span></span>
<span data-ttu-id="404ce-115">Определение ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="404ce-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ce-116">-Name</span><span class="sxs-lookup"><span data-stu-id="404ce-116">-Name</span></span>
<span data-ttu-id="404ce-117">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="404ce-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ce-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="404ce-118">-Namespace</span></span>
<span data-ttu-id="404ce-119">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="404ce-119">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="404ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="404ce-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="404ce-121">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="404ce-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="404ce-122">-Confirm</span></span>
<span data-ttu-id="404ce-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="404ce-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ce-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="404ce-124">-WhatIf</span></span>
<span data-ttu-id="404ce-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="404ce-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="404ce-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="404ce-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="404ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="404ce-127">CommonParameters</span></span>
<span data-ttu-id="404ce-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="404ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="404ce-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="404ce-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="404ce-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="404ce-130">INPUTS</span></span>

### <span data-ttu-id="404ce-131">System.String</span><span class="sxs-lookup"><span data-stu-id="404ce-131">System.String</span></span>

### <span data-ttu-id="404ce-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="404ce-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="404ce-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="404ce-133">OUTPUTS</span></span>

### <span data-ttu-id="404ce-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="404ce-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="404ce-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="404ce-135">NOTES</span></span>

## <span data-ttu-id="404ce-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="404ce-136">RELATED LINKS</span></span>
