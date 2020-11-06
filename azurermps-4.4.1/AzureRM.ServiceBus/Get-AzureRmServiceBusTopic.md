---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559523"
---
# <span data-ttu-id="1d9bc-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="1d9bc-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="1d9bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9bc-103">Возвращает описание для указанной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d9bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d9bc-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9bc-106">Командлет **Get-AzureRmServiceBusTopic** Возвращает описание раздела для указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1d9bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d9bc-107">EXAMPLES</span></span>

### <span data-ttu-id="1d9bc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d9bc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="1d9bc-109">Возвращает описание указанной темы для заданного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="1d9bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d9bc-110">PARAMETERS</span></span>

### <span data-ttu-id="1d9bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9bc-111">-DefaultProfile</span></span>
<span data-ttu-id="1d9bc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9bc-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-113">-Name</span></span>
<span data-ttu-id="1d9bc-114">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d9bc-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d9bc-115">-Namespace</span></span>
<span data-ttu-id="1d9bc-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-116">Namespace Name.</span></span>

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

### <span data-ttu-id="1d9bc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d9bc-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d9bc-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-118">The name of the resource group</span></span>

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

### <span data-ttu-id="1d9bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9bc-119">CommonParameters</span></span>
<span data-ttu-id="1d9bc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9bc-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d9bc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9bc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d9bc-122">INPUTS</span></span>

### <span data-ttu-id="1d9bc-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1d9bc-123">-ResourceGroup</span></span>
 <span data-ttu-id="1d9bc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9bc-124">System.String</span></span>
 

### <span data-ttu-id="1d9bc-125">-+ +</span><span class="sxs-lookup"><span data-stu-id="1d9bc-125">-NamespaceName</span></span>
 <span data-ttu-id="1d9bc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9bc-126">System.String</span></span>
 

### <span data-ttu-id="1d9bc-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="1d9bc-127">-TopicName</span></span>
 <span data-ttu-id="1d9bc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1d9bc-128">System.String</span></span>

## <span data-ttu-id="1d9bc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d9bc-129">OUTPUTS</span></span>

### <span data-ttu-id="1d9bc-130">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="1d9bc-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="1d9bc-131">Name (имя): SB-Topic_exampl1 расположение: Западная часть US ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type: Microsoft. ServiceBus/Topic AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: Microsoft. Azure. Management. ServiceBus. Models. MessageCountDetails DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false: ложь MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false SizeInBytes: 0 1/20/2017 3:16:43</span><span class="sxs-lookup"><span data-stu-id="1d9bc-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="1d9bc-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d9bc-132">NOTES</span></span>

## <span data-ttu-id="1d9bc-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d9bc-133">RELATED LINKS</span></span>

