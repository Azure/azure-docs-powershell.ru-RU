---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732838"
---
# <span data-ttu-id="b269a-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="b269a-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="b269a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b269a-102">SYNOPSIS</span></span>
<span data-ttu-id="b269a-103">Создает новую тему служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="b269a-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b269a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b269a-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b269a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b269a-105">DESCRIPTION</span></span>
<span data-ttu-id="b269a-106">Командлет **New-AzureRmServiceBusTopic** создает новую тему служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="b269a-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b269a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b269a-107">EXAMPLES</span></span>

### <span data-ttu-id="b269a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b269a-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="b269a-109">Создает новую тему служебной шины `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b269a-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="b269a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b269a-110">PARAMETERS</span></span>

### <span data-ttu-id="b269a-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b269a-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b269a-112">Задает интервал бездействия в [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого автоматически удаляется раздел.</span><span class="sxs-lookup"><span data-stu-id="b269a-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="b269a-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="b269a-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b269a-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b269a-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b269a-115">Указывает срок действия сообщения, начиная с того момента, когда сообщение отправляется на служебную служебную.</span><span class="sxs-lookup"><span data-stu-id="b269a-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="b269a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b269a-116">-DefaultProfile</span></span>
<span data-ttu-id="b269a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b269a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b269a-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b269a-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="b269a-119">Задает структуру [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , которая определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="b269a-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="b269a-120">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="b269a-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="b269a-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b269a-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="b269a-122">Указывает, включены ли пакетные операции на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b269a-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="b269a-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="b269a-123">-EnableExpress</span></span>
<span data-ttu-id="b269a-124">Указывает, включены ли функции Express Entities.</span><span class="sxs-lookup"><span data-stu-id="b269a-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="b269a-125">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="b269a-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="b269a-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b269a-126">-EnablePartitioning</span></span>
<span data-ttu-id="b269a-127">Указывает, следует ли включить секционирование темы в нескольких брокерах сообщений.</span><span class="sxs-lookup"><span data-stu-id="b269a-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b269a-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="b269a-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="b269a-129">Максимальный размер темы в мегабайтах, которая является размером памяти, выделенной для темы.</span><span class="sxs-lookup"><span data-stu-id="b269a-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="b269a-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b269a-130">-Name</span></span>
<span data-ttu-id="b269a-131">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="b269a-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b269a-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b269a-132">-Namespace</span></span>
<span data-ttu-id="b269a-133">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b269a-133">Namespace Name.</span></span>

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

### <span data-ttu-id="b269a-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="b269a-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="b269a-135">Указывает, требуется ли для темы обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="b269a-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="b269a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b269a-136">-ResourceGroupName</span></span>
<span data-ttu-id="b269a-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b269a-137">The name of the resource group</span></span>

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

### <span data-ttu-id="b269a-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b269a-138">-SizeInBytes</span></span>
<span data-ttu-id="b269a-139">Указывает размер темы в байтах.</span><span class="sxs-lookup"><span data-stu-id="b269a-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="b269a-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="b269a-140">-SupportOrdering</span></span>
<span data-ttu-id="b269a-141">Указывает, поддерживает ли раздел сортировку.</span><span class="sxs-lookup"><span data-stu-id="b269a-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="b269a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b269a-142">-Confirm</span></span>
<span data-ttu-id="b269a-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b269a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b269a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b269a-144">-WhatIf</span></span>
<span data-ttu-id="b269a-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b269a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b269a-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b269a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b269a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b269a-147">CommonParameters</span></span>
<span data-ttu-id="b269a-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b269a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b269a-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b269a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b269a-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b269a-150">INPUTS</span></span>

### <span data-ttu-id="b269a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b269a-151">System.String</span></span>
<span data-ttu-id="b269a-152">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="b269a-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="b269a-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b269a-153">-ResourceGroup</span></span>
 <span data-ttu-id="b269a-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b269a-154">System.String</span></span>

### <span data-ttu-id="b269a-155">-+ +</span><span class="sxs-lookup"><span data-stu-id="b269a-155">-NamespaceName</span></span>
 <span data-ttu-id="b269a-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b269a-156">System.String</span></span>

### <span data-ttu-id="b269a-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b269a-157">-TopicName</span></span>
 <span data-ttu-id="b269a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b269a-158">System.String</span></span>

### <span data-ttu-id="b269a-159">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="b269a-159">-EnablePartitioning</span></span>
 <span data-ttu-id="b269a-160">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="b269a-160">System.Boolean?</span></span>

## <span data-ttu-id="b269a-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b269a-161">OUTPUTS</span></span>

### <span data-ttu-id="b269a-162">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="b269a-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="b269a-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="b269a-163">NOTES</span></span>

## <span data-ttu-id="b269a-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b269a-164">RELATED LINKS</span></span>

