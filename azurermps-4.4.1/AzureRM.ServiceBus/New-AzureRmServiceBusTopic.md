---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562183"
---
# <span data-ttu-id="7eba7-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7eba7-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="7eba7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7eba7-102">SYNOPSIS</span></span>
<span data-ttu-id="7eba7-103">Создает новую тему служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="7eba7-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eba7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7eba7-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eba7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eba7-105">DESCRIPTION</span></span>
<span data-ttu-id="7eba7-106">Командлет **New-AzureRmServiceBusTopic** создает новую тему служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="7eba7-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7eba7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7eba7-107">EXAMPLES</span></span>

### <span data-ttu-id="7eba7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7eba7-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="7eba7-109">Создает новую тему служебной шины `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7eba7-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7eba7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7eba7-110">PARAMETERS</span></span>

### <span data-ttu-id="7eba7-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="7eba7-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="7eba7-112">Задает интервал бездействия в [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого автоматически удаляется раздел.</span><span class="sxs-lookup"><span data-stu-id="7eba7-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="7eba7-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="7eba7-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="7eba7-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="7eba7-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="7eba7-115">Указывает срок действия сообщения, начиная с того момента, когда сообщение отправляется на служебную служебную.</span><span class="sxs-lookup"><span data-stu-id="7eba7-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="7eba7-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="7eba7-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="7eba7-117">Задает структуру [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , которая определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="7eba7-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="7eba7-118">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="7eba7-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="7eba7-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="7eba7-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="7eba7-120">Указывает, включены ли пакетные операции на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7eba7-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="7eba7-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="7eba7-121">-EnableExpress</span></span>
<span data-ttu-id="7eba7-122">Указывает, включены ли функции Express Entities.</span><span class="sxs-lookup"><span data-stu-id="7eba7-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="7eba7-123">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="7eba7-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="7eba7-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7eba7-124">-EnablePartitioning</span></span>
<span data-ttu-id="7eba7-125">Указывает, следует ли включить секционирование темы в нескольких брокерах сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eba7-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="7eba7-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="7eba7-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="7eba7-127">Указывает, следует ли включить секционирование подписок.</span><span class="sxs-lookup"><span data-stu-id="7eba7-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="7eba7-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="7eba7-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="7eba7-129">Указывает, включена ли фильтрация для сообщений перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="7eba7-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="7eba7-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="7eba7-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="7eba7-131">Указывает, допускает ли сообщение анонимный доступ.</span><span class="sxs-lookup"><span data-stu-id="7eba7-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="7eba7-132">-Express</span><span class="sxs-lookup"><span data-stu-id="7eba7-132">-IsExpress</span></span>
<span data-ttu-id="7eba7-133">Указывает, включена ли в этой теме Экспресс.</span><span class="sxs-lookup"><span data-stu-id="7eba7-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="7eba7-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7eba7-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="7eba7-135">Максимальный размер темы в мегабайтах, которая является размером памяти, выделенной для темы.</span><span class="sxs-lookup"><span data-stu-id="7eba7-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="7eba7-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="7eba7-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="7eba7-137">Указывает, требуется ли для темы обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="7eba7-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="7eba7-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="7eba7-138">-SizeInBytes</span></span>
<span data-ttu-id="7eba7-139">Указывает размер темы в байтах.</span><span class="sxs-lookup"><span data-stu-id="7eba7-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="7eba7-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="7eba7-140">-SupportOrdering</span></span>
<span data-ttu-id="7eba7-141">Указывает, поддерживает ли раздел сортировку.</span><span class="sxs-lookup"><span data-stu-id="7eba7-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="7eba7-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7eba7-142">-Confirm</span></span>
<span data-ttu-id="7eba7-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7eba7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eba7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eba7-144">-WhatIf</span></span>
<span data-ttu-id="7eba7-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7eba7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eba7-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7eba7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eba7-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eba7-147">-DefaultProfile</span></span>
<span data-ttu-id="7eba7-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7eba7-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eba7-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7eba7-149">-Name</span></span>
<span data-ttu-id="7eba7-150">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="7eba7-150">Topic Name.</span></span>

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

### <span data-ttu-id="7eba7-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7eba7-151">-Namespace</span></span>
<span data-ttu-id="7eba7-152">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7eba7-152">Namespace Name.</span></span>

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

### <span data-ttu-id="7eba7-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eba7-153">-ResourceGroupName</span></span>
<span data-ttu-id="7eba7-154">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7eba7-154">The name of the resource group</span></span>

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

### <span data-ttu-id="7eba7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eba7-155">CommonParameters</span></span>
<span data-ttu-id="7eba7-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7eba7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eba7-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eba7-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eba7-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7eba7-158">INPUTS</span></span>

### <span data-ttu-id="7eba7-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7eba7-159">System.String</span></span>
<span data-ttu-id="7eba7-160">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="7eba7-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="7eba7-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7eba7-161">-ResourceGroup</span></span>
 <span data-ttu-id="7eba7-162">System. String</span><span class="sxs-lookup"><span data-stu-id="7eba7-162">System.String</span></span>

### <span data-ttu-id="7eba7-163">-+ +</span><span class="sxs-lookup"><span data-stu-id="7eba7-163">-NamespaceName</span></span>
 <span data-ttu-id="7eba7-164">System. String</span><span class="sxs-lookup"><span data-stu-id="7eba7-164">System.String</span></span>

### <span data-ttu-id="7eba7-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7eba7-165">-TopicName</span></span>
 <span data-ttu-id="7eba7-166">System. String</span><span class="sxs-lookup"><span data-stu-id="7eba7-166">System.String</span></span>

### <span data-ttu-id="7eba7-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="7eba7-167">-EnablePartitioning</span></span>
 <span data-ttu-id="7eba7-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="7eba7-168">System.Boolean?</span></span>

## <span data-ttu-id="7eba7-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eba7-169">OUTPUTS</span></span>

### <span data-ttu-id="7eba7-170">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="7eba7-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="7eba7-171">Name (имя): SB-Topic_exampl1 расположение: Западная часть US ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B – Topic_exampl1 Type (тип): Microsoft. ServiceBus/тема AccessedAt: AutoDeleteOnIdle: 10675199.02:05.4775807: EntityAvailabilityStatus CreatedAt: CountDetails. 1/20/2017 3:16:42 DefaultMessageTimeToLive: 48:10675199.02 05.4775807: DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: false EnableExpress: false EnablePartitioning: false: ложь EnableSubscriptionPartitioning: ложь FilteringMessagesBeforePublishing: ложь IsAnonymousAccessible: ложь-да-значение 1/20/2017 3:16:43 16384.</span><span class="sxs-lookup"><span data-stu-id="7eba7-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="7eba7-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="7eba7-172">NOTES</span></span>

## <span data-ttu-id="7eba7-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eba7-173">RELATED LINKS</span></span>

