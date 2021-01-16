---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415335"
---
# <span data-ttu-id="ad7e0-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ad7e0-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="ad7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7e0-103">Создает подписку на указанную тему "Служлужбу".</span><span class="sxs-lookup"><span data-stu-id="ad7e0-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="ad7e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad7e0-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad7e0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad7e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ad7e0-106">Для **указанной темы** "Служни" создается новая подписка.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="ad7e0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad7e0-107">EXAMPLES</span></span>

### <span data-ttu-id="ad7e0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad7e0-108">Example 1</span></span>
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

<span data-ttu-id="ad7e0-109">Создает подписку для `SB-TopicSubscription-Example1` указанной темы "Служский `SB-Topic_exampl1` автобус".</span><span class="sxs-lookup"><span data-stu-id="ad7e0-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="ad7e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad7e0-110">PARAMETERS</span></span>

### <span data-ttu-id="ad7e0-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="ad7e0-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="ad7e0-112">Указывает [неавтомительный](https://msdn.microsoft.com/library/system.timespan.aspx) интервал интервала времени, после которого подписка будет автоматически удалена.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="ad7e0-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="ad7e0-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="ad7e0-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="ad7e0-115">Значение, которое указывает на то, есть ли в подписке неявные письма в исключениях при оценке фильтра.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="ad7e0-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="ad7e0-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="ad7e0-117">Неявные письма при окончании срока действия сообщения</span><span class="sxs-lookup"><span data-stu-id="ad7e0-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="ad7e0-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ad7e0-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="ad7e0-119">Время отсвея на значение в прямом эфире.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-119">Timespan to live value.</span></span>
<span data-ttu-id="ad7e0-120">Это длительность, по истечении которого срок действия сообщения истекает, начиная с 00:00, когда сообщение отправляется в "Служлужбу".</span><span class="sxs-lookup"><span data-stu-id="ad7e0-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="ad7e0-121">Это значение используется по умолчанию, если TimeToLive не заданной для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="ad7e0-122">Для стандартного = Timespan.Max и Basic = 14 дней</span><span class="sxs-lookup"><span data-stu-id="ad7e0-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="ad7e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7e0-123">-DefaultProfile</span></span>
<span data-ttu-id="ad7e0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad7e0-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ad7e0-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="ad7e0-126">Включить пакетные операции — значение, которое указывает, включены ли пакетные операции на сервере</span><span class="sxs-lookup"><span data-stu-id="ad7e0-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="ad7e0-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="ad7e0-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="ad7e0-128">Имя очереди или темы для переадстройки сообщения "Ненамеряемая буква"</span><span class="sxs-lookup"><span data-stu-id="ad7e0-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="ad7e0-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="ad7e0-129">-ForwardTo</span></span>
<span data-ttu-id="ad7e0-130">Имя очереди или раздела для переадстройки сообщений</span><span class="sxs-lookup"><span data-stu-id="ad7e0-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="ad7e0-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="ad7e0-131">-LockDuration</span></span>
<span data-ttu-id="ad7e0-132">Длительность блокировки</span><span class="sxs-lookup"><span data-stu-id="ad7e0-132">Lock Duration</span></span>

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

### <span data-ttu-id="ad7e0-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="ad7e0-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="ad7e0-134">MaxDeliveryCount — максимальное число доставки.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="ad7e0-135">Такое количество доставок автоматически затеряется.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="ad7e0-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ad7e0-136">-Name</span></span>
<span data-ttu-id="ad7e0-137">Название подписки</span><span class="sxs-lookup"><span data-stu-id="ad7e0-137">Subscription Name</span></span>

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

### <span data-ttu-id="ad7e0-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ad7e0-138">-Namespace</span></span>
<span data-ttu-id="ad7e0-139">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ad7e0-139">Namespace Name</span></span>

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

### <span data-ttu-id="ad7e0-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="ad7e0-140">-RequiresSession</span></span>
<span data-ttu-id="ad7e0-141">RequiresSession — значение, указывающее, требуется ли для этой очереди дублирование обнаружения.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="ad7e0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7e0-142">-ResourceGroupName</span></span>
<span data-ttu-id="ad7e0-143">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ad7e0-143">The name of the resource group</span></span>

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

### <span data-ttu-id="ad7e0-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="ad7e0-144">-Topic</span></span>
<span data-ttu-id="ad7e0-145">Название темы</span><span class="sxs-lookup"><span data-stu-id="ad7e0-145">Topic Name</span></span>

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

### <span data-ttu-id="ad7e0-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad7e0-146">-Confirm</span></span>
<span data-ttu-id="ad7e0-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7e0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7e0-148">-WhatIf</span></span>
<span data-ttu-id="ad7e0-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad7e0-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad7e0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7e0-151">CommonParameters</span></span>
<span data-ttu-id="ad7e0-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad7e0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7e0-153">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7e0-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7e0-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad7e0-154">INPUTS</span></span>

### <span data-ttu-id="ad7e0-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ad7e0-155">System.String</span></span>

### <span data-ttu-id="ad7e0-156">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad7e0-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ad7e0-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad7e0-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ad7e0-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad7e0-158">OUTPUTS</span></span>

### <span data-ttu-id="ad7e0-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ad7e0-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="ad7e0-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad7e0-160">NOTES</span></span>

## <span data-ttu-id="ad7e0-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad7e0-161">RELATED LINKS</span></span>
