---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 1d197683e1459173d96958199ad08b437d1d9e04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999779"
---
# <span data-ttu-id="fd6b9-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="fd6b9-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="fd6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6b9-103">Создает очередь "Автобусы обслуживания" в указанном пространстве имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fd6b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd6b9-104">SYNTAX</span></span>

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

## <span data-ttu-id="fd6b9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd6b9-105">DESCRIPTION</span></span>
<span data-ttu-id="fd6b9-106">Для **создания очереди "Автобус** обслуживания" в указанном пространстве имен «Номер обслуживания».</span><span class="sxs-lookup"><span data-stu-id="fd6b9-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fd6b9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd6b9-107">EXAMPLES</span></span>

### <span data-ttu-id="fd6b9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd6b9-108">Example 1</span></span>
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

<span data-ttu-id="fd6b9-109">Создает новую очередь "Автобусы обслуживания" в указанном пространстве имен `SB-Queue_example1` автобусов `SB-Example1` службы.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="fd6b9-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fd6b9-110">Example 2</span></span>

<span data-ttu-id="fd6b9-111">Создает очередь "Автобусы обслуживания" в указанном пространстве имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="fd6b9-112">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="fd6b9-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="fd6b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd6b9-113">PARAMETERS</span></span>

### <span data-ttu-id="fd6b9-114">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="fd6b9-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="fd6b9-115">Определяет [неавтомительный интервал timeSpan,](https://msdn.microsoft.com/library/system.timespan.aspx) после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="fd6b9-116">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="fd6b9-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="fd6b9-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="fd6b9-118">Неявные письма при окончании срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="fd6b9-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="fd6b9-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="fd6b9-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="fd6b9-120">Время отсвея на значение в прямом эфире.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-120">Timespan to live value.</span></span>
<span data-ttu-id="fd6b9-121">Это длительность, по истечении которого срок действия сообщения истекает, начиная с 00:00, с которого сообщение отправляется в "Служлужбу".</span><span class="sxs-lookup"><span data-stu-id="fd6b9-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="fd6b9-122">Это значение по умолчанию используется, когда TimeToLive не заданной в самом сообщении.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="fd6b9-123">Для стандартного = Timespan.Max и Basic = 14 дней</span><span class="sxs-lookup"><span data-stu-id="fd6b9-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="fd6b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6b9-124">-DefaultProfile</span></span>
<span data-ttu-id="fd6b9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd6b9-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="fd6b9-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="fd6b9-127">Указывает период времени повторяютого обнаружения , то есть значение [timeSpan,](https://msdn.microsoft.com/library/system.timespan.aspx) которое определяет продолжительность повторяютого истории обнаружения.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="fd6b9-128">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="fd6b9-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="fd6b9-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="fd6b9-130">Включить пакетные операции — значение, которое указывает, включены ли пакетные операции на сервере</span><span class="sxs-lookup"><span data-stu-id="fd6b9-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="fd6b9-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="fd6b9-131">-EnableExpress</span></span>
<span data-ttu-id="fd6b9-132">EnableExpress — значение, которое показывает, включены ли express entities.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="fd6b9-133">Express queue holds a message in memory temporarily before writing it to persistent storage.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="fd6b9-134">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="fd6b9-134">-EnablePartitioning</span></span>
<span data-ttu-id="fd6b9-135">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="fd6b9-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="fd6b9-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="fd6b9-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="fd6b9-137">Имя очереди или темы для переадстройки сообщения "Ненамеряемая буква"</span><span class="sxs-lookup"><span data-stu-id="fd6b9-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="fd6b9-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="fd6b9-138">-ForwardTo</span></span>
<span data-ttu-id="fd6b9-139">Имя очереди или раздела для переадстройки сообщений</span><span class="sxs-lookup"><span data-stu-id="fd6b9-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="fd6b9-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="fd6b9-140">-LockDuration</span></span>
<span data-ttu-id="fd6b9-141">Длительность блокировки</span><span class="sxs-lookup"><span data-stu-id="fd6b9-141">Lock Duration</span></span>

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

### <span data-ttu-id="fd6b9-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="fd6b9-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="fd6b9-143">MaxDeliveryCount — максимальное число доставки.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="fd6b9-144">Такое количество доставок автоматически затеряется.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="fd6b9-145">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="fd6b9-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="fd6b9-146">MaxSizeInMegabytes — максимальный размер очереди в мегабайтах, то есть объем памяти, выделенной для очереди. Значение по умолчанию — 1024.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="fd6b9-147">Максимум для стандартного SKU составляет 5120, а для premium — 81920, допустимые значения: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="fd6b9-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="fd6b9-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="fd6b9-148">-MessageCount</span></span>
<span data-ttu-id="fd6b9-149">MessageCount — количество сообщений в очереди</span><span class="sxs-lookup"><span data-stu-id="fd6b9-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="fd6b9-150">-Name</span><span class="sxs-lookup"><span data-stu-id="fd6b9-150">-Name</span></span>
<span data-ttu-id="fd6b9-151">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="fd6b9-151">Queue Name</span></span>

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

### <span data-ttu-id="fd6b9-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fd6b9-152">-Namespace</span></span>
<span data-ttu-id="fd6b9-153">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fd6b9-153">Namespace Name</span></span>

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

### <span data-ttu-id="fd6b9-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="fd6b9-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="fd6b9-155">RequiresDuplicateDetection — значение, которое указывает, поддерживает ли очередь концепцию сеанса.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="fd6b9-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="fd6b9-156">-RequiresSession</span></span>
<span data-ttu-id="fd6b9-157">RequiresSession — значение, указывающее, используется ли в очереди сеансы.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="fd6b9-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd6b9-158">-ResourceGroupName</span></span>
<span data-ttu-id="fd6b9-159">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fd6b9-159">The name of the resource group</span></span>

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

### <span data-ttu-id="fd6b9-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="fd6b9-160">-SizeInBytes</span></span>
<span data-ttu-id="fd6b9-161">SizeInBytes — размер очереди в этихбайтах</span><span class="sxs-lookup"><span data-stu-id="fd6b9-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="fd6b9-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd6b9-162">-Confirm</span></span>
<span data-ttu-id="fd6b9-163">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6b9-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6b9-164">-WhatIf</span></span>
<span data-ttu-id="fd6b9-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6b9-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6b9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6b9-167">CommonParameters</span></span>
<span data-ttu-id="fd6b9-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd6b9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6b9-169">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd6b9-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6b9-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd6b9-170">INPUTS</span></span>

### <span data-ttu-id="fd6b9-171">System.String</span><span class="sxs-lookup"><span data-stu-id="fd6b9-171">System.String</span></span>

### <span data-ttu-id="fd6b9-172">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd6b9-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd6b9-173">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd6b9-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd6b9-174">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd6b9-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fd6b9-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd6b9-175">OUTPUTS</span></span>

### <span data-ttu-id="fd6b9-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="fd6b9-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="fd6b9-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd6b9-177">NOTES</span></span>

## <span data-ttu-id="fd6b9-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd6b9-178">RELATED LINKS</span></span>
