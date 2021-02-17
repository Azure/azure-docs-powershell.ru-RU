---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212657"
---
# <span data-ttu-id="73968-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="73968-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="73968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73968-102">SYNOPSIS</span></span>
<span data-ttu-id="73968-103">Возвращает описание указанной очереди "Автобусы обслуживания".</span><span class="sxs-lookup"><span data-stu-id="73968-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="73968-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73968-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73968-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73968-105">DESCRIPTION</span></span>
<span data-ttu-id="73968-106">Возвращает описание указанной очереди "Автобусы обслуживания".</span><span class="sxs-lookup"><span data-stu-id="73968-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="73968-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73968-107">EXAMPLES</span></span>

### <span data-ttu-id="73968-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73968-108">Example 1</span></span>
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

<span data-ttu-id="73968-109">Возвращает описание очереди.</span><span class="sxs-lookup"><span data-stu-id="73968-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="73968-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="73968-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="73968-111">Возвращает список очередей для заданного пространства имен. По умолчанию возвращается 100 очередей, если возвращается более 100 очередей, используйте параметр -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="73968-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="73968-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="73968-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="73968-113">Возвращает список первых 150 очередей для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="73968-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="73968-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73968-114">PARAMETERS</span></span>

### <span data-ttu-id="73968-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73968-115">-DefaultProfile</span></span>
<span data-ttu-id="73968-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73968-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73968-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="73968-117">-MaxCount</span></span>
<span data-ttu-id="73968-118">Определите максимальное количество очередей, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="73968-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="73968-119">-Name</span><span class="sxs-lookup"><span data-stu-id="73968-119">-Name</span></span>
<span data-ttu-id="73968-120">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="73968-120">Queue Name</span></span>

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

### <span data-ttu-id="73968-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73968-121">-Namespace</span></span>
<span data-ttu-id="73968-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="73968-122">Namespace Name</span></span>

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

### <span data-ttu-id="73968-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73968-123">-ResourceGroupName</span></span>
<span data-ttu-id="73968-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="73968-124">The name of the resource group</span></span>

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

### <span data-ttu-id="73968-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73968-125">CommonParameters</span></span>
<span data-ttu-id="73968-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73968-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73968-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73968-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73968-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73968-128">INPUTS</span></span>

### <span data-ttu-id="73968-129">System.String</span><span class="sxs-lookup"><span data-stu-id="73968-129">System.String</span></span>

## <span data-ttu-id="73968-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73968-130">OUTPUTS</span></span>

### <span data-ttu-id="73968-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="73968-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="73968-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73968-132">NOTES</span></span>

## <span data-ttu-id="73968-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73968-133">RELATED LINKS</span></span>
