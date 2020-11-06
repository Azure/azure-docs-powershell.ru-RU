---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 29e2c0f04dff07e76907ee67c3e012c2b67c1582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566402"
---
# <span data-ttu-id="4e879-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4e879-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="4e879-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e879-102">SYNOPSIS</span></span>
<span data-ttu-id="4e879-103">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4e879-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e879-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e879-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e879-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e879-105">DESCRIPTION</span></span>
<span data-ttu-id="4e879-106">Командлет **New-AzureRmServiceBusQueue** создает очередь служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4e879-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4e879-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e879-107">EXAMPLES</span></span>

### <span data-ttu-id="4e879-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e879-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

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

<span data-ttu-id="4e879-109">Создание новой очереди служебной шины `SB-Queue_example1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="4e879-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="4e879-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e879-110">PARAMETERS</span></span>

### <span data-ttu-id="4e879-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="4e879-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="4e879-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="4e879-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="4e879-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="4e879-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="4e879-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="4e879-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="4e879-115">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="4e879-115">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="4e879-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="4e879-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="4e879-117">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="4e879-117">Timespan to live value.</span></span>
<span data-ttu-id="4e879-118">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="4e879-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="4e879-119">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e879-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="4e879-120">Для стандартных = TimeSpan. Max и Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="4e879-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="4e879-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e879-121">-DefaultProfile</span></span>
<span data-ttu-id="4e879-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e879-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e879-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="4e879-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="4e879-124">Указывает окно времени журнала обнаружения повторов, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="4e879-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="4e879-125">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="4e879-125">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="4e879-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="4e879-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="4e879-127">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="4e879-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="4e879-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="4e879-128">-EnableExpress</span></span>
<span data-ttu-id="4e879-129">EnableExpress — значение, показывающее, включены ли выражения для Экспресс-сущностей.</span><span class="sxs-lookup"><span data-stu-id="4e879-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="4e879-130">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="4e879-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="4e879-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="4e879-131">-EnablePartitioning</span></span>
<span data-ttu-id="4e879-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="4e879-132">EnablePartitioning</span></span>

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

### <span data-ttu-id="4e879-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="4e879-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="4e879-134">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="4e879-134">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="4e879-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="4e879-135">-ForwardTo</span></span>
<span data-ttu-id="4e879-136">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="4e879-136">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="4e879-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="4e879-137">-LockDuration</span></span>
<span data-ttu-id="4e879-138">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="4e879-138">Lock Duration</span></span>

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

### <span data-ttu-id="4e879-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="4e879-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="4e879-140">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="4e879-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="4e879-141">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="4e879-141">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="4e879-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="4e879-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="4e879-143">MaxSizeInMegabytes — максимальный размер очереди в мегабайтах, который является размером памяти, выделенной для очереди.</span><span class="sxs-lookup"><span data-stu-id="4e879-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="4e879-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="4e879-144">-MessageCount</span></span>
<span data-ttu-id="4e879-145">MessageCount — количество сообщений в очереди</span><span class="sxs-lookup"><span data-stu-id="4e879-145">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="4e879-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e879-146">-Name</span></span>
<span data-ttu-id="4e879-147">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="4e879-147">Queue Name</span></span>

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

### <span data-ttu-id="4e879-148">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4e879-148">-Namespace</span></span>
<span data-ttu-id="4e879-149">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="4e879-149">Namespace Name</span></span>

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

### <span data-ttu-id="4e879-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="4e879-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="4e879-151">RequiresDuplicateDetection — значение, указывающее, поддерживает ли очередь понятие сеанса</span><span class="sxs-lookup"><span data-stu-id="4e879-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="4e879-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="4e879-152">-RequiresSession</span></span>
<span data-ttu-id="4e879-153">RequiresSession — значение, показывающее, требуется ли для этой очереди обнаружение повторяющихся данных</span><span class="sxs-lookup"><span data-stu-id="4e879-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

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

### <span data-ttu-id="4e879-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e879-154">-ResourceGroupName</span></span>
<span data-ttu-id="4e879-155">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e879-155">The name of the resource group</span></span>

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

### <span data-ttu-id="4e879-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="4e879-156">-SizeInBytes</span></span>
<span data-ttu-id="4e879-157">SizeInBytes — размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="4e879-157">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="4e879-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e879-158">-Confirm</span></span>
<span data-ttu-id="4e879-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e879-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e879-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e879-160">-WhatIf</span></span>
<span data-ttu-id="4e879-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e879-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e879-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e879-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e879-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e879-163">CommonParameters</span></span>
<span data-ttu-id="4e879-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e879-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e879-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e879-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e879-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e879-166">INPUTS</span></span>

### <span data-ttu-id="4e879-167">System. String</span><span class="sxs-lookup"><span data-stu-id="4e879-167">System.String</span></span>

### <span data-ttu-id="4e879-168">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4e879-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4e879-169">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4e879-169">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4e879-170">System. Nullable "1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4e879-170">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4e879-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e879-171">OUTPUTS</span></span>

### <span data-ttu-id="4e879-172">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="4e879-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="4e879-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e879-173">NOTES</span></span>

## <span data-ttu-id="4e879-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e879-174">RELATED LINKS</span></span>
