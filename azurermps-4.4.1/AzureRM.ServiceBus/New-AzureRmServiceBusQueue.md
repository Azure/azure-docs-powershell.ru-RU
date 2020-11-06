---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559516"
---
# <span data-ttu-id="1ee60-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="1ee60-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="1ee60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ee60-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee60-103">Создание очереди служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1ee60-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ee60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ee60-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee60-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee60-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee60-106">Командлет **New-AzureRmServiceBusQueue** создает очередь служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1ee60-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1ee60-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ee60-107">EXAMPLES</span></span>

### <span data-ttu-id="1ee60-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ee60-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="1ee60-109">Создание новой очереди служебной шины `SB-Queue_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1ee60-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="1ee60-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ee60-110">PARAMETERS</span></span>

### <span data-ttu-id="1ee60-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="1ee60-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="1ee60-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого очередь автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="1ee60-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="1ee60-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="1ee60-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="1ee60-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="1ee60-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="1ee60-115">Указывает, должны ли deadlettered на срок действия сообщения.</span><span class="sxs-lookup"><span data-stu-id="1ee60-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="1ee60-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="1ee60-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="1ee60-117">Задает время жизни сообщения по умолчанию (TTL).</span><span class="sxs-lookup"><span data-stu-id="1ee60-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="1ee60-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="1ee60-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="1ee60-119">Указывает окно времени журнала обнаружения повторов, valuethat [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="1ee60-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="1ee60-120">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="1ee60-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="1ee60-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="1ee60-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="1ee60-122">Указывает, включены ли пакетные операции на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="1ee60-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="1ee60-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="1ee60-123">-EnableExpress</span></span>
<span data-ttu-id="1ee60-124">Указывает, включены ли функции Express Entities.</span><span class="sxs-lookup"><span data-stu-id="1ee60-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="1ee60-125">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="1ee60-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="1ee60-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="1ee60-126">-EnablePartitioning</span></span>
<span data-ttu-id="1ee60-127">Указывает, включена ли EnablePartitioning.</span><span class="sxs-lookup"><span data-stu-id="1ee60-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee60-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="1ee60-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="1ee60-129">Указывает, будет ли сообщение анонимно доступно.</span><span class="sxs-lookup"><span data-stu-id="1ee60-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="1ee60-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="1ee60-130">-LockDuration</span></span>
<span data-ttu-id="1ee60-131">Задает продолжительность блокировки.</span><span class="sxs-lookup"><span data-stu-id="1ee60-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="1ee60-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="1ee60-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="1ee60-133">Задает максимальное число доставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="1ee60-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="1ee60-134">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="1ee60-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="1ee60-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="1ee60-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="1ee60-136">Указывает максимальный размер очереди в мегабайтах, то есть объем памяти, выделенной для очереди.</span><span class="sxs-lookup"><span data-stu-id="1ee60-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="1ee60-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="1ee60-137">-MessageCount</span></span>
<span data-ttu-id="1ee60-138">Указывает количество сообщений в очереди.</span><span class="sxs-lookup"><span data-stu-id="1ee60-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="1ee60-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="1ee60-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="1ee60-140">Указывает, требуется ли для очереди обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="1ee60-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="1ee60-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="1ee60-141">-RequiresSession</span></span>
<span data-ttu-id="1ee60-142">Указывает, поддерживает ли эта очередь сеансы.</span><span class="sxs-lookup"><span data-stu-id="1ee60-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="1ee60-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1ee60-143">-SizeInBytes</span></span>
<span data-ttu-id="1ee60-144">Размер очереди в байтах.</span><span class="sxs-lookup"><span data-stu-id="1ee60-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="1ee60-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ee60-145">-Confirm</span></span>
<span data-ttu-id="1ee60-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ee60-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee60-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee60-147">-WhatIf</span></span>
<span data-ttu-id="1ee60-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ee60-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee60-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ee60-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee60-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee60-150">-DefaultProfile</span></span>
<span data-ttu-id="1ee60-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ee60-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee60-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ee60-152">-Name</span></span>
<span data-ttu-id="1ee60-153">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="1ee60-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee60-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ee60-154">-Namespace</span></span>
<span data-ttu-id="1ee60-155">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1ee60-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee60-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee60-156">-ResourceGroupName</span></span>
<span data-ttu-id="1ee60-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ee60-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee60-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee60-158">CommonParameters</span></span>
<span data-ttu-id="1ee60-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ee60-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee60-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee60-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee60-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ee60-161">INPUTS</span></span>

### <span data-ttu-id="1ee60-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1ee60-162">-ResourceGroup</span></span>
 <span data-ttu-id="1ee60-163">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee60-163">System.String</span></span>

### <span data-ttu-id="1ee60-164">-+ +</span><span class="sxs-lookup"><span data-stu-id="1ee60-164">-NamespaceName</span></span>
 <span data-ttu-id="1ee60-165">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee60-165">System.String</span></span>

### <span data-ttu-id="1ee60-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="1ee60-166">-QueueName</span></span>
 <span data-ttu-id="1ee60-167">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee60-167">System.String</span></span>

### <span data-ttu-id="1ee60-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="1ee60-168">-EnablePartitioning</span></span>
 <span data-ttu-id="1ee60-169">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="1ee60-169">System.Boolean?</span></span>

## <span data-ttu-id="1ee60-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ee60-170">OUTPUTS</span></span>

### <span data-ttu-id="1ee60-171">Microsoft. Azure. Commands. ServiceBus. Models. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="1ee60-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="1ee60-172">Name (имя): SB-Queue_exampl1 Location (Западная часть США): AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 – DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations, DeadLetteringOnMessageExpiration: false EnableExpress: "true EnablePartitioning:" IsAnonymousAccessible: MaxDeliveryCount: 1/20/2017 2:51:37 MaxSizeInMegabytes: "false MessageCount:" для "16384 CountDetails"</span><span class="sxs-lookup"><span data-stu-id="1ee60-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="1ee60-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ee60-173">NOTES</span></span>

## <span data-ttu-id="1ee60-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ee60-174">RELATED LINKS</span></span>

