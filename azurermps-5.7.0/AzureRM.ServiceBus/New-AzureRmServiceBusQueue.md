---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733218"
---
# <span data-ttu-id="43ed5-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="43ed5-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="43ed5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="43ed5-103">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="43ed5-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43ed5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43ed5-104">SYNTAX</span></span>

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

## <span data-ttu-id="43ed5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="43ed5-106">Командлет **New-AzureRmServiceBusQueue** создает очередь служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="43ed5-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="43ed5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="43ed5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43ed5-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="43ed5-109">Создание новой очереди служебной шины `SB-Queue_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="43ed5-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="43ed5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43ed5-110">PARAMETERS</span></span>

### <span data-ttu-id="43ed5-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="43ed5-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="43ed5-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="43ed5-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="43ed5-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="43ed5-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43ed5-114">-Confirm</span></span>
<span data-ttu-id="43ed5-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43ed5-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="43ed5-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="43ed5-117">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="43ed5-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="43ed5-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="43ed5-119">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="43ed5-119">Timespan to live value.</span></span>
<span data-ttu-id="43ed5-120">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="43ed5-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="43ed5-121">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="43ed5-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="43ed5-122">Для стандартных = TimeSpan. Max и Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="43ed5-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ed5-123">-DefaultProfile</span></span>
<span data-ttu-id="43ed5-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43ed5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="43ed5-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="43ed5-126">Указывает окно времени журнала обнаружения повторов, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="43ed5-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="43ed5-127">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="43ed5-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="43ed5-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="43ed5-129">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="43ed5-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="43ed5-130">-EnableExpress</span></span>
<span data-ttu-id="43ed5-131">EnableExpress — значение, показывающее, включены ли выражения для Экспресс-сущностей.</span><span class="sxs-lookup"><span data-stu-id="43ed5-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="43ed5-132">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="43ed5-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="43ed5-133">-EnablePartitioning</span></span>
<span data-ttu-id="43ed5-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="43ed5-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="43ed5-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="43ed5-136">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="43ed5-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="43ed5-137">-ForwardTo</span></span>
<span data-ttu-id="43ed5-138">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="43ed5-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="43ed5-139">-LockDuration</span></span>
<span data-ttu-id="43ed5-140">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="43ed5-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="43ed5-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="43ed5-142">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="43ed5-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="43ed5-143">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="43ed5-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="43ed5-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="43ed5-145">MaxSizeInMegabytes — максимальный размер очереди в мегабайтах, который является размером памяти, выделенной для очереди.</span><span class="sxs-lookup"><span data-stu-id="43ed5-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="43ed5-146">-MessageCount</span></span>
<span data-ttu-id="43ed5-147">MessageCount — количество сообщений в очереди</span><span class="sxs-lookup"><span data-stu-id="43ed5-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43ed5-148">-Name</span></span>
<span data-ttu-id="43ed5-149">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="43ed5-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="43ed5-150">-Namespace</span></span>
<span data-ttu-id="43ed5-151">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="43ed5-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="43ed5-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="43ed5-153">RequiresDuplicateDetection — значение, указывающее, поддерживает ли очередь понятие сеанса</span><span class="sxs-lookup"><span data-stu-id="43ed5-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="43ed5-154">-RequiresSession</span></span>
<span data-ttu-id="43ed5-155">RequiresSession — значение, показывающее, требуется ли для этой очереди обнаружение повторяющихся данных</span><span class="sxs-lookup"><span data-stu-id="43ed5-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43ed5-156">-ResourceGroupName</span></span>
<span data-ttu-id="43ed5-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43ed5-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="43ed5-158">-SizeInBytes</span></span>
<span data-ttu-id="43ed5-159">SizeInBytes — размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="43ed5-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ed5-160">-WhatIf</span></span>
<span data-ttu-id="43ed5-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43ed5-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43ed5-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43ed5-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43ed5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ed5-163">CommonParameters</span></span>
<span data-ttu-id="43ed5-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43ed5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="43ed5-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ed5-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ed5-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43ed5-166">INPUTS</span></span>

### <span data-ttu-id="43ed5-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43ed5-167">-ResourceGroup</span></span>
 <span data-ttu-id="43ed5-168">System. String</span><span class="sxs-lookup"><span data-stu-id="43ed5-168">System.String</span></span>

### <span data-ttu-id="43ed5-169">-+ +</span><span class="sxs-lookup"><span data-stu-id="43ed5-169">-NamespaceName</span></span>
 <span data-ttu-id="43ed5-170">System. String</span><span class="sxs-lookup"><span data-stu-id="43ed5-170">System.String</span></span>

### <span data-ttu-id="43ed5-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="43ed5-171">-QueueName</span></span>
 <span data-ttu-id="43ed5-172">System. String</span><span class="sxs-lookup"><span data-stu-id="43ed5-172">System.String</span></span>

### <span data-ttu-id="43ed5-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="43ed5-173">-EnablePartitioning</span></span>
 <span data-ttu-id="43ed5-174">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="43ed5-174">System.Boolean?</span></span>


## <span data-ttu-id="43ed5-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43ed5-175">OUTPUTS</span></span>

### <span data-ttu-id="43ed5-176">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="43ed5-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="43ed5-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="43ed5-177">NOTES</span></span>

## <span data-ttu-id="43ed5-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43ed5-178">RELATED LINKS</span></span>
