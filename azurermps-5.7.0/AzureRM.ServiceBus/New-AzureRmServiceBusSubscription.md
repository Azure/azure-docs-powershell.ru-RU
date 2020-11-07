---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733217"
---
# <span data-ttu-id="c04f5-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="c04f5-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="c04f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c04f5-102">SYNOPSIS</span></span>
<span data-ttu-id="c04f5-103">Создает подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c04f5-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c04f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c04f5-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c04f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c04f5-105">DESCRIPTION</span></span>
<span data-ttu-id="c04f5-106">Командлет **New-AzureRmServiceBusSubscription** создает новую подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="c04f5-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="c04f5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c04f5-107">EXAMPLES</span></span>

### <span data-ttu-id="c04f5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c04f5-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```
<span data-ttu-id="c04f5-109">Создает подписку `SB-TopicSubscription-Example1` для указанной темы служебной шины `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="c04f5-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="c04f5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c04f5-110">PARAMETERS</span></span>

### <span data-ttu-id="c04f5-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="c04f5-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="c04f5-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого подписка автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="c04f5-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="c04f5-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="c04f5-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="c04f5-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c04f5-114">-Confirm</span></span>
<span data-ttu-id="c04f5-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c04f5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c04f5-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="c04f5-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="c04f5-117">Значение, указывающее на наличие в подписке поддержки недоставленных сообщений в исключениях для оценки фильтра.</span><span class="sxs-lookup"><span data-stu-id="c04f5-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="c04f5-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="c04f5-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="c04f5-119">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="c04f5-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="c04f5-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c04f5-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="c04f5-121">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="c04f5-121">Timespan to live value.</span></span>
<span data-ttu-id="c04f5-122">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="c04f5-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="c04f5-123">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="c04f5-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="c04f5-124">Для стандартных = TimeSpan. Max и Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="c04f5-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="c04f5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c04f5-125">-DefaultProfile</span></span>
<span data-ttu-id="c04f5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c04f5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c04f5-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="c04f5-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="c04f5-128">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="c04f5-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="c04f5-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="c04f5-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="c04f5-130">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="c04f5-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="c04f5-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="c04f5-131">-ForwardTo</span></span>
<span data-ttu-id="c04f5-132">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="c04f5-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="c04f5-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="c04f5-133">-LockDuration</span></span>
<span data-ttu-id="c04f5-134">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="c04f5-134">Lock Duration</span></span>

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

### <span data-ttu-id="c04f5-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="c04f5-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="c04f5-136">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="c04f5-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="c04f5-137">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="c04f5-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="c04f5-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c04f5-138">-Name</span></span>
<span data-ttu-id="c04f5-139">Название подписки</span><span class="sxs-lookup"><span data-stu-id="c04f5-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c04f5-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c04f5-140">-Namespace</span></span>
<span data-ttu-id="c04f5-141">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c04f5-141">Namespace Name</span></span>

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

### <span data-ttu-id="c04f5-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="c04f5-142">-RequiresSession</span></span>
<span data-ttu-id="c04f5-143">RequiresSession — значение, показывающее, требуется ли для этой очереди обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="c04f5-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="c04f5-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c04f5-144">-ResourceGroupName</span></span>
<span data-ttu-id="c04f5-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c04f5-145">The name of the resource group</span></span>

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

### <span data-ttu-id="c04f5-146">-Темы</span><span class="sxs-lookup"><span data-stu-id="c04f5-146">-Topic</span></span>
<span data-ttu-id="c04f5-147">Название раздела</span><span class="sxs-lookup"><span data-stu-id="c04f5-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c04f5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c04f5-148">-WhatIf</span></span>
<span data-ttu-id="c04f5-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c04f5-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c04f5-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c04f5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c04f5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c04f5-151">CommonParameters</span></span>
<span data-ttu-id="c04f5-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c04f5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c04f5-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c04f5-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c04f5-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c04f5-154">INPUTS</span></span>

### <span data-ttu-id="c04f5-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c04f5-155">-ResourceGroup</span></span>
 <span data-ttu-id="c04f5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c04f5-156">System.String</span></span>
 

### <span data-ttu-id="c04f5-157">-+ +</span><span class="sxs-lookup"><span data-stu-id="c04f5-157">-NamespaceName</span></span>
 <span data-ttu-id="c04f5-158">System. String</span><span class="sxs-lookup"><span data-stu-id="c04f5-158">System.String</span></span>
 

### <span data-ttu-id="c04f5-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c04f5-159">-TopicName</span></span>
 <span data-ttu-id="c04f5-160">System. String</span><span class="sxs-lookup"><span data-stu-id="c04f5-160">System.String</span></span>
 

### <span data-ttu-id="c04f5-161">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c04f5-161">-SubscriptionName</span></span>
 <span data-ttu-id="c04f5-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c04f5-162">System.String</span></span>


## <span data-ttu-id="c04f5-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c04f5-163">OUTPUTS</span></span>

### <span data-ttu-id="c04f5-164">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="c04f5-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="c04f5-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="c04f5-165">NOTES</span></span>

## <span data-ttu-id="c04f5-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c04f5-166">RELATED LINKS</span></span>
