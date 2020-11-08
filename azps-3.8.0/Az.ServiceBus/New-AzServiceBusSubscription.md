---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065778"
---
# <span data-ttu-id="9136c-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="9136c-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="9136c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9136c-102">SYNOPSIS</span></span>
<span data-ttu-id="9136c-103">Создает подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9136c-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="9136c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9136c-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9136c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9136c-105">DESCRIPTION</span></span>
<span data-ttu-id="9136c-106">Командлет **New-AzServiceBusSubscription** создает новую подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9136c-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="9136c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9136c-107">EXAMPLES</span></span>

### <span data-ttu-id="9136c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9136c-108">Example 1</span></span>
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

<span data-ttu-id="9136c-109">Создает подписку `SB-TopicSubscription-Example1` для указанной темы служебной шины `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="9136c-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="9136c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9136c-110">PARAMETERS</span></span>

### <span data-ttu-id="9136c-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="9136c-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="9136c-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого подписка автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="9136c-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="9136c-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="9136c-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="9136c-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="9136c-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="9136c-115">Значение, указывающее на наличие в подписке поддержки недоставленных сообщений в исключениях для оценки фильтра.</span><span class="sxs-lookup"><span data-stu-id="9136c-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="9136c-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="9136c-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="9136c-117">Недоставленные письма в течение срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="9136c-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="9136c-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="9136c-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="9136c-119">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="9136c-119">Timespan to live value.</span></span>
<span data-ttu-id="9136c-120">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="9136c-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="9136c-121">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9136c-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="9136c-122">Для стандартных = TimeSpan. Max и Basic = 14 дней</span><span class="sxs-lookup"><span data-stu-id="9136c-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="9136c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9136c-123">-DefaultProfile</span></span>
<span data-ttu-id="9136c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9136c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9136c-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="9136c-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="9136c-126">Включение пакетных операций — значение, указывающее, включены ли пакетные операции на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="9136c-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="9136c-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="9136c-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="9136c-128">Имя очереди/темы для пересылки недоставленного сообщения</span><span class="sxs-lookup"><span data-stu-id="9136c-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="9136c-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="9136c-129">-ForwardTo</span></span>
<span data-ttu-id="9136c-130">Имя очереди/темы для пересылки сообщений</span><span class="sxs-lookup"><span data-stu-id="9136c-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="9136c-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="9136c-131">-LockDuration</span></span>
<span data-ttu-id="9136c-132">Продолжительность блокировки</span><span class="sxs-lookup"><span data-stu-id="9136c-132">Lock Duration</span></span>

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

### <span data-ttu-id="9136c-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="9136c-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="9136c-134">MaxDeliveryCount — максимальное количество доставок.</span><span class="sxs-lookup"><span data-stu-id="9136c-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="9136c-135">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="9136c-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="9136c-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9136c-136">-Name</span></span>
<span data-ttu-id="9136c-137">Название подписки</span><span class="sxs-lookup"><span data-stu-id="9136c-137">Subscription Name</span></span>

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

### <span data-ttu-id="9136c-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9136c-138">-Namespace</span></span>
<span data-ttu-id="9136c-139">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="9136c-139">Namespace Name</span></span>

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

### <span data-ttu-id="9136c-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="9136c-140">-RequiresSession</span></span>
<span data-ttu-id="9136c-141">RequiresSession — значение, показывающее, требуется ли для этой очереди обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="9136c-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="9136c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9136c-142">-ResourceGroupName</span></span>
<span data-ttu-id="9136c-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9136c-143">The name of the resource group</span></span>

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

### <span data-ttu-id="9136c-144">-Темы</span><span class="sxs-lookup"><span data-stu-id="9136c-144">-Topic</span></span>
<span data-ttu-id="9136c-145">Название раздела</span><span class="sxs-lookup"><span data-stu-id="9136c-145">Topic Name</span></span>

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

### <span data-ttu-id="9136c-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9136c-146">-Confirm</span></span>
<span data-ttu-id="9136c-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9136c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9136c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9136c-148">-WhatIf</span></span>
<span data-ttu-id="9136c-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9136c-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9136c-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9136c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9136c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9136c-151">CommonParameters</span></span>
<span data-ttu-id="9136c-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9136c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9136c-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9136c-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9136c-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9136c-154">INPUTS</span></span>

### <span data-ttu-id="9136c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="9136c-155">System.String</span></span>

### <span data-ttu-id="9136c-156">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9136c-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9136c-157">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9136c-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9136c-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9136c-158">OUTPUTS</span></span>

### <span data-ttu-id="9136c-159">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="9136c-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="9136c-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="9136c-160">NOTES</span></span>

## <span data-ttu-id="9136c-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9136c-161">RELATED LINKS</span></span>
