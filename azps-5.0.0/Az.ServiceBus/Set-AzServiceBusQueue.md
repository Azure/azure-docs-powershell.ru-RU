---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318815"
---
# <span data-ttu-id="fd7e6-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fd7e6-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="fd7e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e6-103">Обновляет описание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fd7e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd7e6-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd7e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7e6-106">Командлет **Set-AzServiceBusQueue** обновляет описание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fd7e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd7e6-107">EXAMPLES</span></span>

### <span data-ttu-id="fd7e6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd7e6-108">Example 1</span></span>
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

<span data-ttu-id="fd7e6-109">Обновляет указанную очередь с помощью нового описания в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="fd7e6-110">В этом примере свойство **DeadLetteringOnMessageExpiration** обновляется на **true** и **SupportOrdering** в **true**.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="fd7e6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd7e6-111">PARAMETERS</span></span>

### <span data-ttu-id="fd7e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e6-112">-DefaultProfile</span></span>
<span data-ttu-id="fd7e6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7e6-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7e6-114">-InputObject</span></span>
<span data-ttu-id="fd7e6-115">Определение ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="fd7e6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd7e6-116">-Name</span></span>
<span data-ttu-id="fd7e6-117">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-117">Queue Name.</span></span>

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

### <span data-ttu-id="fd7e6-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd7e6-118">-Namespace</span></span>
<span data-ttu-id="fd7e6-119">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-119">Namespace Name.</span></span>

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

### <span data-ttu-id="fd7e6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e6-120">-ResourceGroupName</span></span>
<span data-ttu-id="fd7e6-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-121">The name of the resource group</span></span>

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

### <span data-ttu-id="fd7e6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd7e6-122">-Confirm</span></span>
<span data-ttu-id="fd7e6-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7e6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7e6-124">-WhatIf</span></span>
<span data-ttu-id="fd7e6-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd7e6-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e6-127">CommonParameters</span></span>
<span data-ttu-id="fd7e6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd7e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e6-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7e6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd7e6-130">INPUTS</span></span>

### <span data-ttu-id="fd7e6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7e6-131">System.String</span></span>

### <span data-ttu-id="fd7e6-132">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fd7e6-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fd7e6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd7e6-133">OUTPUTS</span></span>

### <span data-ttu-id="fd7e6-134">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fd7e6-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fd7e6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd7e6-135">NOTES</span></span>

## <span data-ttu-id="fd7e6-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd7e6-136">RELATED LINKS</span></span>
