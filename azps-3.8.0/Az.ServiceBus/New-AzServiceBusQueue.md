---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: a555e269fd02cb02d420426fed99888b19214f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065782"
---
# <span data-ttu-id="39a4f-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="39a4f-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="39a4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="39a4f-103">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="39a4f-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="39a4f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39a4f-104">SYNTAX</span></span>

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

## <span data-ttu-id="39a4f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="39a4f-106">Командлет **New-AzServiceBusQueue** создает очередь служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="39a4f-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="39a4f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39a4f-107">EXAMPLES</span></span>

### <span data-ttu-id="39a4f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39a4f-108">Example 1</span></span>
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

<span data-ttu-id="39a4f-109">Создание новой очереди служебной шины `SB-Queue_example1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="39a4f-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="39a4f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39a4f-110">PARAMETERS</span></span>

### <span data-ttu-id="39a4f-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="39a4f-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="39a4f-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="39a4f-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="39a4f-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="39a4f-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="39a4f-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="39a4f-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="39a4f-115">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="39a4f-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="39a4f-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="39a4f-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="39a4f-117">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="39a4f-117">Timespan to live value.</span></span>
<span data-ttu-id="39a4f-118">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="39a4f-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="39a4f-119">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="39a4f-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="39a4f-120">Для стандартных = TimeSpan. Max и Basic = 14 дней</span><span class="sxs-lookup"><span data-stu-id="39a4f-120">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="39a4f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a4f-121">-DefaultProfile</span></span>
<span data-ttu-id="39a4f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39a4f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a4f-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="39a4f-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="39a4f-124">Указывает временное окно журнала обнаружения повторений, значение [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , определяющее продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="39a4f-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="39a4f-125">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="39a4f-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="39a4f-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="39a4f-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="39a4f-127">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="39a4f-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="39a4f-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="39a4f-128">-EnableExpress</span></span>
<span data-ttu-id="39a4f-129">EnableExpress — значение, показывающее, включены ли выражения для Экспресс-сущностей.</span><span class="sxs-lookup"><span data-stu-id="39a4f-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="39a4f-130">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="39a4f-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="39a4f-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="39a4f-131">-EnablePartitioning</span></span>
<span data-ttu-id="39a4f-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="39a4f-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="39a4f-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="39a4f-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="39a4f-134">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="39a4f-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="39a4f-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="39a4f-135">-ForwardTo</span></span>
<span data-ttu-id="39a4f-136">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="39a4f-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="39a4f-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="39a4f-137">-LockDuration</span></span>
<span data-ttu-id="39a4f-138">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="39a4f-138">Lock Duration</span></span>

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

### <span data-ttu-id="39a4f-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="39a4f-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="39a4f-140">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="39a4f-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="39a4f-141">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="39a4f-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="39a4f-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="39a4f-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="39a4f-143">MaxSizeInMegabytes — максимальный размер очереди в мегабайтах, который является размером памяти, выделенной для очереди. Значение по умолчанию — 1024.</span><span class="sxs-lookup"><span data-stu-id="39a4f-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="39a4f-144">Макс. для стандартной SKU — 5120, а для Premium SKU — 81920, разрешенные значения: 1024, 2048, 3072, 4096, 5120, 10240, 20480,, 40960</span><span class="sxs-lookup"><span data-stu-id="39a4f-144">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="39a4f-145">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="39a4f-145">-MessageCount</span></span>
<span data-ttu-id="39a4f-146">MessageCount — количество сообщений в очереди</span><span class="sxs-lookup"><span data-stu-id="39a4f-146">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="39a4f-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39a4f-147">-Name</span></span>
<span data-ttu-id="39a4f-148">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="39a4f-148">Queue Name</span></span>

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

### <span data-ttu-id="39a4f-149">-Namespace</span><span class="sxs-lookup"><span data-stu-id="39a4f-149">-Namespace</span></span>
<span data-ttu-id="39a4f-150">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="39a4f-150">Namespace Name</span></span>

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

### <span data-ttu-id="39a4f-151">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="39a4f-151">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="39a4f-152">RequiresDuplicateDetection — значение, указывающее, поддерживает ли очередь понятие сеанса</span><span class="sxs-lookup"><span data-stu-id="39a4f-152">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="39a4f-153">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="39a4f-153">-RequiresSession</span></span>
<span data-ttu-id="39a4f-154">RequiresSession — значение, показывающее, использует ли очередь сеансы</span><span class="sxs-lookup"><span data-stu-id="39a4f-154">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="39a4f-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a4f-155">-ResourceGroupName</span></span>
<span data-ttu-id="39a4f-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39a4f-156">The name of the resource group</span></span>

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

### <span data-ttu-id="39a4f-157">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="39a4f-157">-SizeInBytes</span></span>
<span data-ttu-id="39a4f-158">SizeInBytes — размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="39a4f-158">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="39a4f-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39a4f-159">-Confirm</span></span>
<span data-ttu-id="39a4f-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39a4f-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a4f-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a4f-161">-WhatIf</span></span>
<span data-ttu-id="39a4f-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39a4f-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a4f-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39a4f-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a4f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a4f-164">CommonParameters</span></span>
<span data-ttu-id="39a4f-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39a4f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a4f-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a4f-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a4f-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39a4f-167">INPUTS</span></span>

### <span data-ttu-id="39a4f-168">System. String</span><span class="sxs-lookup"><span data-stu-id="39a4f-168">System.String</span></span>

### <span data-ttu-id="39a4f-169">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39a4f-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="39a4f-170">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39a4f-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="39a4f-171">System. Nullable "1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39a4f-171">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="39a4f-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39a4f-172">OUTPUTS</span></span>

### <span data-ttu-id="39a4f-173">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="39a4f-173">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="39a4f-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="39a4f-174">NOTES</span></span>

## <span data-ttu-id="39a4f-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39a4f-175">RELATED LINKS</span></span>
