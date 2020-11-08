---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247025"
---
# <span data-ttu-id="4b5f3-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="4b5f3-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="4b5f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5f3-103">Создает подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="4b5f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b5f3-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b5f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b5f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4b5f3-106">Командлет **New-AzServiceBusSubscription** создает новую подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="4b5f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b5f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4b5f3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b5f3-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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

<span data-ttu-id="4b5f3-109">Создает подписку `SB-TopicSubscription-Example1` для указанной темы служебной шины `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="4b5f3-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="4b5f3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b5f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4b5f3-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="4b5f3-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="4b5f3-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого подписка автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="4b5f3-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="4b5f3-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="4b5f3-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="4b5f3-115">Значение, указывающее на наличие в подписке поддержки недоставленных сообщений в исключениях для оценки фильтра.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="4b5f3-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="4b5f3-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="4b5f3-117">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="4b5f3-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="4b5f3-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="4b5f3-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="4b5f3-119">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-119">Timespan to live value.</span></span>
<span data-ttu-id="4b5f3-120">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="4b5f3-121">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="4b5f3-122">Для стандартных = TimeSpan. Max и Basic = 14 дней</span><span class="sxs-lookup"><span data-stu-id="4b5f3-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="4b5f3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5f3-123">-DefaultProfile</span></span>
<span data-ttu-id="4b5f3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b5f3-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="4b5f3-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="4b5f3-126">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="4b5f3-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="4b5f3-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="4b5f3-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="4b5f3-128">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="4b5f3-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="4b5f3-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="4b5f3-129">-ForwardTo</span></span>
<span data-ttu-id="4b5f3-130">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="4b5f3-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="4b5f3-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="4b5f3-131">-LockDuration</span></span>
<span data-ttu-id="4b5f3-132">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="4b5f3-132">Lock Duration</span></span>

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

### <span data-ttu-id="4b5f3-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="4b5f3-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="4b5f3-134">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="4b5f3-135">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="4b5f3-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4b5f3-136">-Name</span></span>
<span data-ttu-id="4b5f3-137">Название подписки</span><span class="sxs-lookup"><span data-stu-id="4b5f3-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5f3-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b5f3-138">-Namespace</span></span>
<span data-ttu-id="4b5f3-139">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="4b5f3-139">Namespace Name</span></span>

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

### <span data-ttu-id="4b5f3-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="4b5f3-140">-RequiresSession</span></span>
<span data-ttu-id="4b5f3-141">RequiresSession — значение, показывающее, требуется ли для этой очереди обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="4b5f3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5f3-142">-ResourceGroupName</span></span>
<span data-ttu-id="4b5f3-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-143">The name of the resource group</span></span>

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

### <span data-ttu-id="4b5f3-144">-Темы</span><span class="sxs-lookup"><span data-stu-id="4b5f3-144">-Topic</span></span>
<span data-ttu-id="4b5f3-145">Название раздела</span><span class="sxs-lookup"><span data-stu-id="4b5f3-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5f3-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b5f3-146">-Confirm</span></span>
<span data-ttu-id="4b5f3-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5f3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5f3-148">-WhatIf</span></span>
<span data-ttu-id="4b5f3-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5f3-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5f3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5f3-151">CommonParameters</span></span>
<span data-ttu-id="4b5f3-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b5f3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5f3-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5f3-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5f3-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b5f3-154">INPUTS</span></span>

### <span data-ttu-id="4b5f3-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f3-155">System.String</span></span>

### <span data-ttu-id="4b5f3-156">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b5f3-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4b5f3-157">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b5f3-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4b5f3-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b5f3-158">OUTPUTS</span></span>

### <span data-ttu-id="4b5f3-159">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="4b5f3-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="4b5f3-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b5f3-160">NOTES</span></span>

## <span data-ttu-id="4b5f3-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b5f3-161">RELATED LINKS</span></span>
