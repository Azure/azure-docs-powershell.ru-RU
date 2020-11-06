---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561475"
---
# <span data-ttu-id="3cf71-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="3cf71-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="3cf71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cf71-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf71-103">Возвращает описание для указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3cf71-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cf71-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cf71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf71-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf71-106">Командлет **Get-AzureRmServiceBusQueue** Возвращает описание указанной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="3cf71-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="3cf71-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cf71-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf71-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3cf71-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="3cf71-109">Возвращает описание очереди.</span><span class="sxs-lookup"><span data-stu-id="3cf71-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="3cf71-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cf71-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf71-111">-DefaultProfile</span></span>
<span data-ttu-id="3cf71-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cf71-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3cf71-113">-Name</span></span>
<span data-ttu-id="3cf71-114">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="3cf71-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf71-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3cf71-115">-Namespace</span></span>
<span data-ttu-id="3cf71-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3cf71-116">Namespace Name.</span></span>

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

### <span data-ttu-id="3cf71-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf71-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cf71-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3cf71-118">The name of the resource group</span></span>

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

### <span data-ttu-id="3cf71-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf71-119">CommonParameters</span></span>
<span data-ttu-id="3cf71-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cf71-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf71-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf71-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf71-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cf71-122">INPUTS</span></span>

### <span data-ttu-id="3cf71-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3cf71-123">-ResourceGroup</span></span>
 <span data-ttu-id="3cf71-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf71-124">System.String</span></span>
 

### <span data-ttu-id="3cf71-125">-+ +</span><span class="sxs-lookup"><span data-stu-id="3cf71-125">-NamespaceName</span></span>
 <span data-ttu-id="3cf71-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf71-126">System.String</span></span>
 

### <span data-ttu-id="3cf71-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="3cf71-127">-QueueName</span></span>
 <span data-ttu-id="3cf71-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf71-128">System.String</span></span> 

## <span data-ttu-id="3cf71-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf71-129">OUTPUTS</span></span>

### <span data-ttu-id="3cf71-130">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="3cf71-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="3cf71-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cf71-131">NOTES</span></span>

## <span data-ttu-id="3cf71-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cf71-132">RELATED LINKS</span></span>

