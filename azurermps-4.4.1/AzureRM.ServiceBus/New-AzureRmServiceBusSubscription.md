---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565131"
---
# <span data-ttu-id="3d94e-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="3d94e-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="3d94e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d94e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d94e-103">Создает подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3d94e-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d94e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d94e-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d94e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d94e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d94e-106">Командлет **New-AzureRmServiceBusSubscription** создает новую подписку на определенную тему служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3d94e-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="3d94e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d94e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d94e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d94e-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="3d94e-109">Создает подписку `SB-TopicSubscription-Example1` для указанной темы служебной шины `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="3d94e-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="3d94e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d94e-110">PARAMETERS</span></span>

### <span data-ttu-id="3d94e-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="3d94e-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="3d94e-112">Указывает интервал простоя [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого подписка автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="3d94e-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="3d94e-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="3d94e-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="3d94e-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="3d94e-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="3d94e-115">Указывает, есть ли в подписке поддержка недоставленных сообщений в исключениях для оценки фильтра.</span><span class="sxs-lookup"><span data-stu-id="3d94e-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="3d94e-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="3d94e-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="3d94e-117">Указывает, есть ли у подписки поддержка недоставленных сообщений после истечения срока действия сообщения.</span><span class="sxs-lookup"><span data-stu-id="3d94e-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="3d94e-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="3d94e-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="3d94e-119">Указывает, включены ли пакетные операции на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="3d94e-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="3d94e-120">-ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3d94e-120">-IsReadOnly</span></span>
<span data-ttu-id="3d94e-121">Указывает, доступно ли Описание сущности только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d94e-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="3d94e-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="3d94e-122">-LockDuration</span></span>
<span data-ttu-id="3d94e-123">Задает продолжительность блокировки для подписки.</span><span class="sxs-lookup"><span data-stu-id="3d94e-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="3d94e-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3d94e-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="3d94e-125">Указывает количество максимальных поставок.</span><span class="sxs-lookup"><span data-stu-id="3d94e-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="3d94e-126">Сообщение автоматически deadlettered после того, как это количество поставок.</span><span class="sxs-lookup"><span data-stu-id="3d94e-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="3d94e-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="3d94e-127">-RequiresSession</span></span>
<span data-ttu-id="3d94e-128">Указывает, поддерживает ли подписка концепцию сеансов.</span><span class="sxs-lookup"><span data-stu-id="3d94e-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="3d94e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d94e-129">-Confirm</span></span>
<span data-ttu-id="3d94e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d94e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d94e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d94e-131">-WhatIf</span></span>
<span data-ttu-id="3d94e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d94e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d94e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d94e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d94e-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3d94e-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="3d94e-135">TimeSpan на значение Live.</span><span class="sxs-lookup"><span data-stu-id="3d94e-135">Timespan to live value.</span></span> <span data-ttu-id="3d94e-136">Это продолжительность срока действия сообщения, начиная с, когда сообщение отправляется на служебную служебную шину.</span><span class="sxs-lookup"><span data-stu-id="3d94e-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="3d94e-137">Это значение по умолчанию, которое используется, если TimeToLive не задано для самого сообщения.</span><span class="sxs-lookup"><span data-stu-id="3d94e-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="3d94e-138">Для стандартных = TimeSpan. Max и Basic = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="3d94e-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="3d94e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d94e-139">-DefaultProfile</span></span>
<span data-ttu-id="3d94e-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d94e-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d94e-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d94e-141">-Name</span></span>
<span data-ttu-id="3d94e-142">Название подписки</span><span class="sxs-lookup"><span data-stu-id="3d94e-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d94e-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d94e-143">-Namespace</span></span>
<span data-ttu-id="3d94e-144">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3d94e-144">Namespace Name.</span></span>

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

### <span data-ttu-id="3d94e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d94e-145">-ResourceGroupName</span></span>
<span data-ttu-id="3d94e-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d94e-146">The name of the resource group</span></span>

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

### <span data-ttu-id="3d94e-147">-Темы</span><span class="sxs-lookup"><span data-stu-id="3d94e-147">-Topic</span></span>
<span data-ttu-id="3d94e-148">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="3d94e-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d94e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d94e-149">CommonParameters</span></span>
<span data-ttu-id="3d94e-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d94e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d94e-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d94e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d94e-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d94e-152">INPUTS</span></span>

### <span data-ttu-id="3d94e-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d94e-153">-ResourceGroup</span></span>
 <span data-ttu-id="3d94e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3d94e-154">System.String</span></span>
 

### <span data-ttu-id="3d94e-155">-+ +</span><span class="sxs-lookup"><span data-stu-id="3d94e-155">-NamespaceName</span></span>
 <span data-ttu-id="3d94e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3d94e-156">System.String</span></span>
 

### <span data-ttu-id="3d94e-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3d94e-157">-TopicName</span></span>
 <span data-ttu-id="3d94e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3d94e-158">System.String</span></span>
 

### <span data-ttu-id="3d94e-159">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3d94e-159">-SubscriptionName</span></span>
 <span data-ttu-id="3d94e-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3d94e-160">System.String</span></span>

## <span data-ttu-id="3d94e-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d94e-161">OUTPUTS</span></span>

### <span data-ttu-id="3d94e-162">Microsoft. Azure. Commands. ServiceBus. Models. SubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="3d94e-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="3d94e-163">Имя: SB-TopicSubscription-example1: Западная часть США AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus: "ложь": LockDuration: 00:01:00 MaxDeliveryCount. 1/20/2017 3:18:54</span><span class="sxs-lookup"><span data-stu-id="3d94e-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="3d94e-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d94e-164">NOTES</span></span>

## <span data-ttu-id="3d94e-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d94e-165">RELATED LINKS</span></span>

