---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073739"
---
# <span data-ttu-id="ac6a1-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ac6a1-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="ac6a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6a1-103">Возвращает описание для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="ac6a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac6a1-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac6a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac6a1-105">DESCRIPTION</span></span>
<span data-ttu-id="ac6a1-106">Возвращает описание для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="ac6a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac6a1-107">EXAMPLES</span></span>

### <span data-ttu-id="ac6a1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac6a1-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

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
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="ac6a1-109">Возвращает описание очереди.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="ac6a1-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ac6a1-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="ac6a1-111">Возвращает список очередей для заданного пространства имен, по умолчанию возвращаются очереди 100, если больше 100 очередей, которые нужно вернуть, и используйте параметр-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="ac6a1-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ac6a1-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="ac6a1-113">Возвращает список первых очередей 150 для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="ac6a1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac6a1-114">PARAMETERS</span></span>

### <span data-ttu-id="ac6a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6a1-115">-DefaultProfile</span></span>
<span data-ttu-id="ac6a1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac6a1-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ac6a1-117">-MaxCount</span></span>
<span data-ttu-id="ac6a1-118">Определите максимальное количество возвращаемых очередей.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6a1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac6a1-119">-Name</span></span>
<span data-ttu-id="ac6a1-120">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="ac6a1-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6a1-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac6a1-121">-Namespace</span></span>
<span data-ttu-id="ac6a1-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="ac6a1-122">Namespace Name</span></span>

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

### <span data-ttu-id="ac6a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac6a1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-124">The name of the resource group</span></span>

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

### <span data-ttu-id="ac6a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6a1-125">CommonParameters</span></span>
<span data-ttu-id="ac6a1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac6a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6a1-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac6a1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6a1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac6a1-128">INPUTS</span></span>

### <span data-ttu-id="ac6a1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ac6a1-129">System.String</span></span>

## <span data-ttu-id="ac6a1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac6a1-130">OUTPUTS</span></span>

### <span data-ttu-id="ac6a1-131">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="ac6a1-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ac6a1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac6a1-132">NOTES</span></span>

## <span data-ttu-id="ac6a1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac6a1-133">RELATED LINKS</span></span>
