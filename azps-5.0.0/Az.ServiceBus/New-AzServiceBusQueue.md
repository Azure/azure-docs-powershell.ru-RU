---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249377"
---
# <span data-ttu-id="d9650-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="d9650-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="d9650-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9650-102">SYNOPSIS</span></span>
<span data-ttu-id="d9650-103">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="d9650-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d9650-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9650-104">SYNTAX</span></span>

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

## <span data-ttu-id="d9650-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9650-105">DESCRIPTION</span></span>
<span data-ttu-id="d9650-106">Командлет **New-AzServiceBusQueue** создает очередь служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="d9650-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d9650-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9650-107">EXAMPLES</span></span>

### <span data-ttu-id="d9650-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9650-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="d9650-109">Создание новой очереди служебной шины `SB-Queue_example1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d9650-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d9650-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d9650-110">Example 2</span></span>

<span data-ttu-id="d9650-111">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="d9650-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="d9650-112">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="d9650-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="d9650-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9650-113">PARAMETERS</span></span>

### <span data-ttu-id="d9650-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="d9650-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="d9650-115">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="d9650-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="d9650-116">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="d9650-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="d9650-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="d9650-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="d9650-118">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="d9650-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="d9650-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d9650-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="d9650-120">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="d9650-120">Timespan to live value.</span></span>
<span data-ttu-id="d9650-121">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="d9650-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="d9650-122">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="d9650-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="d9650-123">Для стандартных = TimeSpan. Max и Basic = 14 дней</span><span class="sxs-lookup"><span data-stu-id="d9650-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="d9650-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9650-124">-DefaultProfile</span></span>
<span data-ttu-id="d9650-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9650-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9650-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="d9650-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="d9650-127">Указывает временное окно журнала обнаружения повторений, значение [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , определяющее продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="d9650-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="d9650-128">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="d9650-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="d9650-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="d9650-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="d9650-130">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="d9650-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="d9650-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="d9650-131">-EnableExpress</span></span>
<span data-ttu-id="d9650-132">EnableExpress — значение, показывающее, включены ли выражения для Экспресс-сущностей.</span><span class="sxs-lookup"><span data-stu-id="d9650-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="d9650-133">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d9650-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="d9650-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="d9650-134">-EnablePartitioning</span></span>
<span data-ttu-id="d9650-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="d9650-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="d9650-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="d9650-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="d9650-137">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="d9650-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="d9650-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="d9650-138">-ForwardTo</span></span>
<span data-ttu-id="d9650-139">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="d9650-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="d9650-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="d9650-140">-LockDuration</span></span>
<span data-ttu-id="d9650-141">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="d9650-141">Lock Duration</span></span>

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

### <span data-ttu-id="d9650-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d9650-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="d9650-143">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="d9650-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="d9650-144">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="d9650-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="d9650-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="d9650-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="d9650-146">MaxSizeInMegabytes — максимальный размер очереди в мегабайтах, который является размером памяти, выделенной для очереди. Значение по умолчанию — 1024.</span><span class="sxs-lookup"><span data-stu-id="d9650-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="d9650-147">Макс. для стандартной SKU — 5120, а для Premium SKU — 81920, разрешенные значения: 1024, 2048, 3072, 4096, 5120, 10240, 20480,, 40960</span><span class="sxs-lookup"><span data-stu-id="d9650-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="d9650-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="d9650-148">-MessageCount</span></span>
<span data-ttu-id="d9650-149">MessageCount — количество сообщений в очереди</span><span class="sxs-lookup"><span data-stu-id="d9650-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="d9650-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9650-150">-Name</span></span>
<span data-ttu-id="d9650-151">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="d9650-151">Queue Name</span></span>

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

### <span data-ttu-id="d9650-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d9650-152">-Namespace</span></span>
<span data-ttu-id="d9650-153">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="d9650-153">Namespace Name</span></span>

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

### <span data-ttu-id="d9650-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="d9650-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="d9650-155">RequiresDuplicateDetection — значение, указывающее, поддерживает ли очередь понятие сеанса</span><span class="sxs-lookup"><span data-stu-id="d9650-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="d9650-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="d9650-156">-RequiresSession</span></span>
<span data-ttu-id="d9650-157">RequiresSession — значение, показывающее, использует ли очередь сеансы</span><span class="sxs-lookup"><span data-stu-id="d9650-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="d9650-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9650-158">-ResourceGroupName</span></span>
<span data-ttu-id="d9650-159">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d9650-159">The name of the resource group</span></span>

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

### <span data-ttu-id="d9650-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="d9650-160">-SizeInBytes</span></span>
<span data-ttu-id="d9650-161">SizeInBytes — размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="d9650-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="d9650-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9650-162">-Confirm</span></span>
<span data-ttu-id="d9650-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9650-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9650-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9650-164">-WhatIf</span></span>
<span data-ttu-id="d9650-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9650-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9650-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9650-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9650-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9650-167">CommonParameters</span></span>
<span data-ttu-id="d9650-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9650-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9650-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9650-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9650-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9650-170">INPUTS</span></span>

### <span data-ttu-id="d9650-171">System. String</span><span class="sxs-lookup"><span data-stu-id="d9650-171">System.String</span></span>

### <span data-ttu-id="d9650-172">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9650-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d9650-173">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9650-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d9650-174">System. Nullable "1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d9650-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d9650-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9650-175">OUTPUTS</span></span>

### <span data-ttu-id="d9650-176">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="d9650-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="d9650-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9650-177">NOTES</span></span>

## <span data-ttu-id="d9650-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9650-178">RELATED LINKS</span></span>
