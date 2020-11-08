---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
ms.openlocfilehash: 33952d26d92ce0e70136afe900d7cff479f316b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065777"
---
# <span data-ttu-id="ef03a-101">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ef03a-101">New-AzServiceBusTopic</span></span>

## <span data-ttu-id="ef03a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef03a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef03a-103">Создает новую тему служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ef03a-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ef03a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef03a-104">SYNTAX</span></span>

```
New-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef03a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef03a-105">DESCRIPTION</span></span>
<span data-ttu-id="ef03a-106">Командлет **New-AzServiceBusTopic** создает новую тему служебной шины в указанном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ef03a-106">The **New-AzServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ef03a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef03a-107">EXAMPLES</span></span>

### <span data-ttu-id="ef03a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef03a-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="ef03a-109">Создает новую тему служебной шины `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ef03a-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="ef03a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef03a-110">PARAMETERS</span></span>

### <span data-ttu-id="ef03a-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="ef03a-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="ef03a-112">Задает интервал бездействия в [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , после которого автоматически удаляется раздел.</span><span class="sxs-lookup"><span data-stu-id="ef03a-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="ef03a-113">Минимальная длительность — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="ef03a-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="ef03a-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ef03a-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="ef03a-115">Указывает срок действия сообщения, начиная с того момента, когда сообщение отправляется на служебную служебную.</span><span class="sxs-lookup"><span data-stu-id="ef03a-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="ef03a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef03a-116">-DefaultProfile</span></span>
<span data-ttu-id="ef03a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef03a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef03a-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="ef03a-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="ef03a-119">Задает структуру [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) , которая определяет продолжительность истории обнаружения повторений.</span><span class="sxs-lookup"><span data-stu-id="ef03a-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="ef03a-120">Значение по умолчанию — 10 минут.</span><span class="sxs-lookup"><span data-stu-id="ef03a-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="ef03a-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ef03a-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="ef03a-122">Указывает, включены ли пакетные операции на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="ef03a-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="ef03a-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="ef03a-123">-EnableExpress</span></span>
<span data-ttu-id="ef03a-124">Указывает, включены ли функции Express Entities.</span><span class="sxs-lookup"><span data-stu-id="ef03a-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="ef03a-125">Быстрая очередь содержит сообщение в памяти на временное время, прежде чем записывать его в постоянное хранилище.</span><span class="sxs-lookup"><span data-stu-id="ef03a-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="ef03a-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="ef03a-126">-EnablePartitioning</span></span>
<span data-ttu-id="ef03a-127">Указывает, следует ли включить секционирование темы в нескольких брокерах сообщений.</span><span class="sxs-lookup"><span data-stu-id="ef03a-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="ef03a-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ef03a-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="ef03a-129">Максимальный размер темы в мегабайтах, которая является размером памяти, выделенной для темы.</span><span class="sxs-lookup"><span data-stu-id="ef03a-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="ef03a-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef03a-130">-Name</span></span>
<span data-ttu-id="ef03a-131">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="ef03a-131">Topic Name.</span></span>

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

### <span data-ttu-id="ef03a-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ef03a-132">-Namespace</span></span>
<span data-ttu-id="ef03a-133">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ef03a-133">Namespace Name.</span></span>

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

### <span data-ttu-id="ef03a-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="ef03a-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="ef03a-135">Указывает, требуется ли для темы обнаружение повторяющихся данных.</span><span class="sxs-lookup"><span data-stu-id="ef03a-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="ef03a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef03a-136">-ResourceGroupName</span></span>
<span data-ttu-id="ef03a-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef03a-137">The name of the resource group</span></span>

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

### <span data-ttu-id="ef03a-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ef03a-138">-SizeInBytes</span></span>
<span data-ttu-id="ef03a-139">Указывает размер темы в байтах.</span><span class="sxs-lookup"><span data-stu-id="ef03a-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="ef03a-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="ef03a-140">-SupportOrdering</span></span>
<span data-ttu-id="ef03a-141">Указывает, поддерживает ли раздел сортировку.</span><span class="sxs-lookup"><span data-stu-id="ef03a-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="ef03a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef03a-142">-Confirm</span></span>
<span data-ttu-id="ef03a-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef03a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef03a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef03a-144">-WhatIf</span></span>
<span data-ttu-id="ef03a-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef03a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef03a-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef03a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef03a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef03a-147">CommonParameters</span></span>
<span data-ttu-id="ef03a-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef03a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef03a-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef03a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef03a-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef03a-150">INPUTS</span></span>

### <span data-ttu-id="ef03a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ef03a-151">System.String</span></span>

### <span data-ttu-id="ef03a-152">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef03a-152">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ef03a-153">System. Nullable "1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ef03a-153">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ef03a-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef03a-154">OUTPUTS</span></span>

### <span data-ttu-id="ef03a-155">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="ef03a-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="ef03a-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef03a-156">NOTES</span></span>

## <span data-ttu-id="ef03a-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef03a-157">RELATED LINKS</span></span>
