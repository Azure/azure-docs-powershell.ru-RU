---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 25a64b352622cf9c057ce0e3f38bc3e4e122e22a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732898"
---
# <span data-ttu-id="bfb3b-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="bfb3b-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="bfb3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb3b-103">Возвращает описание для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfb3b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfb3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb3b-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb3b-106">Возвращает описание для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="bfb3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfb3b-107">EXAMPLES</span></span>

### <span data-ttu-id="bfb3b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bfb3b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

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

<span data-ttu-id="bfb3b-109">Возвращает описание очереди.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="bfb3b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bfb3b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="bfb3b-111">Возвращает список очередей для заданного пространства имен, по умолчанию возвращаются очереди 100, если больше 100 очередей, которые нужно вернуть, и используйте параметр-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="bfb3b-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bfb3b-112">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="bfb3b-113">Возвращает список первых очередей 150 для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="bfb3b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfb3b-114">PARAMETERS</span></span>

### <span data-ttu-id="bfb3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb3b-115">-DefaultProfile</span></span>
<span data-ttu-id="bfb3b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb3b-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bfb3b-117">-MaxCount</span></span>
<span data-ttu-id="bfb3b-118">Определите максимальное количество возвращаемых очередей.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="bfb3b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfb3b-119">-Name</span></span>
<span data-ttu-id="bfb3b-120">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="bfb3b-120">Queue Name</span></span>

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

### <span data-ttu-id="bfb3b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bfb3b-121">-Namespace</span></span>
<span data-ttu-id="bfb3b-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="bfb3b-122">Namespace Name</span></span>

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

### <span data-ttu-id="bfb3b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb3b-123">-ResourceGroupName</span></span>
<span data-ttu-id="bfb3b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-124">The name of the resource group</span></span>

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

### <span data-ttu-id="bfb3b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb3b-125">CommonParameters</span></span>
<span data-ttu-id="bfb3b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfb3b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb3b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb3b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb3b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfb3b-128">INPUTS</span></span>

### <span data-ttu-id="bfb3b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bfb3b-129">System.String</span></span>

## <span data-ttu-id="bfb3b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfb3b-130">OUTPUTS</span></span>

### <span data-ttu-id="bfb3b-131">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="bfb3b-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="bfb3b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfb3b-132">NOTES</span></span>

## <span data-ttu-id="bfb3b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfb3b-133">RELATED LINKS</span></span>
