---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: b9ad7c729395115845349c1e39f8d90666a4fcb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729182"
---
# <span data-ttu-id="589e1-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="589e1-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="589e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="589e1-102">SYNOPSIS</span></span>
<span data-ttu-id="589e1-103">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="589e1-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="589e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="589e1-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="589e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="589e1-105">DESCRIPTION</span></span>
<span data-ttu-id="589e1-106">Командлет **New-AzServiceBusQueue** создает очередь служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="589e1-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="589e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="589e1-107">EXAMPLES</span></span>

### <span data-ttu-id="589e1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="589e1-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
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
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="589e1-109">Создание новой очереди служебной шины `SB-Queue_example1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="589e1-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="589e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="589e1-110">PARAMETERS</span></span>

### <span data-ttu-id="589e1-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="589e1-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="589e1-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="589e1-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="589e1-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="589e1-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="589e1-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="589e1-115">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="589e1-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="589e1-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="589e1-117">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="589e1-117">Timespan to live value.</span></span>
<span data-ttu-id="589e1-118">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="589e1-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="589e1-119">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="589e1-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="589e1-120">Для стандартных = TimeSpan. Max и Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="589e1-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589e1-121">-DefaultProfile</span></span>
<span data-ttu-id="589e1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="589e1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="589e1-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="589e1-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="589e1-124">Указывает окно времени журнала обнаружения повторов, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="589e1-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="589e1-125">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="589e1-125">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="589e1-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="589e1-127">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="589e1-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="589e1-128">-EnableExpress</span></span>
<span data-ttu-id="589e1-129">EnableExpress — значение, показывающее, включены ли выражения для Экспресс-сущностей.</span><span class="sxs-lookup"><span data-stu-id="589e1-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="589e1-130">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="589e1-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="589e1-131">-EnablePartitioning</span></span>
<span data-ttu-id="589e1-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="589e1-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="589e1-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="589e1-134">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="589e1-134">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="589e1-135">-ForwardTo</span></span>
<span data-ttu-id="589e1-136">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="589e1-136">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="589e1-137">-LockDuration</span></span>
<span data-ttu-id="589e1-138">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="589e1-138">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="589e1-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="589e1-140">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="589e1-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="589e1-141">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="589e1-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="589e1-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="589e1-143">MaxSizeInMegabytes — максимальный размер очереди в мегабайтах, который является размером памяти, выделенной для очереди.</span><span class="sxs-lookup"><span data-stu-id="589e1-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="589e1-144">-MessageCount</span></span>
<span data-ttu-id="589e1-145">MessageCount — количество сообщений в очереди</span><span class="sxs-lookup"><span data-stu-id="589e1-145">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="589e1-146">-Name</span></span>
<span data-ttu-id="589e1-147">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="589e1-147">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-148">-Namespace</span><span class="sxs-lookup"><span data-stu-id="589e1-148">-Namespace</span></span>
<span data-ttu-id="589e1-149">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="589e1-149">Namespace Name</span></span>

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

### <span data-ttu-id="589e1-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="589e1-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="589e1-151">RequiresDuplicateDetection — значение, указывающее, поддерживает ли очередь понятие сеанса</span><span class="sxs-lookup"><span data-stu-id="589e1-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="589e1-152">-RequiresSession</span></span>
<span data-ttu-id="589e1-153">RequiresSession — значение, показывающее, требуется ли для этой очереди обнаружение повторяющихся данных</span><span class="sxs-lookup"><span data-stu-id="589e1-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="589e1-154">-ResourceGroupName</span></span>
<span data-ttu-id="589e1-155">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="589e1-155">The name of the resource group</span></span>

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

### <span data-ttu-id="589e1-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="589e1-156">-SizeInBytes</span></span>
<span data-ttu-id="589e1-157">SizeInBytes — размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="589e1-157">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="589e1-158">-Confirm</span></span>
<span data-ttu-id="589e1-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="589e1-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589e1-160">-WhatIf</span></span>
<span data-ttu-id="589e1-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="589e1-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="589e1-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="589e1-162">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589e1-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589e1-163">CommonParameters</span></span>
<span data-ttu-id="589e1-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="589e1-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589e1-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="589e1-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589e1-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="589e1-166">INPUTS</span></span>

### <span data-ttu-id="589e1-167">System. String</span><span class="sxs-lookup"><span data-stu-id="589e1-167">System.String</span></span>

### <span data-ttu-id="589e1-168">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="589e1-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="589e1-169">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="589e1-169">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="589e1-170">System. Nullable "1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="589e1-170">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="589e1-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="589e1-171">OUTPUTS</span></span>

### <span data-ttu-id="589e1-172">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="589e1-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="589e1-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="589e1-173">NOTES</span></span>

## <span data-ttu-id="589e1-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="589e1-174">RELATED LINKS</span></span>
